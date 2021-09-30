---
description: 與範例A類似的需求，但使用實色背景，並允許複合影像的高度變化，以容納具有不同外觀比例的影像。
solution: Experience Manager
title: 範例B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '0'
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

影像被放置在第0層中，並且`size=`的高度值設定為0。 此設定會使實際高度在縮放至800像素寬後，由影像的高度決定。

變數`extend=`在上方和底部新增100像素，在右側新增200像素。

第0層和第1層的原點都放置在複合區域的中右側，以達到所需的文本位置。

下圖顯示影像的不同外觀比例和不同文字字串的複合結果。

![範例B影像](assets/exampleb.png)
