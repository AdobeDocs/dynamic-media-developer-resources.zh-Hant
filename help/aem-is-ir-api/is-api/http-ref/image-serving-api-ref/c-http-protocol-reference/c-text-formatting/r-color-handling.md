---
title: 色彩處理
description: RTF規格允許以&bsol；colortbl指定的RGB色彩值。 每個元件分別提供&bsol；red、&bsol；green和&bsol；blue指令。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 590ed0f1-8d78-4afc-ac9e-c28272cd24a6
TQID: 'https://experienceleague.adobe.com/w5IfFwmdMegueJbDMjwvb5XCPuemRcJ1XTqcJFgdEMQ'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 275
ht-degree: 0%

---

# 色彩處理{#color-handling}

RTF規格允許`\colortbl`所指定的RGB色彩值。 每個元件分別提供`\red`、`\green`和`\blue`命令。

專有的RTF延伸命令`\cmykcolortbl`允許指定CMYK色彩，每個色彩元件都有`\cyan`、`\magenta`、`\yellow`和`\black`命令。

`\colortbl`的顏色元件值在0到255的範圍內。 `\cmykcolortbl`的元件值在0到100的範圍內。

`textPs=`支援的RTF延伸模組命令`\*\iscolortbl`提供指定具有標準「影像伺服」色彩值的色彩表的方法，並支援完整的RGB、灰色、CMYK和Alpha。 其語法如下：

` {\&#42;\iscolortbl; *[!DNL colors]*;}`

*[!DNL colors]*&#x200B;一或多個IS色彩值，以「；」分隔

可以在相同的`text=`或`textPs=` RTF字串中指定多種型別的色彩表。 每個色彩表可以有不同的專案數。 「影像伺服」會嘗試在`\colortbl`之前依此順序尋找顏色： `\iscolortbl`在`\cmykcolortbl`之前（僅當文字圖層的畫素型別為CMYK時）。 僅適用於`textPs=`，如有需要（例如，已指定RGB色彩，但需要CMYK輸出），可在CMYK和RGB之間精確轉換顏色。 如果找不到特定索引值的顏色，則會使用預設顏色（黑色）。

如需IS色彩值的語法說明，請參閱[色彩](/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md)。

## 限制 {#section-c5173e672d854e4aa9656844f7fc4d0e}

修飾元`text=`不支援`\*\iscolortbl`。 修飾元`textPs=`不支援`\cmykcolortbl`。

呈現Photofonts時會忽略顏色選取範圍。

## 範例 {#section-0f166bb72bd44479be01131077851142}

允許使用變數控制三種文字色彩，同時當在標準RTF文字編輯器中開啟RTF字串時仍顯示色彩預設值。

`…&$c1=ff0000&$c2=00ff00&$c3=0000ff&textPs={{\*\iscolortbl;$c1$;$c2$;$c3$;}{\colortbl;\red255;\green0;\blue0;\red0;\green255;\blue0;\red0;\green0;\blue255;}…}…`
