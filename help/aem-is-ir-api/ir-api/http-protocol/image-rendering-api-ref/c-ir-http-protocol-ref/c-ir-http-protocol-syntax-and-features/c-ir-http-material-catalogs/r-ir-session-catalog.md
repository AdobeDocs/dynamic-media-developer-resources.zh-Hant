---
description: 會話目錄是提供請求會話屬性的材料目錄，以及所有src=、vignette=和icc=命令的預設catId值。
solution: Experience Manager
title: 作業目錄
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '248'
ht-degree: 0%

---


# 會話目錄{#session-catalog}

會話目錄是提供請求會話屬性的材料目錄，以及所有src=、vignette=和icc=命令的預設catId值。

會話目錄被指定為HTTP請求路徑的第一個路徑元素（緊接在伺服器名稱后面）。 如果第一個路徑元素與任何目錄的屬性：:RootId不匹配，則會使用預設目錄作為作業目錄。

會話目錄提供以下會話預設值：

<table id="table_DB5E0DD8E9B440A4964A1326433597C8"> 
 <thead> 
  <tr> 
   <th class="entry"> <p>屬性 </p> </th> 
   <th class="entry"> <p>附註 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:RootPath</span> </p> </td> 
   <td> <p> 材料資料檔案的根路徑 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:VignettePath</span> </p> </td> 
   <td> <p> 暈映檔案的根路徑 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:IccProfileRgb</span> </p> </td> 
   <td> <p> 如果暈映未內嵌ICC描述檔，則預設工作色域 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:RootUrl</span> </p> </td> 
   <td> <p> <span class="codeph"> src=</span>命令中相對HTTP檔案路徑的根URL </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:ShowOverlapObjs</span> </p> </td> 
   <td> <p> 重疊物件的初始顯示／隱藏狀態 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：：到期</span> </p> </td> 
   <td> <p> 代理伺服器和瀏覽器快取的回覆映像的即時值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:MaxPix</span> </p> </td> 
   <td> <p> 允許的回覆影像寬度和高度上限 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:DefaultPix</span> </p> </td> 
   <td> <p> <span class="codeph"> wid=</span>和<span class="codeph"> hei=</span>的預設值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：：格式</span> </p> </td> 
   <td> <p> <span class="codeph"> fmt=</span>的預設值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:JpegQuality</span> </p> </td> 
   <td> <p> <span class="codeph"> qlt=</span>的預設值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:TiffEncoding</span> </p> </td> 
   <td> <p> TIFF影像輸出的壓縮類型 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：：銳利化</span> </p> </td> 
   <td> <p> <span class="codeph">銳利化的預設值=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:OnFailSel</span> </p> </td> 
   <td> <p> 指定<span class="codeph"> sel=</span>命令失敗時的行為 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:OnFailObj</span> </p> </td> 
   <td> <p> 指定<span class="codeph"> obj=</span>命令失敗時的行為 </p> </td> 
  </tr> 
 </tbody> 
</table>

