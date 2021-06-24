---
description: 建立一個固定大小的模板，該模板包含靜態背景影像、一個與左側中心的背景對齊、縮放到不超過背景寬度和高度的80%的可變影像，以及一個文本層，該文本層的垂直文本居中在畫布的右側邊緣。
solution: Experience Manager
title: 範例A
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 0%

---

# 範例A{#example-a}

建立一個固定大小的模板，該模板包含靜態背景影像、一個與左側中心的背景對齊、縮放到不超過背景寬度和高度的80%的可變影像，以及一個文本層，該文本層的垂直文本居中在畫布的右側邊緣。

![](assets/examplea.png)

## 範本記錄 {#section-32f54710593e438fa0622224c89380af}

插入對象

<table id="simpletable_97ECA49445634F59B3F1D100412EFC70"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 目錄：:Id  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> myTemplate1  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 目錄：：修飾詞  </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> src=backgroundImage&amp;size=1000,1000&amp;originN=0,0&amp;layer=1&amp;src=$object$&amp;size=800,800&amp;originN=-0.5,0&amp;posN=-0.5,0&amp;layer=2&amp;$text=layer+2+text+goes+text&amp;text=.....$text...rtf-encoding=-90&amp;originN=0.5,0.05,n.  </span> </p> </td> 
 </tr> 
</table>

所有層的`origin=`值在模板中顯式指定，以嚴格控制層的定位和對齊。 每個圖層原點被設定為與該圖層所需的對齊方式相匹配。 背景（第0層）的`origin=`設定為中心；這是任意的，因為在運行時，背景影像不會更改；可以使用第0層原點的任何值。

`pos=`值在層原點之間提供必要的偏移，以實現所需的層定位。

第1層影像的錨點位於左中心；結合`pos=`值，這實現背景和第1層影像之間的左心對齊，而不考慮第1層影像的長寬比。

同樣，文本層的錨點位於自動縮放文本框的右中心。 結合pos=，可實現旋轉文本所需的右中心對齊，而不受字型大小和字串長度的影響。

實際顯示文本將在運行時提供，因此使用變數將文本與rtf格式信封分開。 對於第1層影像，我們使用預設變數`$object`。 這可讓您在要求路徑中指定此影像。

任何影像都可用於背景影像和第1層影像。 如果背景影像具有遮色片，則未遮色片區域會填入預設背景顏色(`attribute::BkgColor`)，或當`fmt=png-alpha`或`fmt=tif-alpha`時保持透明。 如果背景影像具有非方形的縱橫比，則在回復影像中置中，並且額外的空間填充`attribute::BkgColor`。 如果第1層影像具有Alpha資料或遮色片，則背景影像（或背景顏色）將保持在透明區域中可見。 如果影像沒有遮色片，則會填滿整個已分配的矩形。

## 使用範本 {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`伺服器`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

下圖顯示第1層影像的不同外觀比例和不同文本字串的複合結果。

![](assets/exampleausing.png)
