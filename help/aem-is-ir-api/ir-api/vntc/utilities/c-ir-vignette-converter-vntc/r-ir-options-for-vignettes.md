---
description: 下列選項可控制暈映檔案的處理。 如果sourceFile不是暈映，則會忽略它們。
solution: Experience Manager
title: 暈映選項
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 97fbf820590b53de5a1e6ce904e44d6b0ef9a214
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 0%

---

# 暈映選項{#options-for-vignettes}

下列選項可控制暈映檔案的處理。 如果sourceFile不是暈映，則會忽略它們。

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -contents</span> </p></td> 
  <td class="stentry"> <p>建立代表物件階層的XML檔案，並包含選取的物件屬性。 檔案的內容與<span class="codeph"> req=contents</span>命令傳回的內容相同。 檔案的名稱與來源檔案相同，但尾碼為<span class="filepath"> .xml</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> — 裁切<span class="varname"> x</span><span class="varname"> y</span><span class="varname"> wid</span><span class="varname">hei</span></span> </p></td> 
  <td class="stentry"> <p>縮放前裁切暈映。 </p> <p><span class="codeph"><span class="varname"> x</span>，<span class="varname"> y</span></span>是裁切矩形的左上角，而<span class="codeph"><span class="varname"> wid</span>，<span class="varname"> hei</span></span>是裁切矩形的大小。 值是相對於來源暈映之完整解析度檢視影像的畫素座標。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> xn</span><span class="varname"> yn</span><span class="varname"> widn</span><span class="varname"> hein</span></span> </p> </td> 
  <td class="stentry"> <p>縮放前裁切暈映。 </p> <p><span class="codeph"><span class="varname"> xn</span>，<span class="varname"> yn</span></span>是裁切矩形的左上角，而<span class="codeph"><span class="varname"> widn</span>，<span class="varname"> hein</span></span>是裁切矩形的大小。 值會相對於來源暈映的檢視影像進行標準化，且必須介於0.0...1.0之間。 </p> <p><span class="codeph"><span class="varname"> xn</span></span>+<span class="codeph"><span class="varname"> widn</span></span>和<span class="codeph"><span class="varname"> yn</span></span>+<span class="codeph"><span class="varname"> hein</span></span>不得大於1.0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> — 內嵌資料</span> </p></td> 
  <td class="stentry"> <p>將內嵌材質保留在輸出暈映中。 依預設，會從輸出暈映中移除材料。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> — 高度<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>一或多個輸出暈映高度（畫素）。 如果指定 — info，則忽略。 <span class="varname"> ival</span>可以是0，代表輸入暈映的寬度。 如需詳細資訊，請參閱<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">暈映縮放比例</a>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -imagemap</span> </p></td> 
  <td class="stentry"> <p>啟用從暈映擷取影像地圖檔案。 對應資料會寫入只包含<span class="codeph"> &lt;map&gt;</span>專案的HTML檔案。 輸出檔案的名稱與輸出影像檔案相同，但尾碼為<span class="filepath"> .htm</span>。 如果指定命令，但暈映中沒有對應資料，則會產生警告訊息，且不會建立檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> — 設定檔</span> </p></td> 
  <td class="stentry"> <p>將內嵌於暈映中的ICC設定檔復本儲存到檔案中。 如果指定命令但暈映中沒有ICC設定檔，則會產生警告訊息，且不會建立ICC設定檔檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> — 金字塔</span> </p></td> 
  <td class="stentry"> <p>建立金字塔暈映。 當使用Dynamic Media縮放檢視器顯示演算後的影像時需要。 如需詳細資訊，請參閱<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">暈映縮放比例</a>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> — 縮圖寬度<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>縮圖影像的畫素寬度和高度限制。 如果已指定，則會從暈映檢視影像、封包樣式檔案的面板影像，或視窗遮蓋樣式檔案中第一個樣式的照明對映中產生不寬、不高於<span class="varname"> ival</span>的JPEG影像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> — 寬度<span class="varname"> ival</span> *[，<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>一或多個輸出暈映寬度（畫素）。 若指定<span class="codeph"> -info</span>，則略過。 <span class="varname"> ival</span>可以是0，代表輸入暈映的高度。 如需詳細資訊，請參閱<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local">暈映縮放比例</a>。 </p></td> 
 </tr> 
</table>
