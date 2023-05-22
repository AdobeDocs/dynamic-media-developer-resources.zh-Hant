---
description: vntc生成文本資料，該文本資料被發送到stderr或日誌檔案。
solution: Experience Manager
title: 輸出
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '673'
ht-degree: 0%

---

# 輸出{#output}

vntc生成文本資料，該文本資料被發送到stderr或日誌檔案。

資料格式化為 `name=value` 每個文本記錄的屬性。 字串值不帶引號。 警告和錯誤消息始終發送到 `stderr`，即使 `-log` 。

某些屬性可在同一輸出中多次發生。 序列號（以0開頭）將附加到這些屬性的名稱中，並以句點分隔。 該等物業於下文識別， `. *`n`*` 尾碼。

將生成以下屬性：

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> 伊瓦爾</span>。<span class="varname"> 伊瓦爾</span>。<span class="varname"> 伊瓦爾</span></span> </p> </td> 
  <td class="stentry"> <p>檔案櫃樣式的RGB背景顏色。 僅限檔案櫃樣式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p>預設輸出檔案版本。 此版本的最高檔案版本號 <span class="filepath"> ntc</span> 可以生成。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">錯誤.<span class="varname"> n</span>=<span class="varname"> 字串</span></span> </p></td> 
  <td class="stentry"> <p>錯誤訊息. 出現錯誤消息通常表示未建立任何輸出檔案，或者這些檔案不適合由影像呈現使用。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">file.<span class="varname"> n</span>=<span class="varname"> 字串</span></span> </p></td> 
  <td class="stentry"> <p>所有輸出檔案（包括小圖、檔案櫃樣式檔案、全解析度影像和縮略圖）的完全限定路徑/名稱。 每個生成的檔案（日誌檔案除外）都有一個檔案屬性。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">玻璃=<span class="varname"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 伊瓦爾</span> 如果機櫃包括玻璃門，則為1，否則為0。 僅限檔案櫃樣式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">icc配置檔案=<span class="varname"> 字串</span></span> </p></td> 
  <td class="stentry"> <p>嵌入到 <span class="varname"> 源檔案</span>。 </p> <p>空，如果 <span class="varname"> 源檔案</span> 不受顏色管理。 僅限Vignettes。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=<span class="varname"> 字串</span></span> </p></td> 
  <td class="stentry"> <p>資訊性消息，如進度資訊。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 伊瓦爾</span> 如果為1 <span class="varname"> 源檔案</span> 是主視頻，如果以前處理過，則為0 <span class="filepath"> vn更新</span> 或 <span class="filepath"> ntc</span>。 僅限Vignettes。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">主=<span class="varname"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 伊瓦爾</span> 如果為0 <span class="varname"> 源檔案</span> 是包含JPEG影像資料的檔案櫃樣式（在此情況下也會輸出警告），否則為1。 僅覆蓋樣式檔案的檔案櫃和窗口。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> 字串</span></span> </p></td> 
  <td class="stentry"> <p>適用於運行的最大記憶體限制 <span class="filepath"> ntc</span> 處理。 <span class="varname"> 字串</span> 或 <span class="varname"> 伊瓦爾</span>。 <span class="varname"> 伊瓦爾克</span>。 <span class="varname"> 伊瓦爾M</span>。 <span class="varname"> 伊瓦爾</span>或 <span class="codeph"> 0</span> （已禁用）。 位置 <span class="varname"> K</span>。 <span class="varname"> M</span>, <span class="varname"> G</span> 請參閱千位元組（1024位元組）、兆位元組（1048576位元組）和千兆位元組（1073741824位元組）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p>輸出視頻中解析度最低的金字塔級的比例。 僅當 <span class="codeph">  — 金字塔</span> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">數量材料=<span class="varname"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p>保存在 <span class="varname"> 源檔案</span>。 僅限Vignettes。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p>此檔案櫃樣式檔案中的面板影像數。 僅限檔案櫃樣式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p>輸出視圖中的金字塔級數。 僅當指定了 — pyramid時才存在。 僅限Vignettes。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">金字塔=<span class="varname"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p>0（如果源視頻或目標視頻具有稜錐結構）。 僅限Vignettes。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">解析度=<span class="varname"> 谷</span></span> </p></td> 
  <td class="stentry"> <p>對於檔案櫃樣式，<span class="varname"> 源檔案</span>。 對於小圖，這是在渲染輸出視頻時為獲得最佳質量的渲染結果而建議的材料解析度。 像素/英吋(ppi)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> 谷</span></span> </p></td> 
  <td class="stentry"> <p>輸出視圖中最小的對象解析度。 僅限Vignettes。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">解析度.avg=<span class="varname"> 谷</span></span> </p></td> 
  <td class="stentry"> <p>輸出視圖中的平均對象解析度。 僅限Vignettes。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">源檔案=<span class="varname"> 字串</span></span> </p></td> 
  <td class="stentry"> <p>完全合格 <span class="varname"> 源檔案</span> 路徑。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p>檔案版本 <span class="varname"> 源檔案</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">源大小=<span class="varname"> 伊瓦爾</span>。<span class="varname"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p>輸入視頻的像素大小、檔案櫃樣式檔案中的預設面板影像或覆蓋樣式檔案的窗口的第一不透明度影像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">樣式=<span class="varname"> 字串</span></span> </p></td> 
  <td class="stentry"> <p>窗口覆蓋類型（僅覆蓋窗口樣式）: </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=水準陰影或百葉窗 </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=垂直百葉窗 </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=全寬短窗簾 </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=左/右短窗簾 </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=全寬全長窗簾 </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=左/右全長窗簾 </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=咖啡幕 </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=值 </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">尾碼=<span class="varname"> 字串</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vnt</span> 如果 <span class="varname"> 源檔案</span> 是一隻小獵犬， <span class="codeph"> VNC</span> 如果 <span class="varname"> 源檔案</span> 是檔案櫃樣式，或 <span class="codeph"> 瓦努</span> 如果 <span class="varname"> 源檔案</span> 是窗戶遮風。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p>指定的值 <span class="codeph">  — 版本</span>，或<span class="codeph"> 預設檔案版本</span> 如果<span class="codeph">  — 版本</span> 未指定。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> 伊瓦爾</span>。<span class="varname"> 伊瓦爾</span>*[,<span class="varname"> 伊瓦爾</span>。<span class="varname"> 伊瓦爾</span>]</span> </p></td> 
  <td class="stentry"> <p>以逗號分隔的清單，列出輸出視圖（金字塔形小圖的全解析度視圖）、檔案櫃樣式檔案中預設面板影像或覆蓋樣式檔案的窗口的第一個不透明度影像的所有視圖的像素大小。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">真假=<span class="varname"> 伊瓦爾</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 伊瓦爾</span> 如果機櫃樣式是可紡的，則為1；否則為0。 對於小圖和窗口覆蓋樣式檔案不存在。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">警告.<span class="varname"> n</span>=<span class="varname"> 字串</span></span> </p></td> 
  <td class="stentry"> <p>警告消息(例如 <span class="codeph">  — 影像映射</span> 已指定，但在vignette中找不到映射資料)。 </p></td> 
 </tr> 
</table>
