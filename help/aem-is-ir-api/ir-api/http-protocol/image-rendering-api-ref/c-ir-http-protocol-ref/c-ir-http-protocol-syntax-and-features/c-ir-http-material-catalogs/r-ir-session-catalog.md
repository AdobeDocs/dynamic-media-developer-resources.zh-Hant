---
description: 會話目錄是提供請求會話屬性的材料目錄，以及所有src=、vignette=和icc=命令的預設catId值。
seo-description: 會話目錄是提供請求會話屬性的材料目錄，以及所有src=、vignette=和icc=命令的預設catId值。
seo-title: 作業目錄
solution: Experience Manager
title: 作業目錄
topic: Scene7 Image Serving - Image Rendering API
uuid: 69c0f6cd-dfaf-47bf-bdd9-7abb4e6f7465
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 作業目錄{#session-catalog}

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
   <td> <p> src=命令中相對HTTP檔案路徑的 <span class="codeph"> 根URL</span> </p> </td> 
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
   <td> <p> wid=和 <span class="codeph"> hei=的</span><span class="codeph"> 預設值</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：：格式</span> </p> </td> 
   <td> <p> fmt=的 <span class="codeph"> 預設值</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:JpegQuality</span> </p> </td> 
   <td> <p> qlt=的預 <span class="codeph"> 設值</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:TiffEncoding</span> </p> </td> 
   <td> <p> TIFF影像輸出的壓縮類型 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：：銳利化</span> </p> </td> 
   <td> <p> 銳利化的預 <span class="codeph"> 設值=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:OnFailSel</span> </p> </td> 
   <td> <p> 指定sel=命令失 <span class="codeph"> 敗時的</span> 行為 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:OnFailObj</span> </p> </td> 
   <td> <p> 指定obj=命令失 <span class="codeph"> 敗時的</span> 行為 </p> </td> 
  </tr> 
 </tbody> 
</table>

