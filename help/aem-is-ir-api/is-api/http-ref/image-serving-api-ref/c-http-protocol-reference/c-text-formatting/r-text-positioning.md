---
title: 文本定位
description: 將text= renderer應用於預定大小的圖層時（即當也指定了size=時），文本的位置與textPs= renderer的位置有根本的不同。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 092444bf-9964-4d97-b06e-3add033da284
source-git-commit: 24667a5ebab54ba22c4a3f6b52d19d7a31a93576
workflow-type: tm+mt
source-wordcount: '302'
ht-degree: 0%

---

# 文本定位{#text-positioning}

的 `text=` 呈現器將文本定位在與應用於預定大小的圖層時完全不同的位置（即當也指定了size=時）。

自調整大小 `text=`和 `textPs=` 圖層具有相似的外觀和定位。

的 `textPs=` 將字元單元格的頂部與文本框的頂部對齊(假定 `\vertalt`)，即使它導致部分渲染的文本字形部分延伸到文本框邊界之外。 某些字型的渲染字形也可能略微突出到文本框的左右邊緣之外。 對於要求圖層矩形中包含所有渲染文本的應用程式，RTF `\marg*` 或 `textFlowPath=` 可用於調整文本渲染區域。

相反， `text=` 根據需要移動渲染的文本，並確保所有渲染的字形完全適合在指定的文本框內。

同時 `text=` 對於簡單的應用程式，可能會稍微容易一些， `textPs=` 提供與字面和文本效果無關的精確定位。

## 範例 {#section-1b6bdf2ea34447528188ae4e1430ee71}

以下示例用於預定大小的文本。 自調整文本大小的行為不同。

** `Text=` 始終在頂部提供一個窄邊距：**

![文本定位示例一個影像](assets/tp01.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20Normal%20Normal`

** `textPs=` 將文本緊對齊到文本框頂部，這會導致輕微剪切，即使是常用字型，如Arial®:**

![文本定位示例二圖](assets/tp02.png)

`/is/image/?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20Normal%20Normal`

** `text=` 自動將渲染的文本向下移動以避免剪切：**

![文本定位示例三幅影像](assets/tp03.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&text=\fs40Normal%20{\up20Raised%20}Normal`

** `textPs=` 不移動包含凸起部分的文本，如果文本位於圖層0:**上，則會導致顯著剪切

![文本定位示例四幅影像](assets/tp04.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\fs40Normal%20{\up20Raised%20}Normal`

**頂部的10 pt(200 twips)邊距將呈現此文本，而不進行剪貼：**

![文本定位示例五幅影像](assets/tp05.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs=\margt200\fs40Normal%20{\up20Raised}%20Normal`

**某些指令碼字型的渲染字形可能會顯著擴展到文本框之外：**

![文本定位示例六幅影像](assets/tp06.png)

`/is/image?size=230,50&bgc=f0f0f0&fmt=png&textPs={\fonttbl{\f1\fcharset0%20FluffyFont;}}\f1\fs88%20fluffy%20font%20problems`
