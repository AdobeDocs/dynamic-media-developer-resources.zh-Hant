---
description: 建立具有靜態背景影像的固定大小範本、與左側中心背景對齊且縮放為不超過背景寬度和高度80%的可變影像，以及位於畫布右側邊緣的垂直文字圖層。
seo-description: 建立具有靜態背景影像的固定大小範本、與左側中心背景對齊且縮放為不超過背景寬度和高度80%的可變影像，以及位於畫布右側邊緣的垂直文字圖層。
seo-title: 範例A
solution: Experience Manager
title: 範例A
topic: Scene7 Image Serving - Image Rendering API
uuid: c250dbc8-1e32-46b8-ba55-c1fb0ae62695
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 範例A{#example-a}

建立具有靜態背景影像的固定大小範本、與左側中心背景對齊且縮放為不超過背景寬度和高度80%的可變影像，以及位於畫布右側邊緣的垂直文字圖層。

![](assets/examplea.png)

## 範本記錄 {#section-32f54710593e438fa0622224c89380af}

插入物件

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 目錄：:Id </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 目錄：：修飾詞 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp;layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp;圖層=2&amp;$text=layer+2+text+ges here&amp;text=rtf...$text$...rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0 </span> </p> </td> 
 </tr> 
</table>

在模 `origin=` 板中明確指定所有圖層的值，以嚴格控製圖層的定位和對齊。 每個圖層原點都會設為與該圖層的所需對齊方式相符。 背 `origin=` 景（0層）設定在中心；這是任意的，因為背景影像在運行時不會改變；可以使用層0原點的任何值。

這些 `pos=` 值提供圖層原點之間的必要偏移，以達到所需的圖層定位。

第1層影像的錨點位於左中心；結合值，這 `pos=` 就可以實現背景和第1層影像之間的左心對齊，而不管第1層影像的長寬比如何。

同樣地，文字圖層的錨點位於自動調整大小文字方塊的右中心。 與pos=搭配使用，可獲得旋轉文字所需的右中心對齊方式，不受字型大小和字串長度的影響。

實際的顯示文字會在執行時期提供，因此會使用變數來將文字與RTF格式封套分隔開。 我們會針對第1層影 `$object` 像使用預設變數。 這允許在請求路徑中指定此影像。

任何影像都可用於背景影像和第1層影像。 如果背景影像有遮色片，則未遮色片的區域會填入預設背景顏色( `attribute::BkgColor`)，或在或時會保持透明 `fmt=png-alpha` 狀態 `fmt=tif-alpha`。 如果背景影像具有非方形的長寬比，則在回復影像中置中，並且額外的空間被填充 `attribute::BkgColor`。 如果第1層影像有Alpha資料或遮色片，背景影像（或背景顏色）將會保留在透明區域中。 如果影像沒有遮色片，則會填滿整個已分配的矩形。

## 使用範本 {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`伺服器`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

下圖顯示了圖層1影像不同外觀比例和不同文字字串的複合結果。

![](assets/exampleausing.png)

