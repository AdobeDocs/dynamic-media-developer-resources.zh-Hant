---
title: SVG
description: 只有在需要SVG轉譯時才能考量此區段中的設定。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
TQID: 'https://experienceleague.adobe.com/B9kyf-cEvz6A-IPoeY6jLzP4mUnGoG2ZjxAGKexdDpE'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 271
ht-degree: 0%

---

# SVG{#svg}

只有在需要SVG轉譯時才能考量此區段中的設定。

## SV：：SvgHeapSize - SVG棧積大小 {#section-59ab17681daa4be8b5d794713e1a504e}

SVG轉譯器的Java棧積大小。 預設為「200m」(200 MB)。

## PS：：svgProvider.rootPaths - SVG資料根資料夾 {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

SVG來源資料檔案的位置。 可以是相對於&#x200B;*[!DNL install_folder]*&#x200B;的一或多個絕對檔案路徑或路徑（以分號分隔）。 通常設定為與`IS::RootPath`相同的值。

## PS：：svgProvider.SVGFileSizeLimit - SVG檔案大小上限 {#section-b9c81e3e104642ebbdd9f000843d3256}

SVG來源檔案大小上限（以千位元組為單位）。 嘗試轉譯大於此限制的SVG檔案時，伺服器會傳回錯誤。 預設值為1024 KB。

## IS：：SvgMAxRenderRgnPixels - SVG輸出影像大小限制 {#section-5be1fd9639424d878a5ffd11736d3920}

它會限制SVGRender可產生的影像大小。 大於0的整數值（百萬畫素）。 如果轉譯作業超過大小限制，則會傳回錯誤。 預設值為4。

## PS：：svgProvider.port - [!DNL Platform Server]接聽連線埠 {#section-f7e42a96c2dd4523b46f0557c239e659}

用於SvgRender從[!DNL Platform Server]取得影像以內嵌於SVG轉譯的連線埠。

重要若想讓SVGRender元件正確運作，此組態選項必須設定為與`TC::PsPort`相同的值。

## PS：：svgProvider.fontRoot - SVG字型檔案資料夾 {#section-a8d45b0d68504945b8780f5eac351b0d}

指定SvgRender尋找轉譯SVG文字所需字型檔案的位置；通常是`IS::RootPaths`中指定的路徑之一。 預設值為[!DNL *[!DNL install_folder]*/images]。

## SVG：：SVGRender.port， IS：：SVGTcpPort - SVG通訊連線埠 {#section-608687123aa644b7b58fe42385d71b79}

設定影像伺服器和SVGRender元件通訊的連線埠。

>[!NOTE]
>
>為了讓SVGRender元件正確運作，必須為`SVG::SVGRender.port`和`IS::SVGTcpPort`指定相同的連線埠號碼。
