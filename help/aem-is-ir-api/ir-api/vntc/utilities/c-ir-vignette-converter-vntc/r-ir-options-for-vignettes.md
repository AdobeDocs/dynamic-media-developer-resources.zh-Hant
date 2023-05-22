---
description: 以下選項控制視頻檔案的處理。 如果sourceFile不是vignette，則會忽略它們。
solution: Experience Manager
title: 小圖選項
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 7f9c2b43-9264-46a4-9519-64148aebf258
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 0%

---

# 小圖選項{#options-for-vignettes}

以下選項控制視頻檔案的處理。 如果sourceFile不是vignette，則會忽略它們。

<table id="simpletable_6D0C967EB84947FBAC34B46C4BB23AF0"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -內容</span> </p></td> 
  <td class="stentry"> <p>建立表示對象層次結構並包括選定對象屬性的XML檔案。 檔案的內容與 <span class="codeph"> req=內容</span> 的子菜單。 該檔案與源檔案同名，但 <span class="filepath"> .xml</span> 尾碼。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">作物 <span class="varname"> x</span><span class="varname"> y</span><span class="varname"> 寬</span><span class="varname"> 平</span></span> </p></td> 
  <td class="stentry"> <p>縮放前先裁切病毒。 </p> <p><span class="codeph"><span class="varname"> x</span>。<span class="varname"> y</span></span> 是裁剪矩形的上小角， <span class="codeph"><span class="varname"> 寬</span>。<span class="varname"> 平</span></span> 是裁剪矩形的大小。 值是相對於源視頻的全解析度視圖影像的像素坐標。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">-cropn <span class="varname"> x</span><span class="varname"> 英</span><span class="varname"> 維登</span><span class="varname"> 海</span></span> </p> </td> 
  <td class="stentry"> <p>縮放前先裁切病毒。 </p> <p><span class="codeph"><span class="varname"> x</span>。<span class="varname"> 英</span></span> 是裁剪矩形的上小角， <span class="codeph"><span class="varname"> 維登</span>。<span class="varname"> 海</span></span> 是裁剪矩形的大小。 值相對於源視圖的視圖影像進行規範化，且必須介於0.0...1.0之間。 </p> <p><span class="codeph"><span class="varname"> x</span></span>+<span class="codeph"><span class="varname"> 維登</span></span> 和 <span class="codeph"><span class="varname"> 英</span></span>+<span class="codeph"><span class="varname"> 海</span></span> 不得大於1.0。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">  — 嵌入材料</span> </p></td> 
  <td class="stentry"> <p>將嵌入的材料保留在輸出視圖中。 預設情況下，材料會從輸出視圖中移除。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">高度 <span class="varname"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p>一個或多個輸出視頻高度（以像素為單位）。 如果指定了 — info，則忽略。 <span class="varname"> 伊瓦爾</span> 可以是0，表示輸入視頻的寬度。 請參閱 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 維涅特縮放</a> 的上界。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">  — 影像映射</span> </p></td> 
  <td class="stentry"> <p>啟用從視頻中提取影像映射檔案。 映射資料被寫入僅包含 <span class="codeph"> &lt;map&gt;</span> 的子菜單。 輸出檔案與輸出影像檔案命名相同，但 <span class="filepath"> .htm</span> 尾碼。 如果指定了命令，但視圖中不存在映射資料，則會生成警告消息，並且不會建立檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> -設定檔</span> </p></td> 
  <td class="stentry"> <p>將嵌入到視圖中的ICC配置檔案的副本保存到檔案。 如果指定了命令，但視圖中不存在ICC配置檔案，則會生成警告消息，並且不會建立ICC配置檔案檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">  — 金字塔</span> </p></td> 
  <td class="stentry"> <p>建立金字塔視圖。 當要與Dynamic Media縮放查看器一起顯示渲染的影像時為必需。 請參閱 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 維涅特縮放</a> 的雙曲餘切值。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> — 拇指寬度 <span class="varname"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p>縮略影像的像素寬度和高度約束。 如果指定，則JPEG影像不寬且不高於 <span class="varname"> 伊瓦爾</span> 從窗口覆蓋樣式檔案中的第一樣式的視圖影像、機櫃樣式檔案的面板影像或照明映射生成。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> — 寬度 <span class="varname"> 伊瓦爾</span> *[,<span class="varname"> 伊瓦爾</span>]</span> </p></td> 
  <td class="stentry"> <p>一個或多個輸出視頻寬度（以像素為單位）。 如果忽略 <span class="codeph">  — 資訊</span> 。 <span class="varname"> 伊瓦爾</span> 可能為0，表示輸入視頻的高度。 請參閱 <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/c-ir-vignette-scaling.md#concept-e373a29c2f954df98d704c7723804585" type="concept" format="dita" scope="local"> 維涅特縮放</a> 的上界。 </p></td> 
 </tr> 
</table>
