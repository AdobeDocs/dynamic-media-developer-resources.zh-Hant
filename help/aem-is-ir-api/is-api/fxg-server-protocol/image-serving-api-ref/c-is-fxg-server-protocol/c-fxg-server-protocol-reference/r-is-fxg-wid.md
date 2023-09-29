---
title: wid
description: 檢視寬度。 指定回覆影像（檢視影像）的寬度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 2%

---

# wid{#wid}

檢視寬度。 指定回覆影像（檢視影像）的寬度。

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>影像寬度（以畫素為單位，int大於0）， </p></td> 
 </tr> 
</table>

## 預設 {#section-830bae0b6bac440098444d7cdcb23e2e}

如果兩者皆非 `wid=`， `hei=`、或 `scale=` 指定時，回覆影像為FXG檔案中指定的預設檢視大小。

點陣化格式會使用「預設檢視大小」(或「預設畫素」(DefaultPix)設定)呈現。 按一下 **[!UICONTROL 應用程式設定]** > **[!UICONTROL 發佈設定]** > **[!UICONTROL 影像伺服器]**，然後輸入您的「寬度」和「高度」值。 更小尺寸可提供更優異的效能。 儲存您的設定並執行影像伺服發佈以套用變更。

如果您套用 `scale=1` 指令，點陣化格式要求會以FXG中指定的大小呈現。

## 範例 {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

除非指定格式，否則影像會呈現為SWF檔案。 在這種情況下，高度和寬度沒有意義，因為SWF通常會展開到瀏覽器視窗的大小。 因此， `hei` 和 `wid` 僅適用於點陣化或PDF格式。 點陣化格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* tif-alpha
* png-alpha
