---
description: 檢視寬度。 指定回覆影像（檢視影像）的寬度。
solution: Experience Manager
title: wid
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 5edd045c-600e-4295-9672-04a5c3bc651d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 3%

---

# wid{#wid}

檢視寬度。 指定回覆影像（檢視影像）的寬度。

`wid= *`val`*`

<table id="simpletable_8229FEFB366F4A799C206FD3E3C601BA"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname"> val</span></span> </p> </td> 
  <td class="stentry"> <p>影像寬度（以像素為單位）（整數大於0）, </p></td> 
 </tr> 
</table>

## 預設 {#section-830bae0b6bac440098444d7cdcb23e2e}

如果未指定`wid=`、`hei=`或`scale=`，則回復影像為FXG檔案中指定的預設視圖大小。

柵格格式使用「預設視圖大小」(Default View Size)（或「DefaultPix」設定）呈現。 按一下「**[!UICONTROL 應用程式設定]** > **[!UICONTROL 發佈設定]** > **[!UICONTROL 影像伺服器]**」，然後輸入您的寬度和高度值。 較小的尺寸可提供更好的效能。 您必須儲存設定並執行「影像伺服發佈」以套用變更。

如果應用`scale=1`命令，則按照FXG中指定的大小呈現柵格格式請求。

## 範例 {#section-2f72cb2653d54c6aaacf0d97521fb72c}

[!DNL http://server/is/agm/myRootId/myImageId?wid=200]

除非指定格式，否則影像將呈現為SWF檔案。 在這種情況下，高度和寬度沒有意義，因為SWF通常會擴展到瀏覽器窗口的大小。 因此，hei和wid僅適用於光柵或PDF格式。 光柵格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* TIF-α
* PNG-alpha
