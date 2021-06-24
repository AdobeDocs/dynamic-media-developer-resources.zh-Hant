---
description: 無論sourceFile的類型為何，都可應用以下選項。
solution: Experience Manager
title: 常見選項
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '661'
ht-degree: 0%

---

# 常見選項{#common-options}

無論sourceFile的類型為何，都可應用以下選項。

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath字 <span class="varname"> 串  </span> </span> </p> </td> 
  <td class="stentry"> <p>要放置輸出檔案的資料夾（如果指定<span class="codeph"> -log </span>，則包括日誌檔案）。 可以是絕對路徑，也可以是相對於當前工作目錄。 如果資料夾階層不存在，則會建立該資料夾階層。 不適用於以<span class="codeph"> -log </span>指定的檔案。 如果未指定，則將輸出檔案寫入<span class="varname"> sourceFile </span>所在的資料夾。 如果指定了<span class="varname"> destFile </span>，則始終會將其寫入該位置，並且<span class="codeph"> -destpath </span>僅適用於次輸出檔案。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -影像 </span> </p> </td> 
  <td class="stentry"> <p>如果指定，則從暈映中提取（第一）視圖影像、從櫃式樣式中提取合適的面板影像或窗口覆蓋樣式的第一照明影像。 擷取的影像會儲存為全解析度TIFF檔案。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>防止生成目標檔案。 用於從<span class="varname"> sourceFile </span>快速提取屬性。 僅生成可選縮略圖(<span class="codeph"> -thumbwidth </span>)、影像(<span class="codeph"> -image </span>)和日誌檔案(<span class="codeph"> -log </span>)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>為嵌入在輸出檔案中的RGB和灰度影像資料選擇有損JPEG編碼，而不是無損PNG。 含有Alpha(RGBA)的影像一律會使用PNG編碼來儲存。 <span class="varname"> ival </span> 指定JPEG質量(1...100);建議85個或更高版本。預設值為<span class="codeph"> -jpegquality 0 </span>，可選擇PNG編碼。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 日誌路 <span class="varname"> 徑  </span> </span> </p> </td> 
  <td class="stentry"> <p>使用指定的路徑/名稱建立日誌檔案寫入目標資料夾的所有輸出檔案的完整路徑寫入日誌檔案，以及一些其他設定，如版本資訊和遇到的任何警告或錯誤（有關詳細資訊，請參閱<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local">輸出</a>）。 如果未指定<span class="codeph"> -log </span> ，則不會建立日誌檔案；在這種情況下，所有文本輸出都寫入<span class="codeph"> stdout </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 低優先順 <span class="varname"> 序ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>降低<span class="filepath"> vntc </span>進程的優先順序。 這可以使<span class="filepath"> vntc </span>在處理暈映時不會接管整個CPU。 它允許作業系統給其他更重要的流程更多時間。 <span class="varname"> ival </span> 指定優先順序百分比較低(0.100)。預設值為<span class="codeph"> -lowerpriority 0 </span>，它不會降低<span class="filepath"> vntc </span>進程的優先順序。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定允許<span class="filepath"> vntc </span>以位元組為單位使用的最大記憶體量。 當<span class="filepath"> vntc </span>達到最大記憶體限制時，它停止處理並產生錯誤。 <span class="varname"> ival </span> 指定最大記憶體限制（以位元組為單位）(0..3,758,096,384(3.5GB)。 當<span class="varname"> ival </span>為0時，最大記憶體限制將關閉。 預設值為<span class="codeph"> -maxmem 3221225472 </span>，這意味著最大記憶體限制為3 GB。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 分隔符" <span class="varname"> 字串 </span>"  </span> </p> </td> 
  <td class="stentry"> <p>指定檔案名和大小/解析度尾碼之間的分隔符，用於自動生成輸出檔案名。 若未指定，則預設為「 — 」。 如果指定<span class="varname"> destFile </span>或<span class="codeph"> -info </span>，則忽略。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 銳化 <span class="varname"> 間隔  </span> </span> </p> </td> 
  <td class="stentry"> <p>可在處理期間銳利化影像重新取樣（縮放）。 僅適用於檔案櫃樣式檔案的縮圖銳利化。 </p> <p>指定0以禁用銳利化（預設值），指定1以啟用正常銳利化，指定2以僅啟用亮度的非銳利化遮色片，或指定3以為每個顏色元件啟用非銳利化遮色片。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel  </span> </p> </td> 
  <td class="stentry"> <p>設定記錄層級。 預設值為1，會輸出所有資訊、警告和錯誤訊息。 設為0可停用除錯誤訊息外的所有訊息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> 量半 </span> <span class="varname"> 徑閾 </span> <span class="varname"> 值  </span> </span> </p> </td> 
  <td class="stentry"> <p>設定非銳利化遮色片參數。 如果將<span class="codeph"> -sharpen </span>設定為0或1，則忽略；如果<span class="codeph"> -sharpen </span>設為2或3，則此為必填項。 <span class="varname">  </span> amount是0.0..500.0範圍內的實數值，radius <span class="varname">  </span> 是0.0..10.0範圍內的實數值，閾值是0 <span class="varname">  </span> 到255之間的整數。如需詳細資訊，請參閱影像伺服通訊協定參考中<span class="codeph"> op_usm= </span>的說明。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>驗證指定的暈映是否為正確的生產暈映。 <span class="varname"> ival </span> 表示暈映的最低檔案版本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 版本 <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>輸出檔案的檔案版本。 如果指定，則必須為0或有效的暈映檔案版本（不大於預設檔案版本）。 如果設定為0或未指定，則使用最新的檔案版本建立輸出檔案。 如果指定<span class="codeph"> -info </span>，則忽略。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo  </span> </p> </td> 
  <td class="stentry"> <p>返回此實用程式的版本資訊。 不指定檔案名和其他選項。 </p> </td> 
 </tr> 
</table>
