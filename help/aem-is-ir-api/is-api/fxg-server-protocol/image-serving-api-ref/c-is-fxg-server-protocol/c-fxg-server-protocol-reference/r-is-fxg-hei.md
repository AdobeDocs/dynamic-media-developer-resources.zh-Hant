---
description: 檢視高度。 指定回覆影像的高度。
solution: Experience Manager
title: hei
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '180'
ht-degree: 3%

---


# hei{#hei}

檢視高度。 指定回覆影像的高度。

`hei= *`val`*`

<table id="simpletable_627E67D201744588815325F3C55F76A5"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>影像高度（以像素為單位，整數大於0）。 </p></td> 
 </tr> 
</table>

點陣格式是使用「預設視圖大小」(Default View Size)(或「預設影像」(DefaultPix)設定呈現的。 按一下「**[!UICONTROL 應用程式設定」>「]** > **[!UICONTROL 發佈設定」>「**[!UICONTROL &#x200B;影像伺服器」，然後輸入「寬度」和「高度」值。 ]**]**&#x200B;較小的尺寸可提供更好的效能。 您必須儲存設定並執行影像伺服發佈才能套用變更。

如果您套用`scale=1`命令，則會以FXG中指定的大小呈現點陣格式要求。

## 預設 {#section-76ee3daa77cb468ab310821357cc9404}

如果未指定`wid=`、`hei=`和`scale=`，則回覆影像是FXG檔案中指定的預設檢視大小。

## 範例 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL http://server/is/agm/myRootId/myImageId?hei=200]

除非指定格式，否則影像會呈現為SWF檔案。 在這種情況下，高度和寬度沒有意義，因為SWF通常會擴展為瀏覽器視窗的大小。 因此，hei和wid僅適用於點陣或PDF格式。 點陣格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-alpha
* PNG-alpha

