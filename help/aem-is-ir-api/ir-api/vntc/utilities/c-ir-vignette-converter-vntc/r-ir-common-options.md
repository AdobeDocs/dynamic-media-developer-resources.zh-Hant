---
title: 常用選項
description: 不論sourceFile的型別為何，皆可套用下列選項。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 38f3e425be0ce3e241fc18b477e3f68b7b763b51
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# 常用選項{#common-options}

不論sourceFile的型別為何，皆可套用下列選項。

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -destpath <span class="varname">字串</span> </span> </p> </td> 
  <td class="stentry"> <p>要放置輸出檔案的資料夾（如果指定<span class="codeph"> -log </span>，則包括記錄檔）。 可以是目前工作目錄的絕對路徑或相對路徑。 如果資料夾階層不存在，則會建立該資料夾階層，但不會套用至使用<span class="codeph"> -log </span>指定的檔案。 如果未指定，則會將輸出檔案寫入<span class="varname"> sourceFile </span>所在的資料夾。 若指定<span class="varname"> destFile </span>，則一律會寫入該位置，<span class="codeph"> -destpath </span>只適用於次要輸出檔案。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> — 影像</span> </p> </td> 
  <td class="stentry"> <p>如果已指定，則會從暈映、封櫃樣式的適當面板影像或視窗遮蓋樣式的第一個照明影像中擷取（第一個）檢視影像。 擷取的影像會儲存為完整解析度的TIFF檔案。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> — 資訊</span> </p> </td> 
  <td class="stentry"> <p>防止產生目標檔案。 有助於從<span class="varname"> sourceFile </span>快速擷取屬性。 只產生選用的縮圖( <span class="codeph"> -thumbwidth </span>)、影像( <span class="codeph"> -image </span>)和記錄檔( <span class="codeph"> -log </span>)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>選取有損JPEG編碼，用於內嵌在輸出檔案中的RGB和灰階影像資料，而不是無損PNG。 含Alpha (RGBA)的影像一律使用PNG編碼儲存。 <span class="varname"> ival </span>指定了JPEG品質(1...100)；建議使用85或更高。 預設值為<span class="codeph"> -jpegquality 0 </span>，會選取PNG編碼。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname">路徑</span> </span> </p> </td> 
  <td class="stentry"> <p>以指定的路徑/名稱建立記錄檔。 寫入目的地資料夾的所有輸出檔案完整路徑會寫入記錄檔，以及一些其他設定，例如版本資訊以及遇到的任何警告或錯誤（如需詳細資訊，請參閱<a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local">輸出</a>）。 如果未指定<span class="codeph"> -log </span>，則不會建立記錄檔；在此情況下，所有文字輸出都會寫入<span class="codeph"> stdout </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -lowerpriority <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>降低<span class="filepath"> vntc </span>處理序的優先順序。 使用此處理序，以便<span class="filepath"> vntc </span>在處理暈映時不會接管整個CPU。 它讓作業系統有更多時間處理其他更重要的程式。 <span class="varname"> ival </span>指定較低的優先順序百分比(0..100)。 預設值為<span class="codeph"> -lowerpriority 0 </span>，不會降低<span class="filepath"> vntc </span>處理序的優先順序。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>指定允許<span class="filepath"> vntc </span>使用的最大記憶體數量（位元組）。 當<span class="filepath"> vntc </span>達到最大記憶體限制時，它會停止處理並產生錯誤。 <span class="varname"> ival </span>指定最大記憶體限制（以位元組為單位） (0.. 3,758,096,384 (3.5 GB)。 當<span class="varname"> ival </span>為0時，會關閉記憶體上限。 預設值為<span class="codeph"> -maxmem 3221225472 </span>，這表示最大記憶體限製為3 GB。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> — 分隔符號" <span class="varname">字串</span>" </span> </p> </td> 
  <td class="stentry"> <p>指定位於檔案名稱與自動產生的輸出檔案名稱大小/解析度尾碼之間的分隔符號。 若未指定，則預設為「 — 」。 若指定<span class="varname"> destFile </span>或<span class="codeph"> -info </span>，則略過。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> — 銳利化<span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>在處理期間啟用重新取樣（縮放）影像的銳利化功能。 僅適用於封包樣式檔案中的縮圖銳利化。 </p> <p>指定0可停用銳利化（預設），指定1可啟用一般銳利化，指定2可啟用僅針對亮度進行遮色片銳利化調整，指定3可針對每個色彩元件啟用遮色片銳利化調整。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -tracelevel </span> </p> </td> 
  <td class="stentry"> <p>設定記錄層級。 預設值為1，這會輸出所有資訊、警告和錯誤訊息。 設為0可停用所有訊息，但錯誤訊息除外。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname">數量</span> <span class="varname">半徑</span> <span class="varname">閾值</span> </span> </p> </td> 
  <td class="stentry"> <p>設定遮色片銳利化調整引數。 若<span class="codeph"> — 銳利化</span>設為0或1則忽略；若<span class="codeph"> — 銳利化</span>設為2或3，則為必要。 <span class="varname">量</span>是範圍0.0...500.0內的實數值，<span class="varname">半徑</span>是範圍0.0...10.0內的實數值，而<span class="varname">臨界值</span>是從0到255的整數。 如需詳細資訊，請參閱「影像伺服通訊協定參考」中的<span class="codeph">op_usm= </span>的說明。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validateproduction <span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>驗證指定的暈映是否為適當的生產暈映。 <span class="varname"> ival </span>代表暈映的最低檔案版本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> — 版本<span class="varname"> ival </span> </span> </p> </td> 
  <td class="stentry"> <p>輸出檔案的檔案版本。 如果已指定，則必須為0或有效的暈映檔案版本（不超過預設檔案版本）。 如果設為0或未指定，則會使用最新的檔案版本建立輸出檔案。 若指定<span class="codeph"> -info </span>，則略過。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> — 版本資訊</span> </p> </td> 
  <td class="stentry"> <p>傳回此公用程式的版本資訊。 指定而不使用檔案名稱和其他選項。 </p> </td> 
 </tr> 
</table>
