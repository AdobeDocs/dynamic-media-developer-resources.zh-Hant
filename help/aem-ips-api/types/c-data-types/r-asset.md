---
description: 資料夾階層中的物件或容器。
seo-description: 資料夾階層中的物件或容器。
seo-title: 資產
solution: Experience Manager
title: 資產
topic: Scene7 Image Production System API
uuid: 758ac593-98d8-4366-a723-a06435c7fd3c
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 資產{#asset}

資料夾階層中的物件或容器。

語法

## 參數 {#section-0f2abb29deaf4d73bbbd0a5a2dc9ca3b}

<table id="table_C58EF9963CB34179A9D6C9F0F6FF24F2"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> acoInfo</span></span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 動 <span class="varname"> 畫GifInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AnimatedGifInfo</span> </td> 
   <td colname="col3"> GIF動畫檔案的詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 資 <span class="varname"> 產控制代碼</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 資產控制代碼。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> assetSetInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 文 <span class="varname"> 件櫃資訊</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：檔案櫃資訊</span> </td> 
   <td colname="col3"> 檔案櫃資產類型的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 已 <span class="varname"> 建立</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 資產上傳的日期和時間。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> createUser</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 建立資產之使用者的電子郵件地址。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> css資訊</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：CssInfo</span> </td> 
   <td colname="col3"> CSS檔案的詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> cuePointInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> excelInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fileName</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">返回虛擬檔案名。 完整的虛擬檔案路徑是 <span class="codeph"> folder</span>+<span class="codeph"> fileName</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> flashInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 資 <span class="varname"> 料夾</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 包含資產的資料夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> folderHandle <span class="varname"> (資料夾句柄</span> ) </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 處理資產的父資料夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> fontInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> type:fontInfo</span> </td> 
   <td colname="col3"> 字型資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> iccProfileInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：IccProfileInfo</span> </td> 
   <td colname="col3"> ICC描述檔資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> illustrator資訊</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> imageInfo <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ImageInfo</span> </td> 
   <td colname="col3"> 影像資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> inDesignInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> ipsImageUrl</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 代表資產縮圖檢視的相對URL。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> javascriptInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：JavascriptInfo</span> </td> 
   <td colname="col3"> JavaScript檔案的詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 上次 <span class="varname"> 修改</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 上次修改資產的日期和時間。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> lastModifyUser</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 上次修改資產之使用者的電子郵件地址。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> layerViewInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：LayerViewInfo</span> </td> 
   <td colname="col3"> 圖層檢視資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 遮色 <span class="varname"> 片資訊</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> masterVideoInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 中繼 <span class="varname"> 資料陣列</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：MetadataArray</span> </td> 
   <td colname="col3"> 與資產相關聯的中繼資料值陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 資產名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdf資訊</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> pdf設定資訊</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：PdfSettingsInfo</span> </td> 
   <td colname="col3"> PDF設定資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 權 <span class="varname"> 限</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> postScriptInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> powerPointInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> premiereExpressInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 專 <span class="varname"> 案</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 專案名稱清單。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> psd資訊</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 就 <span class="varname"> 緒發佈</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 設定標幟，以指出資產是否應發佈。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> renderSceneInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：RenderSceneInfo</span> </td> 
   <td colname="col3"> 演算場景資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> rtf資訊</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 子 <span class="varname"> 類型</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">支援子類型值的一般資產子類型(例如 <span class="codeph"> AssetSet</span>)。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> svg資訊</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：SvgInfo</span> </td> 
   <td colname="col3"> SVG資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> swcInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：SwcInfo</span> </td> 
   <td colname="col3"> SWC資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 范 <span class="varname"> 本資訊</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：模板資訊</span> </td> 
   <td colname="col3"> 範本資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 垃圾 <span class="varname"> 州</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 指出資產是位於垃圾筒還是即時（如需值，請參閱「垃圾筒狀態」）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 類型</span></span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">資產類型. 有關值 <a href="../../string-constants/c-string-constants/r-asset-types.md#reference-2fe75d230663419d88632d30f1144a10" format="dita" scope="local"> ，請參閱</a> 「資產類型」。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> videoCaptionInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：VideoCaptionInfo</span> </td> 
   <td colname="col3"> <p>視訊標題資產的屬性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 視 <span class="varname"> 訊資訊</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> <p>視訊資產的屬性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> viewerPresetInfo <span class="varname"> (檢視器預設集資訊</span> ) </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ViewerPresetInfo</span> </td> 
   <td colname="col3"> 檢視器預設資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 檢視 <span class="varname"> 器SwfInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ViewerSwfInfo</span> </td> 
   <td colname="col3"> 檢視器SWf資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 暈映資訊</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：暈映資訊</span> </td> 
   <td colname="col3"> 暈映資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 浮 <span class="varname"> 水印資訊</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：WatermarkInfo</span> </td> 
   <td colname="col3"> 浮水印資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> windowCoveringInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：WindowCoveringInfo</span> </td> 
   <td colname="col3"> 涵蓋資產的視窗屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> wordInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xmlInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：XmlInfo</span> </td> 
   <td colname="col3"> XML資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xslInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：XslInfo</span> </td> 
   <td colname="col3"> XSL資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> zipInfo</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 程式碼片語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>

