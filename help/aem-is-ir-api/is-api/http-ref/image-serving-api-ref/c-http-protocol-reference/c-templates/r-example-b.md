---
description: 與範例A類似的需求，但使用實色背景，並允許複合影像的高度變化，以容納具有不同外觀比例的影像。
solution: Experience Manager
title: 範例B
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 0%

---

# 範例B{#example-b}

與範例A類似的需求，但使用實色背景，並允許複合影像的高度變化，以容納具有不同外觀比例的影像。

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 目錄：:Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 目錄：：修飾詞</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here+tes&amp;layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp;layer=1&amp;text=rtf...$text$....rtf-encoding&amp;rotate=-90&amp;originN=.5,0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

影像被放置在層0中，並且`size=`的高度值被設定為0，這導致在將影像縮放到800像素寬後，實際高度由影像的高度確定。

`extend=` 在上方和下方新增100像素，在右側新增200像素。

第0層和第1層的原點都放置在複合區域的中右側，以達到所需的文本位置。

下圖顯示影像的不同外觀比例和不同文字字串的複合結果。

![](assets/exampleb.png)
