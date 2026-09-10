---
title: UV 像素密度
description: 學習如何使用 Substance 3D Painter 的 UV Texel 密度產生器。
source-git-commit: b7770a9497f0db047433aec32c31b57f8dc13ae7
workflow-type: tm+mt
source-wordcount: '204'
ht-degree: 0%

---


# UV 像素密度

<table>
  <tr style="border: 0;">
    <td style="border: 0;" valign="top"><img src="../../../assets/generators/icon_uv_texel_density.png" alt=""/><br><strong>在：</strong> 紫外線、尺寸、實用性</td>
    <td style="border: 0;" valign="top"><strong>說明</strong><br>UV Texel 密度產生器透過從低到高的彩色漸層來視覺化網格的像素密度。<br>UV Texel 密度產生器輸出全色紋理，最適合用於填充層，以識別不一致的 UV 縮放並確保模型紋理細節均勻。</td>
  </tr>
</table>

>[!NOTE]
>
> 像素密度指的是你模型某一表面積內的紋素（紋理像素）數量。 高的像素密度代表你可以在模型的小區域內塞入大量細節，而低像素密度可能限制細節量，但能提升效能。 一般來說，不論材質解析度如何，建議保持網格的紋素密度一致，因為像素密度差異很大，觀眾常常能察覺，這會讓資產感覺品質較低或不夠真實。

## 參數

| 參數名稱 | 說明 |
| --- | --- |
| **低色** | 設定低紋素密度區域&#x200B;****&#x200B;的顏色。 |
| **色彩媒介** | 設定中等像素密度區域的&#x200B;****&#x200B;顏色。 |
| **色彩高** | 設定高紋素密度區域&#x200B;****&#x200B;的顏色。 |
