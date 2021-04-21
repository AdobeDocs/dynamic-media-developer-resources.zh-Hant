---
description: 無論sourceFile的類型如何，都可以應用以下選項。
solution: Experience Manager
title: 常用選項
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '664'
ht-degree: 0%

---


# 常用選項{#common-options}

無論sourceFile的類型如何，都可以應用以下選項。

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath字 <span class="varname"> 符串  </span> </span> </p> </td> 
  <td class="stentry"> <p>要放置輸出檔案的資料夾（如果指定了<span class="codeph"> -log </span> ，則包括日誌檔案）。 可以是絕對路徑或相對於當前工作目錄。 如果資料夾層次不存在，將建立該資料夾層次。 不適用於使用<span class="codeph"> -log </span>指定的檔案。 如果未指定，則輸出檔案將寫入<span class="varname"> sourceFile </span>所在的資料夾。 如果指定<span class="varname"> destFile </span>，則始終會將其寫入到該位置，並且<span class="codeph"> -destpath </span>僅適用於次輸出檔案。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -影像 </span> </p> </td> 
  <td class="stentry"> <p>如果指定，則從暈映中提取（第一）視圖影像、從機櫃樣式中提取合適的面板影像或窗口覆蓋樣式的第一照明影像。 提取的影像會儲存為完整解析度的TIFF檔案。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>防止產生目標檔案。 從<span class="varname"> sourceFile </span>快速擷取屬性非常有用。 僅生成可選縮圖(<span class="codeph"> -thumbwidth </span>)、影像(<span class="codeph"> -image </span>)和日誌檔案(<span class="codeph"> -log </span>)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>針對內嵌在輸出檔案中的RGB和灰階影像資料選取有損JPEG編碼，而非無損PNG。 使用alpha(RGBA)的影像一律會使用PNG編碼來儲存。 <span class="varname"> ival </span> 指定JPEG品質(1...100);建議使用85或以上版本。預設值為<span class="codeph"> -jpegquality 0 </span>，可選擇PNG編碼。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log路 <span class="varname"> 徑  </span> </span> </p> </td> 
  <td class="stentry"> <p>建立具有指定路徑／名稱的日誌檔案寫入目標資料夾的所有輸出檔案的完整路徑都寫入日誌檔案，以及某些其他設定，如版本資訊和出現的任何警告或錯誤（有關詳細資訊，請參閱<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local">輸出</a>）。 如果未指定<span class="codeph"> -log </span>，則不建立日誌檔案；在這種情況下，所有文本輸出都寫入<span class="codeph"> stdout </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -低優先順序 <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>降低<span class="filepath"> vntc </span>進程的優先順序。 這可以使<span class="filepath"> vntc </span>在處理暈映時不佔用整個CPU。 它可讓作業系統為其他更重要的程式提供更多時間。 <span class="varname"> ival指 </span> 定較低的優先順序百分比(0..100)。預設值為<span class="codeph"> -lowerpriority 0 </span> ，它不會降低<span class="filepath"> vntc </span>進程的優先順序。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定<span class="filepath"> vntc </span>允許以位元組為單位使用的最大記憶體量。 當<span class="filepath"> vntc </span>達到最大記憶體限制時，它會停止處理並產生錯誤。 <span class="varname"> ival指 </span> 定最大記憶體限制（以位元組為單位）(0...)。3,758,096,384(3.5GB)。 當<span class="varname"> ival </span>為0時，最大記憶體限制將關閉。 預設值為<span class="codeph"> -maxmem 322125472 </span> ，表示最大記憶體限制為3 GB。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -separator "字 <span class="varname"> 符串 </span>"  </span> </p> </td> 
  <td class="stentry"> <p>為自動生成的輸出檔案名指定檔案名和大小／解析度尾碼之間的分隔符。 如果未指定，則預設為"-"。 如果指定<span class="varname"> destFile </span>或<span class="codeph"> -info </span>，則忽略。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -銳利 <span class="varname"> 化  </span> </span> </p> </td> 
  <td class="stentry"> <p>可在處理期間銳利化重新取樣（縮放）的影像。 僅適用於檔案櫃樣式檔案的縮圖銳化。 </p> <p>指定0可停用銳利化（預設值）、1可啟用一般銳利化、2可僅啟用亮度的銳利化遮色片，或3可啟用每個色彩元件的銳利化遮色片。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel  </span> </p> </td> 
  <td class="stentry"> <p>設定日誌級別。 預設值為1，會輸出所有資訊性、警告和錯誤訊息。 設定為0可禁用除錯誤消息之外的所有消息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> 量半 </span> <span class="varname"> 徑閾 </span> <span class="varname"> 值  </span> </span> </p> </td> 
  <td class="stentry"> <p>設定遮色片銳利化參數。 如果<span class="codeph"> -sharpen </span>設定為0或1，則忽略；<span class="codeph"> -sharpen </span>設為2或3時為必要項。 <span class="varname"> amount </span> 是0.0...500.0範圍內的實數值， <span class="varname">  </span> 半徑是0.0...10.0範圍內的實數值， <span class="varname"> 閾 </span> 值是0到255之間的整數。如需詳細資訊，請參閱影像伺服通訊協定參考中的<span class="codeph"> op_usm= </span>說明。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>驗證指定的暈映是否為正確的生產暈映。 <span class="varname"> ival代 </span> 表暈映的最小檔案版本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -version  <span class="varname"> ival  </span> </span> </p> </td> 
  <td class="stentry"> <p>輸出檔案的檔案版本。 如果指定，則必須為0或有效的暈映檔案版本（不大於預設檔案版本）。 如果設定為0或未指定，則使用最新檔案版本建立輸出檔案。 如果指定<span class="codeph"> -info </span>，則忽略。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -versioninfo  </span> </p> </td> 
  <td class="stentry"> <p>返回此實用程式的版本資訊。 不使用檔案名稱和其他選項指定。 </p> </td> 
 </tr> 
</table>

