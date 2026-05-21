---
title: hei
description: 檢視高度。 指定回覆影像的高度。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: dcc9311d-4157-490b-9fc4-47060ddb0e37
TQID: 'https://experienceleague.adobe.com/Tpl8zVXQVzs3isa26A3YvnOzs6gqpz3-4L-qDBx-eK0'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 174
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

點陣化格式會使用「預設檢視大小」(或「預設畫素」(DefaultPix)設定)呈現。 選取&#x200B;**[!UICONTROL 應用程式設定]** > **[!UICONTROL 發佈設定]** > **[!UICONTROL 影像伺服器]**，然後輸入您的寬度和高度值。 更小尺寸可提供更優異的效能。 儲存您的設定並執行影像伺服發佈以套用變更。

如果您套用`scale=1`命令，則會以FXG中指定的大小呈現點陣化格式要求。

## 預設 {#section-76ee3daa77cb468ab310821357cc9404}

如果未指定`wid=`、`hei=`或`scale=`，則回覆影像為FXG檔案中指定的預設檢視大小。

## 範例 {#section-a91c14d31e71481ba054412d9f642885}

[!DNL `http://server/is/agm/myRootId/myImageId?hei=200`]

除非指定格式，否則影像會呈現為SWF檔案。 在此情況下，高度和寬度沒有意義，因為SWF通常會展開至瀏覽器視窗的大小。 因此，hei和wid僅適用於點陣化或PDF格式。 點陣化格式包括：

* GIF
* TIF
* PNG
* JPG
* JPEG
* GIF-alpha
* tif-alpha
* png-alpha
