---
description: 下列選項可控制暈映檔案的處理。 如果sourceFile不是暈映，則會忽略它們。
solution: Experience Manager
title: 暈映選項
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '463'
ht-degree: 0%

---


# 暈映選項{#options-for-vignettes}

下列選項可控制暈映檔案的處理。 如果sourceFile不是暈映，則會忽略它們。

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -內容</span> </p></td> 
  <td class="stentry"> <p>建立表示對象層次並包括選定對象屬性的XML檔案。 檔案的內容與<span class="codeph"> req=contents</span>命令返回的內容相同。 該檔案與源檔案的名稱相同，但具有<span class="filepath"> .xml</span>尾碼。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-作物 <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> 木</span></span> </p></td> 
  <td class="stentry"> <p>縮放前先裁切暈映。 </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> </span></span> y是裁切矩形的左上角， <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> </span></span> hei是裁切矩形的大小。值是相對於源暈映的全解析度視圖影像的像素坐標。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn  <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> xnynwidnhein</span></span> </p> </td> 
  <td class="stentry"> <p>縮放前先裁切暈映。 </p> <p><span class="codeph"><span class="varname"> xn</span>,<span class="varname"> </span></span> ynis是裁切矩形的左上角，而widn <span class="codeph"><span class="varname"> ,</span><span class="varname"> </span></span> heinis是裁切矩形的大小。值會相對於來源暈映的檢視影像進行標準化，且必須介於0.0...1.0之間。 </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> widnand  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> hein不得大於1.0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -嵌入材料</span> </p></td> 
  <td class="stentry"> <p>將內嵌的材質保留在輸出暈映中。 預設情況下，材料會從輸出暈映中移除。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-height  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>一個或多個輸出暈映高度（以像素為單位）。 如果指定-info，則忽略。 <span class="varname"> </span> ival可以是0，表示輸入暈映的寬度。如需詳細資訊，請參閱<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">暈映縮放</a>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>啟用從暈映擷取影像地圖檔案。 映射資料被寫入僅包含<span class="codeph"> &lt;map&gt;</span>元素的HTML檔案。 輸出檔案的名稱與輸出影像檔案相同，但具有<span class="filepath"> .htm</span>尾碼。 如果指定命令但暈映中沒有映射資料，則會生成警告消息，並且不建立任何檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -設定檔</span> </p></td> 
  <td class="stentry"> <p>將內嵌在暈映中的ICC配置檔案副本保存到檔案。 如果指定命令但暈映中沒有ICC配置檔案，則會生成警告消息，並且不建立ICC配置檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -金字塔</span> </p></td> 
  <td class="stentry"> <p>建立金字塔暈映。 當要使用Dynamic Media縮放檢視器顯示演算後的影像時，此為必要項。 如需詳細資訊，請參閱<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">暈映縮放</a>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth  <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>縮圖影像的像素寬度和高度限制。 如果指定，則從暈映視圖影像、櫃式檔案的面板影像或窗口覆蓋樣式檔案中第一樣式的照明映射中生成寬度不大且不高於<span class="varname"> ival</span>的JPEG影像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-width  <span class="varname"> ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>一或多個輸出暈映寬度（像素）。 如果指定<span class="codeph"> -info</span>，則忽略。 <span class="varname"> </span> ival可以是0，表示輸入暈映的高度。如需詳細資訊，請參閱<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">暈映縮放</a>。 </p></td> 
 </tr> 
</table>

