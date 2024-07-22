---
title: 工作階段目錄
description: 作業階段目錄是提供請求作業階段屬性的材質目錄，以及所有src=、vignette=和icc=命令的預設catId值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# 工作階段目錄{#session-catalog}

工作階段目錄是提供要求的工作階段屬性的材質目錄，以及所有`src=`、`vignette=`和`icc=`命令的預設catId值。

工作階段目錄會指定為HTTP要求路徑的第一個路徑元素（緊接在伺服器名稱后面）。 如果第一個路徑元素與任何目錄的attribute：：RootId不相符，則會使用預設目錄作為工作階段目錄。

作業階段目錄提供下列作業階段預設值：

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>屬性 </p> </th> 
   <th class="entry"> <p>附註 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：RootPath</span> </p> </td> 
   <td> <p> 材質資料檔案的根路徑 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：VignettePath</span> </p> </td> 
   <td> <p> 暈映檔案的根路徑 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：IccProfileRgb</span> </p> </td> 
   <td> <p> 如果暈映未內嵌ICC設定檔，則為預設的工作色域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：RootUrl</span> </p> </td> 
   <td> <p> <span class="codeph"> src=</span>命令中相對HTTP檔案路徑的根URL </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：ShowOverlapObjs</span> </p> </td> 
   <td> <p> 重疊物件的初始顯示/隱藏狀態 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：Expiration</span> </p> </td> 
   <td> <p> Proxy伺服器和瀏覽器快取回覆影像的存留時間值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：MaxPix</span> </p> </td> 
   <td> <p> 允許的回覆影像寬度與高度上限 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：DefaultPix</span> </p> </td> 
   <td> <p> <span class="codeph"> wid=</span>和<span class="codeph"> hei=</span>的預設值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：Format</span> </p> </td> 
   <td> <p> <span class="codeph"> fmt=</span>的預設值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：JpegQuality</span> </p> </td> 
   <td> <p> <span class="codeph"> qlt=</span>的預設值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：TiffEncoding</span> </p> </td> 
   <td> <p> TIFF影像輸出的壓縮型別 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：銳利化</span> </p> </td> 
   <td> <p> <span class="codeph">銳利化的預設值=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：OnFailSel</span> </p> </td> 
   <td> <p> 指定<span class="codeph"> sel=</span>命令失敗時的行為 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph">屬性：：OnFailObj</span> </p> </td> 
   <td> <p> 指定<span class="codeph"> obj=</span>命令失敗時的行為 </p> </td> 
  </tr> 
 </tbody> 
</table>
