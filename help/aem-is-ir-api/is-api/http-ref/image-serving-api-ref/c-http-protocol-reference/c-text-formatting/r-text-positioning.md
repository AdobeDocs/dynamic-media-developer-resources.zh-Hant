---
description: 應用於預定大小的圖層時（即當指定size=時）,text=呈現器會定位與textPs=呈現器基本不同的文本。
solution: Experience Manager
title: 文本定位
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 0%

---

# 文本定位{#text-positioning}

應用於預定大小的圖層時（即當指定size=時）,text=呈現器會定位與textPs=呈現器基本不同的文本。

自調整`text=`和`textPs=`層的外觀和位置相似。

`textPs=` 會將字元單元格的頂部與文本框的頂部對齊(假設為 `\vertalt`)，即使這會導致部分呈現的文本字形部分延伸到文本框邊界之外。某些字型的渲染字形也可能稍微突出到文本框的左右邊緣之外。 對於需要將所有渲染文本包含在圖層矩形內的應用程式，可以使用RTF `\marg*`命令或`textFlowPath=`來調整文本渲染區域。

相反地， `text=`會視需要移動呈現的文字，並確保所有呈現的字元完全符合指定的文字方塊。

雖然`text=`在簡單應用程式中的使用可能會稍微容易一些，但`textPs=`提供與字型面和文本效果無關的精確定位。

## 範例 {#section-1b6bdf2ea34447528188ae4e1430ee71}

下列範例適用於預先大小的文字。 自我調整文字的行為不同。

** `Text=`總是在頂部提供窄邊距：**

![](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=`將文本緊靠在文本框的頂部，這可能會導致輕微剪切，即使是常用字型(如Arial:**)也是如此。

![](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=`將自動向下移動已呈現的文本以避免剪切：**

![](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=`不會移動包含凸起部分的文本，如果文本位於圖層0:**，則會導致顯著剪切

![](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**頂端的10點(200 twip)邊界可呈現此文字，而不會剪裁：**

![](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**某些指令碼字型的渲染字形可能會顯著擴展到文本框之外：**

![](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
