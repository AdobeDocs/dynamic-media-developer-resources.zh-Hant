---
description: 資料夾層次結構中的對象或容器。
solution: Experience Manager
title: 資產
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 943e653a-ed30-4c75-9bad-6ef5b72f5219
source-git-commit: f42378a20b58e4c5ebc961c6526d7cecabc2ae38
workflow-type: tm+mt
source-wordcount: '381'
ht-degree: 8%

---

# [!DNL Asset]{#asset}

資料夾層次結構中的對象或容器。

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
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL acoInfo]</span> </span> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL animatedGifInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：動畫Gif資訊</span> </td> 
   <td colname="col3"> 有關動畫GIF檔案的詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL assetHandle]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 資產句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL assetSetInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL cabinetInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：CabinetInfo</span> </td> 
   <td colname="col3"> 檔案櫃資產類型的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL created]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 上載資產的日期和時間。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL createUser]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 建立資產的用戶的電子郵件地址。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL cssInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：CssInfo</span> </td> 
   <td colname="col3"> 有關CSS檔案的詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL cuePointInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL excelInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL fileName]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">返回虛擬檔案名。 完整虛擬檔案路徑為 <span class="codeph"> 資料夾</span>+<span class="codeph"> 檔案名</span>。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL flashInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL folder]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 包含資產的資料夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL folderHandle]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 處理資產的父資料夾。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL fontInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：fontInfo</span> </td> 
   <td colname="col3"> 字型資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL iccProfileInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：IccProfileInfo</span> </td> 
   <td colname="col3"> ICC配置檔案資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL illustratorInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL imageInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ImageInfo</span> </td> 
   <td colname="col3"> 影像資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL inDesignInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL ipsImageUrl]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 表示資產的縮略圖視圖的相對URL。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL javascriptInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：JavascriptInfo</span> </td> 
   <td colname="col3"> 有關JavaScript檔案的詳細資訊。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL lastModified]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:dateTime</span> </td> 
   <td colname="col3"> 上次修改資產的日期和時間。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL lastModifyUser]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 上次修改資產的用戶的電子郵件地址。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL layerViewInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：LayerViewInfo</span> </td> 
   <td colname="col3"> 層視圖資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL maskInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL masterVideoInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL metadataArray]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：元資料陣列</span> </td> 
   <td colname="col3"> 與資產關聯的元資料值的陣列。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL name]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 資產名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL pdfInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL pdfSettingsInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：PdfSettingsInfo</span> </td> 
   <td colname="col3"> PDF設定資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL permissions]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL postScriptInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL powerPointInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL premiereExpressInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL projects]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 項目名稱清單。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL psdInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL readyForPublish]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean</span> </td> 
   <td colname="col3"> 設定一個標誌以指示是否應發佈資產。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL renderSceneInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：RenderSceneInfo</span> </td> 
   <td colname="col3"> 渲染場景資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL rtfInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL subType]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">支援子類型值的通用資產子類型(例如， <span class="codeph"> 資產集</span>)。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL svgInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：SvgInfo</span> </td> 
   <td colname="col3"> SVG資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL swcInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：SwcInfo</span> </td> 
   <td colname="col3"> SWC資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL templateInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：模板資訊</span> </td> 
   <td colname="col3"> 模板資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL trashState]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 指示資產是否在垃圾箱或活動（有關值，請參閱「垃圾狀態」）。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL type]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3">資產類型. 請參閱 <a href="../../string-constants/c-string-constants/r-asset-types.md#reference-2fe75d230663419d88632d30f1144a10" format="dita" scope="local"> 資產類型</a> 值。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL videoCaptionInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：VideoCaptionInfo</span> </td> 
   <td colname="col3"> <p>視頻字幕資產的屬性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL videoInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> <p>視頻資產的屬性。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL viewerPresetInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ViewerPresetInfo</span> </td> 
   <td colname="col3"> 查看器預設資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL viewerSwfInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：ViewerSwfInfo</span> </td> 
   <td colname="col3"> 查看器SWf資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL vignetteInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：VignetteInfo</span> </td> 
   <td colname="col3"> 虛擬資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL watermarkInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：水印資訊</span> </td> 
   <td colname="col3"> 水印資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL windowCoveringInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：WindowCoveringInfo</span> </td> 
   <td colname="col3"> 覆蓋資產的窗口的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL wordInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> [!DNL xmlInfo]</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：XmlInfo</span> </td> 
   <td colname="col3"> XML資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> xsl資訊</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：XslInfo</span> </td> 
   <td colname="col3"> XSL資產的屬性。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> zip資訊</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> 代碼短語 </span> </td> 
   <td colname="col3"> </td> 
  </tr> 
 </tbody> 
</table>
