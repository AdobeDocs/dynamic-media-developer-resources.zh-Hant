---
description: 下列選項可控制暈映檔案的處理。 如果sourceFile不是暈映，則會忽略它們。
solution: Experience Manager
title: 暈映選項
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 0%

---

# 暈映選項{#options-for-vignettes}

下列選項可控制暈映檔案的處理。 如果sourceFile不是暈映，則會忽略它們。

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -內容</span> </p></td> 
  <td class="stentry"> <p>建立表示對象層次結構的XML檔案，並包括所選對象屬性。 檔案的內容與<span class="codeph"> req=contents</span>命令返回的內容相同。 檔案的名稱與源檔案相同，但尾碼為<span class="filepath"> .xml</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> — 農作物 <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> 木頭</span></span> </p></td> 
  <td class="stentry"> <p>縮放前先裁切暈映。 </p> <p><span class="codeph"><span class="varname"> x</span>,<span class="varname"> </span></span> 是裁切矩形的左上角， <span class="codeph"><span class="varname"> wid</span>,<span class="varname"> </span></span> 是裁切矩形的大小。值是相對於源暈映的全解析度視圖影像的像素坐標。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn xnynwidnhein <span class="varname"> </span><span class="varname"> </span><span class="varname"> </span><span class="varname"> </span></span> </p> </td> 
  <td class="stentry"> <p>縮放前先裁切暈映。 </p> <p><span class="codeph"><span class="varname"> xn</span>、<span class="varname"> </span></span> yn是裁切矩形的左上角， <span class="codeph"><span class="varname"> widn</span><span class="varname"> </span></span> 、hein是裁切矩形的大小。值會相對於源暈映的視圖影像進行標準化，且必須介於0.0..1.0之間。 </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> </span></span> widnand  <span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> </span></span> hein不得大於1.0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">  — 嵌入材料</span> </p></td> 
  <td class="stentry"> <p>將嵌入的材料保留在輸出暈映中。 預設情況下，材料從輸出暈映中移除。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> — 高 <span class="varname"> 度</span></span> </p></td> 
  <td class="stentry"> <p>一個或多個輸出暈映高度（像素）。 如果指定了 — info，則忽略。 <span class="varname"> </span> 值可以是0，表示輸入暈映的寬度。如需詳細資訊，請參閱<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">暈映縮放</a> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>啟用從暈映擷取影像映射檔案。 映射資料被寫入僅包含<span class="codeph"> &lt;map&gt;</span>元素的HTML檔案。 輸出檔案的名稱與輸出影像檔案相同，但尾碼為<span class="filepath"> .htm</span>。 如果指定命令，但暈映中沒有映射資料，則會生成警告消息，並且不會建立任何檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -設定檔</span> </p></td> 
  <td class="stentry"> <p>將內嵌於暈映中的ICC配置檔案的副本保存到檔案中。 如果指定了命令，但暈映中沒有ICC配置檔案，則將生成警告消息，並且不建立ICC配置檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">  — 金字塔</span> </p></td> 
  <td class="stentry"> <p>建立金字塔暈。 使用Dynamic Media縮放檢視器顯示轉譯的影像時為必要。 如需詳細資訊，請參閱<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">暈映縮放</a> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-thumbwidth <span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>縮圖影像的像素寬度和高度限制。 如果指定，則從暈映視圖影像、櫃式檔案的面板影像或窗口覆蓋樣式檔案中第一樣式的照明映射中生成寬度不大且不高於<span class="varname">ival</span>的JPEG影像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">- <span class="varname"> width ival</span> *[,<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>一個或多個輸出暈映寬度（像素）。 若指定<span class="codeph"> -info</span>，則忽略。 <span class="varname"> </span> 值可以是0，表示輸入暈映的高度。如需詳細資訊，請參閱<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">暈映縮放</a> 。 </p></td> 
 </tr> 
</table>
