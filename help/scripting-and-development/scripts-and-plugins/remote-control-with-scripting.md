---
helpx_url: "https://helpx.adobe.com/tw/substance-3d-painter/scripting-and-development/scripts-and-plugins/remote-control-with-scripting.html"
breadcrumb-title: ''
description: 學習如何在 Substance 3D Painter 中使用遠端控制腳本來自動化工作流程並以程式化方式控制應用程式。
helpx_creative_field: ""
helpx_description: Painter > Scripting and development > Scripts and plugins > Remote control with scripting
helpx_experience_level: ""
helpx_learn_topic: ""
helpx_tags: ""
title: 帶有腳本的遠端控制
user-guide-description: ''
user-guide-title: ''
source-git-commit: 9f20406f682e0e6a2e9a423e81c5ecfc7430ecfd
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 0%

---


# 帶有腳本的遠端控制

本頁說明如何遠端控制應用程式以執行 Javascript 或 Python 指令。\
這需要特定的命令列參數，然後一個簡單的 Python 腳本就能執行現有 Javascript 和 Python API 中可用的任何指令。

## 啟動應用程式

為了遠端控制應用程式，必須以以下命令列啟動 Substance 3D Painter：

```
"Adobe Substance 3D painter.exe" --enable-remote-scripting
```


>[!NOTE]
>
> 在執行任何腳本之前，請先用這個指令確認應用程式已經啟動並能正常運作。 如果應用程式還在啟動或還沒準備好，腳本可能會失敗。

## 遠端控制腳本

以下的 Python 腳本可作為函式庫與應用程式溝通。

請將以下腳本儲存在名為 **lib\_remote.py** 的檔案中，這樣下面的範例才能正常運作。

```
import sys 

import json 

import base64 

import subprocess 

 

if sys.version_info >= (3, 0): 

 import http.client as http 

else: 

 import httplib as http 

 

class RemotePainter() : 

 def __init__(self, port=60041, host='localhost'): 

  self._host = host 

  self._port = port 

 

## Json server connection

  self._PAINTER_ROUTE = '/run.json' 

  self._HEADERS = {'Content-type': 'application/json', 'Accept': 'application/json'} 

 

## Execute a HTTP POST request to the Substance Painter server and send/receive JSON data

 def _jsonPostRequest( self, route, body, type ) : 

  connection = http.HTTPConnection(self._host, self._port, timeout=3600) 

  connection.request('POST', route, body, self._HEADERS) 

  response = connection.getresponse() 

 

  data = response.read() 

  connection.close() 

 

  if type == "js" : 

   data = json.loads( data.decode('utf-8') ) 

 

   if 'error' in data: 

    OutJson = json.loads( body.decode() ) 

    print( base64.b64decode( OutJson["js"] ) ) 

    raise ExecuteScriptError(data['error']) 

  else : 

## Python can return nothing, so decoding can fail

   try: 

    data = data.decode('utf-8').rstrip() 

   except: 

    pass 

 

  return data 

 

 def checkConnection(self): 

  connection = http.HTTPConnection(self._host, self._port) 

  connection.connect() 

 

## Execute a command

 def execScript( self, script, type ) : 

  Command = base64.b64encode( script.encode('utf-8') ) 

 

  if type == "js" : 

   Command = '{{"js":"{0}"}}'.format( Command.decode('utf-8') ) 

  else : 

   Command = '{{"python":"{0}"}}'.format( Command.decode('utf-8') ) 

 

  Command = Command.encode( "utf-8" ) 

 

  return self._jsonPostRequest( self._PAINTER_ROUTE, Command, type ) 

 

class PainterError(Exception): 

 def __init__(self, message): 

  super(PainterError, self).__init__(message) 

 

class ExecuteScriptError(PainterError): 

 def __init__(self, data): 

  super(PainterError, self).__init__('An error occured when executing script: {0}'.format(data)) 

 
```


## 範例

以下是兩個簡單的範例，說明如何在應用程式支援的兩個 API 中執行指令：

### 執行 Javascript 指令

API 中的大多數 Javascript 函式會回傳 String 或 Json 資料，這讓它們在 Python 腳本中操作起來很方便。 傳送和接收資料時應該不會有重大問題。

建立一個名為 **example\_js.py** 的 Python 腳本檔案，並加入以下程式碼：

```
import lib_remote 

 

Remote = lib_remote.RemotePainter() 

Remote.checkConnection() 

 

## Print the API version

Version = Remote.execScript( "alg.version.painter", "js" ) 

print( Version ) 

 

## Get a list of all the files in the default shelf/library:

Files = Remote.execScript( 'alg.resources.findResources("starter_assets", "*")', "js" ) 

 

for File in Files : 

 print( File )
```


如果應用程式是用命令列執行，執行這個腳本會讓它執行指令並取得結果。

### 執行 Python 指令

大多數 Python 函式可能會回傳無法傳送到遠端腳本的物件，這表示為了接收資料，必須明確轉換成字串或 JSON 字典。

為了簡化流程，你可以建立自訂的 Python 腳本，在應用程式啟動時載入，並呼叫處理這類轉換的函式，而不必依賴內嵌轉換。

建立一個名為 **example\_py.py** 的 Python 腳本檔案，並加入以下程式碼：

```
import lib_remote 

 

Remote = lib_remote.RemotePainter() 

Remote.checkConnection() 

 

## import the substance_painter module to make

## its API available to us

Remote.execScript( "import substance_painter", "python" ) 

 

## Print the API version

Version = Remote.execScript( "substance_painter.__version__", "python" ) 

print( Version ) 

 

## Get a list of all the files in the default shelf/library

## Because the search function return objects, we have to convert

## the information into a string within the same command (inline)

Command = 'substance_painter.resource.search( "p:starter_assets/" )' 

Command = '"|||".join( [ x.identifier().url() for x in {0}] )'.format( Command ) 

 

Files = Remote.execScript( Command, "python" ) 

Files = Files.split( "|||" ) 

 

for File in Files : 

 print( File )
```


如果應用程式是用命令列執行，執行這個腳本會讓它執行指令並取得結果。
