---
description: 查看高度。 指定回復影像的高度。
solution: Experience Manager
title: hei
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# hei{#hei}

查看高度。 指定回復影像的高度。

`hei= *`谷`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> 谷</span></span> </p> </td> 
  <td class="stentry"> <p>影像高度（以像素為單位）（大於0的整數）。 </p></td> 
 </tr> 
</table>

柵格格式使用「預設視圖大小」(Default View Size)（或DefaultPix設定）呈現。 按一下 **[!UICONTROL 應用程式設定]** > **[!UICONTROL 發佈設定]** > **[!UICONTROL 映像伺服器]**，然後輸入「寬度」和「高度」值。 較小的尺寸可提供更好的效能。 必須保存設定並執行「影像服務發佈」以應用更改。

如果應用 `scale=1` 命令，以在FXG中指定的大小呈現光柵格式請求。

## 預設 {#section-76ee3daa77cb468ab310821357cc9404}

如果兩者都不 `wid=`。 `hei=`，或 `scale=` ，回復影像是在FXG檔案中指定的預設視圖大小。

## 範例 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

除非指定格式，否則影像將呈現為SWF檔案。 在這種情況下，高度和寬度沒有意義，因為SWF通常會擴展到瀏覽器窗口的大小。 因此，hei和wid僅應用於光柵或PDF格式。 光柵格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIFα
* TIF-α
* PNG-α
