---
description: 下列選項可控制暈映檔案的處理。 如果sourceFile不是暈映，則會忽略它們。
seo-description: 下列選項可控制暈映檔案的處理。 如果sourceFile不是暈映，則會忽略它們。
seo-title: 暈映選項
solution: Experience Manager
title: 暈映選項
topic: Scene7 Image Serving - Image Rendering API
uuid: 0cb40314-07ce-496b-a27b-560d7bb4fa8e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# 暈映選項{#options-for-vignettes}

下列選項可控制暈映檔案的處理。 如果sourceFile不是暈映，則會忽略它們。

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -內容</span> </p></td> 
  <td class="stentry"> <p>建立表示對象層次並包括選定對象屬性的XML檔案。 檔案的內容與req=contents命令返回 <span class="codeph"> 的內容相同</span> 。 該檔案與源檔案的名稱相同，但帶有 <span class="filepath"> .xml尾碼</span> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-裁剪 <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid hei</span><span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>縮放前先裁切暈映。 </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> y</span></span> 是裁切矩形的左上角，wid <span class="codeph"><span class="varname"> ,</span>hei<span class="varname"></span></span> 是裁切矩形的大小。 值是相對於源暈映的全解析度視圖影像的像素坐標。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widn</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>縮放前先裁切暈映。 </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> yn</span></span> 是裁切矩形的左上角， <span class="codeph"><span class="varname"> widn</span>,<span class="varname"> hein</span></span> 是裁切矩形的大小。 值會相對於來源暈映的檢視影像進行標準化，且必須介於0.0...1.0之間。 </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span> 和yn <span class="codeph"><span class="varname"> +</span></span>hein<span class="codeph"><span class="varname"></span></span> 不得大於1.0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -嵌入材料</span> </p></td> 
  <td class="stentry"> <p>將內嵌的材質保留在輸出暈映中。 預設情況下，材料會從輸出暈映中移除。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-高 <span class="varname"> 度</span></span> </p></td> 
  <td class="stentry"> <p>一個或多個輸出暈映高度（以像素為單位）。 如果指定-info，則忽略。 <span class="varname"> ival</span> 可以是0，表示輸入暈映的寬度。 如需詳 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 細資訊，請參閱暈映縮放</a> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>啟用從暈映擷取影像地圖檔案。 地圖資料會寫入僅包含&lt;map&gt;元素 <span class="codeph"> 的HTML檔</span> 。 輸出檔案的名稱與輸出影像檔案相同，但 <span class="filepath"> 帶。htm</span> 尾碼。 如果指定命令但暈映中沒有映射資料，則會生成警告消息，並且不建立任何檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -設定檔</span> </p></td> 
  <td class="stentry"> <p>將內嵌在暈映中的ICC配置檔案副本保存到檔案。 如果指定命令但暈映中沒有ICC配置檔案，則會生成警告消息，並且不建立ICC配置檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -金字塔</span> </p></td> 
  <td class="stentry"> <p>建立金字塔暈映。 當要與Scene7縮放檢視器一起顯示轉譯的影像時，此為必要項。 如需詳 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 細資訊</a> ，請參閱暈映縮放。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-縮圖寬 <span class="varname"> 度</span></span> </p></td> 
  <td class="stentry"> <p>縮圖影像的像素寬度和高度限制。 如果指定，則從暈映視圖影像、櫃式檔案的面板影像或窗口覆蓋樣式檔案中第一樣式的照明映射中生成寬度不大且不高於ival的JPEG影像。 <span class="varname"></span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>一或多個輸出暈映寬度（像素）。 如果指定 <span class="codeph"> -info</span> ，則忽略。 <span class="varname"> ival</span> 可以是0，這表示輸入暈映的高度。 如需詳 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 細資訊，請參閱暈映縮放</a> 。 </p></td> 
 </tr> 
</table>

