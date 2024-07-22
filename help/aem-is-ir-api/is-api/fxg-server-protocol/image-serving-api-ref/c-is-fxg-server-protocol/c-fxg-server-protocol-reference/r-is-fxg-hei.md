---
title: hei
description: 檢視高度。 指定回覆影像的高度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '171'
ht-degree: 1%

---

# hei{#hei}

檢視高度。 指定回覆影像的高度。

`hei= *`值`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">值</span></span> </p> </td> 
  <td class="stentry"> <p>影像高度，以畫素為單位（int大於0）。 </p></td> 
 </tr> 
</table>

點陣化格式會使用「預設檢視大小」(或「預設畫素」(DefaultPix)設定)呈現。 選取&#x200B;**[!UICONTROL 應用程式設定]** > **[!UICONTROL Publish設定]** > **[!UICONTROL 影像伺服器]**，然後輸入您的寬度和高度值。 更小尺寸可提供更優異的效能。 儲存您的設定並執行影像伺服Publish以套用變更。

如果您套用`scale=1`命令，則會以FXG中指定的大小呈現點陣化格式要求。

## 預設 {#section-76ee3daa77cb468ab310821357cc9404}

如果未指定`wid=`、`hei=`或`scale=`，則回覆影像為FXG檔案中指定的預設檢視大小。

## 範例 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

除非指定格式，否則影像會呈現為SWF檔案。 在這種情況下，高度和寬度沒有意義，因為SWF通常會展開到瀏覽器視窗的大小。 因此，hei和wid僅適用於點陣化或PDF格式。 點陣化格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* tif-alpha
* png-alpha
