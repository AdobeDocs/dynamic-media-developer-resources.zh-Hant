---
title: 範例A
description: 使用靜態背景影像建立固定大小的範本，此可變影像在左中心與背景對齊，並縮放至不超過背景寬度和高度的80%。 最後，在畫布的右邊緣置中對齊垂直文字的文字圖層。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '468'
ht-degree: 0%

---

# 範例A{#example-a}

使用靜態背景影像建立固定大小的範本，此可變影像在左中心與背景對齊，並縮放至不超過背景寬度和高度的80%。 最後，在畫布的右邊緣置中對齊垂直文字的文字圖層。

![範例影像](assets/examplea.png)

## 範本記錄 {#section-32f54710593e438fa0622224c89380af}

插入物件

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">目錄：：識別碼</span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">目錄：：修飾元</span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp;layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp;layer=2&amp;$text=layer+2+text+goes+here&amp;text=rtf....$text$..rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;poseN=0.5,0&amp;posisN=0.5,0.5,0 </span> </p> </td> 
 </tr> 
</table>

所有圖層的`origin=`值都在範本中明確指定，以嚴格控制圖層的定位和對齊。 每個圖層原點都會設定為符合該圖層的所需對齊方式。 背景（圖層0）的`origin=`設定為中央；這個值是任意的，因為背景影像在執行階段不會變更；可以使用圖層0原點的任何值。

`pos=`值會提供圖層原點之間的必要位移，以達到所要的圖層位置。

第1層影像的錨點位於左中央，值為`pos=`。 此設定可達成背景和第一層影像之間的左中心對齊，無論第一層影像的外觀比例為何。

同樣地，文字圖層的錨點位於自動調整大小的文字方塊的中央，且值為`pos=`。 此設定可達成旋轉文字所需的置中右對齊，不受字型大小和字串長度影響。

實際顯示文字是在執行階段提供，因此使用變數將文字與rtf格式信封分開。 預設變數`$object`用於圖層1影像。 此變數可讓您在請求路徑中指定此影像。

任何影像都可以用於背景影像和圖層1影像。 如果背景影像有遮色片，則未遮色的區域會以預設的背景顏色( `attribute::BkgColor`)填滿，或在`fmt=png-alpha`或`fmt=tif-alpha`時保持透明。 如果背景影像具有非正方形外觀比例，它會在回覆影像中置中，而額外的空間會以`attribute::BkgColor`填滿。 如果圖層1影像有Alpha資料或遮色片，背景影像（或背景顏色）仍會顯示在透明區域中。 如果影像沒有遮色片，則會填滿整個配置的矩形。

## 使用範本 {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`伺服器`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

下圖顯示圖層1影像的不同外觀比例和不同文字字串的合成結果。

![範例複合結果影像](assets/exampleausing.png)
