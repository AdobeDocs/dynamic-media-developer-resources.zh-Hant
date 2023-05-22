---
description: 映像驗證實用程式。 此命令行實用程式將驗證映像檔案，以確保它們有效，並且映像服務可以無困難地讀取。
solution: Experience Manager
title: 驗證
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 1%

---

# 驗證{#validate}

映像驗證實用程式。 此命令行實用程式將驗證映像檔案，以確保它們有效，並且映像服務可以無困難地讀取。

所有非PTIFF影像檔案必須通過驗證，才能將該檔案作為源影像供影像服務使用。 在可能不可靠的複製操作之後，應驗證PTIFF影像。

## 使用 {#usage}

` validate *`檔案類型`* [ *`選項`*] [ *`源檔案`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 檔案類型 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg |-ptif | -any </span> </p> <p>源檔案類型；必須至少指定一個（ — any允許IC支援的相同映像檔案類型）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 選項 </span> </span> </p> </td> 
  <td class="stentry"> <p>其他命令選項（請參閱下文）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 源檔案 </span> </span> </p> </td> 
  <td class="stentry"> <p> 影像檔案。 無或更多，以空格分隔。 </p> </td> 
 </tr> 
</table>

## 返回 {#section-67a7cf7c53144fbb8f24b818f4a10901}

0（如果成功）。 如果發生錯誤，則返回非零值，並將錯誤詳細資訊發送到 `stderr`。

## 選項 {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> 清單檔案 </span> </span> </p> </td> 
  <td class="stentry"> <p>指定包含影像檔案清單的單獨文本檔案。 每個檔案一條記錄。 如果 <span class="codeph"> -fileList </span> 包含， <span class="varname"> 源檔案 </span> 不能指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>啟用整個映像檔案的驗證。 預設情況下，僅驗證影像標頭。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>驗證嵌入的顏色配置檔案是否有效。 預設情況下，不檢查配置檔案主體。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> 拒絕每個影像元件16位的影像。 在驗證遠程源映像時始終由映像伺服器指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph">  — 詳細 </span> </p> </td> 
  <td class="stentry"> <p> 如果影像無效，則打印詳細資訊。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 靜默 </span> </p> </td> 
  <td class="stentry"> <p>禁用 <span class="codeph"> 施圖 </span>/ <span class="codeph"> 施特 </span> 。 只返回狀態。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>在檔案驗證失敗時終止處理，即使其他檔案尚未驗證。 預設情況下，在出現驗證錯誤時繼續處理 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -版本 </span> </p> </td> 
  <td class="stentry"> <p>返回此實用程式的版本資訊。 不使用其他選項指定。 </p> </td> 
 </tr> 
</table>
