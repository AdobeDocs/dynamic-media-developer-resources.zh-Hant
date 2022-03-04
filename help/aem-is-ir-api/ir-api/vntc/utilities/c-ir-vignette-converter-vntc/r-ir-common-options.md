---
description: 無論sourceFile的類型如何，都可以應用以下選項。
solution: Experience Manager
title: 常用選項
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 1237aaf7-4585-4240-b227-c34413165dd4
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '655'
ht-degree: 0%

---

# 常用選項{#common-options}

無論sourceFile的類型如何，都可以應用以下選項。

<table id="simpletable_3BFC3737C891411D84405CEEF6B19542"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 目標路徑 <span class="varname"> 字串 </span> </span> </p> </td> 
  <td class="stentry"> <p>要放置輸出檔案的資料夾(包括日誌檔案，如果 <span class="codeph"> -log </span> 指定)。 可以是絕對路徑或相對於當前工作目錄。 如果資料夾層次結構不存在，則建立它。 不適用於指定的檔案 <span class="codeph"> -log </span>。 如果未指定，則輸出檔案將寫入其中 <span class="varname"> 源檔案 </span> 的子菜單。 如果 <span class="varname"> 目標檔案 </span> 指定，它將始終寫入到該位置 <span class="codeph">  — 目標路徑 </span> 僅應用於輔助輸出檔案。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -影像 </span> </p> </td> 
  <td class="stentry"> <p>如果指定，則從視頻中提取（第一）視圖影像、從機櫃樣式中提取合適的面板影像或窗口覆蓋樣式的第一照明影像。 提取的影像被保存為全解析度TIFF檔案。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -info </span> </p> </td> 
  <td class="stentry"> <p>防止生成目標檔案。 用於快速從 <span class="varname"> 源檔案 </span>。 僅可選縮略圖( <span class="codeph">  — 拇指寬度 </span>)，影像( <span class="codeph">  — 影像 </span>)和日誌檔案( <span class="codeph"> -log </span>)。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -jpegquality <span class="varname"> 伊瓦爾 </span> </span> </p> </td> 
  <td class="stentry"> <p>選擇有損JPEG編碼，以便RGB和灰度影像資料嵌入輸出檔案中，而不是無損PNG。 Alpha(RGBA)影像始終使用PNG編碼進行保存。 <span class="varname"> 伊瓦爾 </span> 指定JPEG質量(1...100);建議使用85或更高版本。 預設值為 <span class="codeph"> -jpegquality 0 </span>，則選擇PNG編碼。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -log <span class="varname"> 路徑 </span> </span> </p> </td> 
  <td class="stentry"> <p>建立具有指定路徑/名稱的日誌檔案寫入目標資料夾的所有輸出檔案的完整路徑將寫入日誌檔案，以及其他一些設定，如版本資訊和遇到的任何警告或錯誤（請參見） <a href="../../../../ir-api/vntc/utilities/c-ir-vignette-converter-vntc/r-ir-output.md#reference-c51e30b721eb416bb646089f0ac045c5" type="reference" format="dita" scope="local"> 輸出 </a> )。 如果 <span class="codeph"> -log </span> 未指定；在這種情況下，所有文本輸出都寫入 <span class="codeph"> 施圖 </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 低優先順序 <span class="varname"> 伊瓦爾 </span> </span> </p> </td> 
  <td class="stentry"> <p>降低 <span class="filepath"> ntc </span> 處理。 可以使用它 <span class="filepath"> ntc </span> 在處理視頻時不會接管整個CPU。 它允許作業系統為其他更重要的進程提供更多時間。 <span class="varname"> 伊瓦爾 </span> 指定較低優先順序百分比(0.100)。 預設值為 <span class="codeph">  — 低優先順序0 </span>，這不會降低 <span class="filepath"> ntc </span> 處理。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -maxmem <span class="varname"> 伊瓦爾 </span> </span> </p> </td> 
  <td class="stentry"> <p>指定最大記憶體量 <span class="filepath"> ntc </span> 允許以位元組為單位使用。 當 <span class="filepath"> ntc </span> 達到最大記憶體限制，停止處理並產生錯誤。 <span class="varname"> 伊瓦爾 </span> 指定最大記憶體限制（以位元組為單位）(0...) 3,758,096,384(3.5GB)。 當 <span class="varname"> 伊瓦爾 </span> 為0時，最大記憶體限制已關閉。 預設值為 <span class="codeph"> -maxmem 3221225472 </span>，表示最大記憶體限制為3 GB。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 分隔符" <span class="varname"> 字串 </span>" </span> </p> </td> 
  <td class="stentry"> <p>指定位於檔案名和自動生成的輸出檔案名的大小/解析度尾碼之間的分隔符。 如果未指定，則預設為「 — 」。 如果忽略 <span class="varname"> 目標檔案 </span> 或 <span class="codeph">  — 資訊 </span> 。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 銳化 <span class="varname"> 伊瓦爾 </span> </span> </p> </td> 
  <td class="stentry"> <p>允許在處理期間銳化重採樣（縮放）的影像。 僅適用於檔案櫃樣式檔案的縮略圖銳化。 </p> <p>指定0以禁用銳化（預設），指定1以啟用正常銳化，指定2以僅啟用亮度的反銳化，指定3以啟用每個顏色分量的反銳化。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 跟蹤級別 </span> </p> </td> 
  <td class="stentry"> <p>設定日誌級別。 預設值為1，它輸出所有資訊性、警告和錯誤消息。 設定為0可禁用除錯誤消息之外的所有消息。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -usm <span class="varname"> 金額 </span> <span class="varname"> 半徑 </span> <span class="varname"> 閾值 </span> </span> </p> </td> 
  <td class="stentry"> <p>設定反銳化掩碼參數。 如果忽略 <span class="codeph">  — 銳化 </span> 設定為0或1;需要 <span class="codeph">  — 銳化 </span> 設定為2或3。 <span class="varname"> 金額 </span> 是0.0...500.0範圍內的實際值， <span class="varname"> 半徑 </span> 是0.0...10.0範圍內的實際值， <span class="varname"> 閾值 </span> 是介於0和255之間的整數。 請參閱 <span class="codeph"> op_usm= </span> 的子菜單。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 驗證生產 <span class="varname"> 伊瓦爾 </span> </span> </p> </td> 
  <td class="stentry"> <p>驗證給定的視頻是正確的生產視頻。 <span class="varname"> 伊瓦爾 </span> 表示vignette的最小檔案版本。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 版本 <span class="varname"> 伊瓦爾 </span> </span> </p> </td> 
  <td class="stentry"> <p>輸出檔案的檔案版本。 如果指定，則必須為0或有效的視頻檔案版本（不大於預設檔案版本）。 如果設定為0或未指定，則使用最新檔案版本建立輸出檔案。 如果忽略 <span class="codeph">  — 資訊 </span> 。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 版本資訊 </span> </p> </td> 
  <td class="stentry"> <p>返回此實用程式的版本資訊。 指定時不使用檔案名和其他選項。 </p> </td> 
 </tr> 
</table>
