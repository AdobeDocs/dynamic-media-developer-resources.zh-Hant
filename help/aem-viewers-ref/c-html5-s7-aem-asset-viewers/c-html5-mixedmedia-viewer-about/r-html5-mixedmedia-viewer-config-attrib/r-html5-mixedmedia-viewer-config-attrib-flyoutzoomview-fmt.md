---
description: 指定元件用於從Image Server載入映像的映像格式。
seo-description: 指定元件用於從Image Server載入映像的映像格式。
seo-title: FlyoutZoomView.fmt
solution: Experience Manager
title: FlyoutZoomView.fmt
topic: Dynamic media
uuid: 6f6a69b4-d581-44ff-b089-ce9d0d0170bf
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# FlyoutZoomView.fmt{#flyoutzoomview-fmt}

指定元件用於從Image Server載入映像的映像格式。

`[FlyoutZoomView.|<containerId>_flyout.]fmt=jpg|jpeg|png|png-alpha|gif|gif-alpha`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> jpg|jpeg|png|png-alpha|gif|gif-alpha</span> </p> </td> 
   <td colname="col2"> <p> 如果指定的格式以 <span class="codeph"> -alpha結尾</span>，元件會將影像轉譯為透明內容。 對於所有其他影像格式，元件會將影像視為不透明。 </p> <p>請注意，元件預設有白色背景。 因此，若要將它完全透明，請將背 <span class="codeph"> 景顏色</span> CSS屬性設 <span class="codeph"> 為透明</span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選填。

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`jpeg`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`fmt=png-alpha`
