---
description: 只有在需要SVG呈現時，才需要考慮本節中的設定。
solution: Experience Manager
title: SVG
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 2863cc86-1f79-4db3-bd6f-a42839ef3439
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '266'
ht-degree: 1%

---

# SVG{#svg}

只有在需要SVG呈現時，才需要考慮本節中的設定。

## SV::SvgHeapSize -SVG堆大小 {#section-59ab17681daa4be8b5d794713e1a504e}

SVG呈現器的Java堆大小。 預設為「200m」(200 MB)。

## PS::svgProvider.rootPaths -SVG資料根資料夾 {#section-70fe575b0ad54e3b8b6d3a01ea8f1f44}

SVG源資料檔案的位置。 可以是一個或多個相對於 *[!DNL install_folder]*，用分號分隔。 通常設定為與 `IS::RootPath`。

## PS::svgProvider.SVGFileSizeLimit — 最大SVG檔案大小 {#section-b9c81e3e104642ebbdd9f000843d3256}

最大SVG源檔案大小（千位元組）。 當嘗試呈現大於此限制的SVG檔案時，伺服器返回錯誤。 預設值為1024 KB。

## IS::SvgMAxRenderRgnPixels -SVG輸出影像大小限制 {#section-5be1fd9639424d878a5ffd11736d3920}

限制SVGRender可生成的影像大小。 大於0的整數值（以百萬像素為單位）。 如果渲染操作將超過大小限制，則返回錯誤。 預設為 4。

## PS::svgProvider.port - [!DNL Platform Server] 偵聽埠 {#section-f7e42a96c2dd4523b46f0557c239e659}

用於SvgRender從 [!DNL Platform Server] 嵌入到SVG繪畫中。

重要資訊：要正確運行SVGRender元件，必須將此配置選項設定為與 `TC::PsPort`。

## PS::svgProvider.fontRoot -SVG字型檔案資料夾 {#section-a8d45b0d68504945b8780f5eac351b0d}

指定SvgRender在何處找到呈現SVG文本所需的字型檔案；通常指定的路徑之一 `IS::RootPaths`。 預設值為[!DNL  *[!DNL install_folder]*/images]。

## SVG::SVGRender.port, IS::SVGTcpPort -SVG通信埠 {#section-608687123aa644b7b58fe42385d71b79}

配置Image Server和SVGRender元件通信的埠。

>[!NOTE]
>
>要使SVGRender元件正確運行，必須為 `SVG::SVGRender.port` 和 `IS::SVGTcpPort`。
