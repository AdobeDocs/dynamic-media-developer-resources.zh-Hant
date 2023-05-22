---
description: 與示例A類似的要求，但使用純色背景並允許合成的高度改變，以適應具有不同長寬比的影像。
solution: Experience Manager
title: 示例B
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 90ef96fc-c12f-4fc8-b465-6520b71f4e7b
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '174'
ht-degree: 0%

---

# 示例B{#example-b}

與示例A類似的要求，但使用純色背景並允許合成的高度改變，以適應具有不同長寬比的影像。

<table id="simpletable_37BA3B2A75A9468C9ADEBBC034BADAE7"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> 目錄：:ID</span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> 目錄：：修改量</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> myTemplate2</span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> $text=layer+1+text+goes+here&amp;layer=0&amp;size=800,0&amp;extend=0,100,200,100&amp;src=$object$&amp;originN=.5,0&amp;layer=1&amp;text=rtf.....rtf-encoding&amp;rotate=-90&amp;originN=.50&amp;posN=0.5,0</span> </p></td> 
 </tr> 
</table>

影像放置在圖層0中，其高度值 `size=` 設定為0。 此設定將使實際高度由縮放到800像素寬後的影像高度確定。

變數 `extend=` 在頂部和底部添加100像素，在右側添加200像素。

層0和層1的原點都位於合成區域的中右側，以達到所需的文本位置。

下圖顯示了不同長寬比和不同文本字串的複合結果。

![示例B影像](assets/exampleb.png)
