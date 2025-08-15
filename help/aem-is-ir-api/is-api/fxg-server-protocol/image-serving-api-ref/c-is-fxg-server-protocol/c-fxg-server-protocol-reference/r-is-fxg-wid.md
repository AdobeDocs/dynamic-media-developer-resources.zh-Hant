---
title: wid
description: 檢視寬度。 指定回覆影像（檢視影像）的寬度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 6a4c1f4425199cfa6088fc42137552748c1a9dcf
workflow-type: tm+mt
source-wordcount: '173'
ht-degree: 1%

---

# wid{#wid}

檢視寬度。 指定回覆影像（檢視影像）的寬度。

`wid= *`值`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">值</span></span> </p> </td> 
  <td class="stentry"> <p>影像寬度（以畫素為單位，int大於0）， </p></td> 
 </tr> 
</table>

## 預設 {#section-830bae0b6bac440098444d7cdcb23e2e}

若未指定`wid=`、`hei=`或`scale=`，則回覆影像為FXG檔案中指定的預設檢視大小。

點陣化格式會使用「預設檢視大小」(或「預設畫素」(DefaultPix)設定)呈現。 按一下&#x200B;**[!UICONTROL 應用程式設定]** > **[!UICONTROL 發佈設定]** > **[!UICONTROL 影像伺服器]**，然後輸入您的寬度和高度值。 更小尺寸可提供更優異的效能。 儲存您的設定並執行影像伺服發佈以套用變更。

如果您套用`scale=1`命令，則會以FXG中指定的大小呈現點陣化格式要求。

## 範例 {#section-2f72cb2653d54c6aaacf0d97521fb72c}

`http://server/is/agm/myRootId/myImageId?wid=200`

除非指定格式，否則影像會呈現為SWF檔案。 在此情況下，高度和寬度沒有意義，因為SWF通常會展開至瀏覽器視窗的大小。 因此，`hei`和`wid`只適用於點陣或PDF格式。 點陣化格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* tif-alpha
* png-alpha
