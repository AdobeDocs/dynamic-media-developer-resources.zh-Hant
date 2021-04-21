---
description: 與範例A類似的需求，但使用純色背景，並允許合成影像的高度不同，以容納具有不同外觀比例的影像。
solution: Experience Manager
title: 範例B
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '176'
ht-degree: 0%

---


# 範例B{#example-b}

與範例A類似的需求，但使用純色背景，並允許合成影像的高度不同，以容納具有不同外觀比例的影像。

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 目錄：:Id</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 目錄：：修飾詞</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp;layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp;圖層=1&amp;tf=...$text$...rtf-encoding&amp;rotate=-90&amp;originN=.5,rigigin0&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

將影像放置在圖層0中，並將`size=`的高度值設定為0，這使得將影像縮放為800像素寬後，實際高度由影像的高度確定。

`extend=` 在頂端和底部加上100像素，在右側加上200像素。

圖層0和圖層1的原點都位於合成區域的中右側，以達到所需的文字位置。

下圖顯示了不同影像長寬比和不同文本字串的合成結果。

![](assets/exampleb.png)

