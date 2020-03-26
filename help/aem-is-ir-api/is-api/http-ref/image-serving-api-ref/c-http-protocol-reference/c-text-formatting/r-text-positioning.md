---
description: 當套用至預先調整大小的圖層時（亦即指定size=時）,text= renderer會將文字定位在與textPs= renderer根本不同的位置。
seo-description: 當套用至預先調整大小的圖層時（亦即指定size=時）,text= renderer會將文字定位在與textPs= renderer根本不同的位置。
seo-title: 文字定位
solution: Experience Manager
title: 文字定位
topic: Scene7 Image Serving - Image Rendering API
uuid: 77289c50-2f3a-4486-8274-eecfd6e5452f
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 文字定位{#text-positioning}

當套用至預先調整大小的圖層時（亦即指定size=時）,text= renderer會將文字定位在與textPs= renderer根本不同的位置。

自動調整大小 `text=`和圖 `textPs=` 層的外觀和位置類似。

`textPs=` 將字元單元格的頂部與文本框的頂部對齊(假設 `\vertalt`)，即使這會導致部分渲染的文本字元部分延伸到文本框邊界之外。 某些字型的轉換字元也可能略微突出到文字方塊的左右邊緣之外。 對於要求所有渲染文本都包含在圖層矩形中的應用程式，可 `\marg*` 以使 `textFlowPath=` 用RTF命令或來調整文本渲染區域。

相反地， `text=` 會視需要移動轉譯的文字，並確保所有轉譯的字元完全符合指定的文字方塊。

雖然 `text=` 簡單應用程式的使用稍為簡單，但提供 `textPs=` 的精確定位與字型臉和文字效果無關。

## 範例 {#section-1b6bdf2ea34447528188ae4e1430ee71}

以下範例適用於預先調整大小的文字。 自行調整文字大小的行為不同。

** `Text=` 始終在頂部提供窄邊距：**

![](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` 將文字與文字方塊頂端緊密對齊，這可能會造成輕微剪裁，即使是常用字型（例如Arial）亦然：**

![](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

**將 `text=` 自動將轉換的文字向下移動，以避免剪裁：**

![](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

**不 `textPs=` 會移動包含凸起部分的文字，如果文字位於圖層0上，會造成顯著的剪裁：**

![](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**頂端的10點(200 twips)邊界會呈現此文字，而不會剪裁：**

![](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**特定指令碼字型的轉譯字元可能會明顯延伸至文字方塊外：**

![](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
