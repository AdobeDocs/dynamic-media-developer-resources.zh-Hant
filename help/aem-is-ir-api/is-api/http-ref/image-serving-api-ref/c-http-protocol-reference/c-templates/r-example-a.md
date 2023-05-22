---
title: 示例A
description: 建立具有靜態背景影像的固定大小模板，該模板是與左中心的背景對齊的可變影像，並縮放到不超過背景寬度和高度的80%。 最後，一個文本圖層，垂直文本居中在畫布的右邊緣。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '457'
ht-degree: 0%

---

# 示例A{#example-a}

建立具有靜態背景影像的固定大小模板，該模板是與左中心的背景對齊的可變影像，並縮放到不超過背景寬度和高度的80%。 最後，一個文本圖層，垂直文本居中在畫布的右邊緣。

![示例A影像](assets/examplea.png)

## 模板記錄 {#section-32f54710593e438fa0622224c89380af}

插入對象

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 目錄：:ID </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 目錄：：修改量 </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=background影像大小=1000,1000&amp;originN=0,0&amp;圖層=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;圖層=-0.5,0&amp;圖層=2&amp;$text=layer+2+text+到此處+文本=rtf...$text$..rtf-encoding&amp;rotate=-90&amp;originN=0.5,0&amp;posN=0.5,0 </span> </p> </td> 
 </tr> 
</table>

的 `origin=` 在模板中顯式指定所有圖層的值，以嚴格控製圖層的定位和對齊。 每個圖層原點都設定為與該圖層的所需對齊方式相匹配。 的 `origin=` 對於背景（第0層）設定為中心；該值是任意的，因為在運行時背景影像不會更改；可以使用層0原點的任何值。

的 `pos=` 值提供層原點之間的必要偏移，以實現所需的層定位。

第1層影像的錨點位於左中心， `pos=` 值。 此設定實現背景和第1層影像之間的左中心對齊，而不管第1層影像的縱橫比如何。

同樣，文本圖層的錨點位於自動調整大小文本框的右中心， `pos=` 值。 此設定實現了旋轉文本所需的右中心對齊，與字型大小和字串長度無關。

實際顯示文本是在運行時提供的，因此使用變數將文本與rtf格式封套分開。 預設變數 `$object` 用於第1層影像。 此變數允許您在請求路徑中指定此影像。

任何影像都可用於背景影像和第1層影像。 如果背景影像具有蒙版，則未蒙版區域將用預設背景顏色填充( `attribute::BkgColor`)，或在 `fmt=png-alpha` 或 `fmt=tif-alpha`。 如果背景影像具有非方形長寬比，則在應答影像中居中，並填充額外的空間 `attribute::BkgColor`。 如果第1層影像具有Alpha資料或蒙版，則背景影像（或背景顏色）在透明區域中保持可見。 如果影像沒有蒙版，則會填充整個分配的矩形。

## 使用模板 {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`伺服器`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

下圖顯示了圖層1影像不同長寬比和不同文本字串的複合結果。

![示例A合成結果影像](assets/exampleausing.png)
