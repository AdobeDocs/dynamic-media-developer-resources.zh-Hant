---
title: 會話目錄
description: 會話目錄是提供請求會話屬性的材料目錄，並為所有src=、vignette=和icc=命令提供一個預設的catId值。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 36e0571e-7451-423f-a1df-540680381902
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '233'
ht-degree: 0%

---

# 會話目錄{#session-catalog}

會話目錄是提供請求的會話屬性的物料目錄，並且是所有的預設catId值 `src=`。 `vignette=`, `icc=` 的雙曲餘切值。

會話目錄被指定為HTTP請求路徑（緊隨伺服器名稱后）的第一個路徑元素。 如果第一個路徑元素與任何目錄的屬性：:RootId不匹配，則預設目錄將用作會話目錄。

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
   <td> <p> 視頻檔案的根路徑 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:IccProfileRgb</span> </p> </td> 
   <td> <p> 如果視頻未嵌入ICC配置檔案，則預設工作色彩空間 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:RootUrl</span> </p> </td> 
   <td> <p> 中相對HTTP檔案路徑的根URL <span class="codeph"> src=</span> 命令 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:ShowOverlapObjs</span> </p> </td> 
   <td> <p> 重疊對象的初始顯示/隱藏狀態 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：：到期</span> </p> </td> 
   <td> <p> 代理伺服器和瀏覽器快取的回復映像的即時值 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:MaxPix</span> </p> </td> 
   <td> <p> 允許的最大回復影像寬度和高度 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:DefaultPix</span> </p> </td> 
   <td> <p> 預設值 <span class="codeph"> wid=</span> 和 <span class="codeph"> 黑=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：：格式</span> </p> </td> 
   <td> <p> 預設值 <span class="codeph"> fmt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:JpegQuality</span> </p> </td> 
   <td> <p> 預設值 <span class="codeph"> qlt=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:TiffEncoding</span> </p> </td> 
   <td> <p> 用於TIFF影像輸出的壓縮類型 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：：銳化</span> </p> </td> 
   <td> <p> 預設值 <span class="codeph"> 銳化=</span> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:OnFailSel</span> </p> </td> 
   <td> <p> 指定當 <span class="codeph"> sel=</span> 命令失敗 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"> 屬性：:OnFailObj</span> </p> </td> 
   <td> <p> 指定當 <span class="codeph"> obj=</span> 命令失敗 </p> </td> 
  </tr> 
 </tbody> 
</table>
