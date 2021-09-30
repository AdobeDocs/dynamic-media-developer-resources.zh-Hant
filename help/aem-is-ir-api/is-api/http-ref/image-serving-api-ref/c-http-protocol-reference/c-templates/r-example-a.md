---
title: 範例A
description: 建立具有靜態背景影像的固定大小模板，該影像是與左側中心的背景對齊的可變影像，並縮放到不超過背景寬度和高度的80%。 最後，一個文本層，垂直文本置於畫布的右邊。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f731b41-994d-4f1d-b42d-e14db47e4d6c
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '0'
ht-degree: 0%

---

# 範例A{#example-a}

建立具有靜態背景影像的固定大小模板，該影像是與左側中心的背景對齊的可變影像，並縮放到不超過背景寬度和高度的80%。 最後，一個文本層，垂直文本置於畫布的右邊。

![影像範例](assets/examplea.png)

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

所有層的`origin=`值在模板中顯式指定，以嚴格控制層的定位和對齊。 每個圖層原點被設定為與該圖層所需的對齊方式相匹配。 背景（第0層）的`origin=`設定為中心；此值是任意值，因為後台映像在運行時不會更改；可以使用第0層原點的任何值。

`pos=`值在層原點之間提供必要的偏移，以實現所需的層定位。

第1層影像的錨點位於左側中心，且帶有`pos=`值。 該設定實現背景和第1層影像之間的左中心對齊，而不考慮第1層影像的長寬比。

同樣，文本層的錨點位於自動縮放文本框的右中心，並帶有`pos=`值。 此設定可實現旋轉文本的右居中對齊，而與字型大小和字串長度無關。

實際顯示文本在運行時提供，因此使用變數將文本與rtf格式信封分開。 第1層影像使用預設變數`$object`。 此變數可讓您在請求路徑中指定此影像。

任何影像都可用於背景影像和第1層影像。 如果背景影像具有遮色片，則未遮色片區域會填入預設背景顏色(`attribute::BkgColor`)，或當`fmt=png-alpha`或`fmt=tif-alpha`時保持透明。 如果背景影像具有非方形的縱橫比，則在回復影像中置中，並且額外的空間填充`attribute::BkgColor`。 如果第1層影像具有Alpha資料或遮色片，則背景影像（或背景顏色）在透明區域中仍可見。 如果影像沒有遮色片，則會填入整個已分配的矩形。

## 使用範本 {#section-3e04eedc268c482db5a8cfc662c0f327}

` http:// *`伺服器`*/myRootId/anotherImage?template=myTemplate1&$text=about+the+image`

下圖顯示了第1層影像的不同外觀比例和不同文本字串的複合結果。

![複合結果影像示例](assets/exampleausing.png)
