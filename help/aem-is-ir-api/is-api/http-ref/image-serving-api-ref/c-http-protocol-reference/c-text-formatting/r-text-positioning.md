---
description: 當套用至預先調整大小的圖層時（亦即指定size=時）,text= renderer會將文字定位在與textPs= renderer根本不同的位置。
solution: Experience Manager
title: 文字定位
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---


# 文字定位{#text-positioning}

當套用至預先調整大小的圖層時（亦即指定size=時）,text= renderer會將文字定位在與textPs= renderer根本不同的位置。

自行調整`text=`和`textPs=`層的外觀和位置相似。

`textPs=` 將字元單元格的頂部與文本框的頂部對齊(假設 `\vertalt`)，即使這會導致部分渲染的文本字元部分延伸到文本框邊界之外。某些字型的轉換字元也可能略微突出到文字方塊的左右邊緣之外。 對於要求圖層矩形中包含所有渲染文本的應用程式，可使用RTF `\marg*`命令或`textFlowPath=`來調整文本渲染區域。

相反地，`text=`會視需要移動轉譯的文字，並確保所有轉譯的字元完全符合指定的文字方塊。

雖然`text=`可能較容易用於簡單應用程式，但`textPs=`提供的精確定位與字型面和文字效果無關。

## 範例 {#section-1b6bdf2ea34447528188ae4e1430ee71}

以下範例適用於預先調整大小的文字。 自行調整文字大小的行為不同。

** `Text=`總是在頂部提供窄邊距：**

![](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=`會將文字與文字方塊頂端緊密對齊，這可能會造成輕微剪裁，即使是常用字型（例如Arial:**）

![](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=`會自動將轉換的文字向下移位，以避免剪裁：**

![](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=`不會移動包含凸起部分的文本，如果文本位於圖層0上，則會導致顯著剪裁：**

![](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**頂端的10點(200 twips)邊界會呈現此文字，而不會剪裁：**

![](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**特定指令碼字型的轉譯字元可能會明顯延伸至文字方塊外：**

![](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
