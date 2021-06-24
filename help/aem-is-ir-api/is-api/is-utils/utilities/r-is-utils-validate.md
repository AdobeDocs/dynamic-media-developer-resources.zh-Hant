---
description: 映像驗證實用程式。 此命令行實用程式驗證映像檔案以確保它們有效，並且映像服務可以無困難地讀取。
solution: Experience Manager
title: 驗證
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '285'
ht-degree: 1%

---

# 驗證{#validate}

映像驗證實用程式。 此命令行實用程式驗證映像檔案以確保它們有效，並且映像服務可以無困難地讀取。

所有非PTIFF影像檔案都必須通過驗證，檔案才可供「影像伺服」作為源影像使用。 複製操作可能不可靠後，應驗證PTIFF影像。

## 使用 {#usage}

` validate *``* [ *``*] [ *`fileTypeptionssourceFile`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any  </span> </p> <p>源檔案類型；必須至少指定一個（ — any允許IC支援的相同影像檔案類型）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 選項  </span> </span> </p> </td> 
  <td class="stentry"> <p>其他命令選項（請參見下面）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile  </span> </span> </p> </td> 
  <td class="stentry"> <p> 影像檔案。 無或更多，以空格分隔。 </p> </td> 
 </tr> 
</table>

## 傳回 {#section-67a7cf7c53144fbb8f24b818f4a10901}

若成功，則為0。 如果發生錯誤，則返回非零值，並將錯誤詳細資訊發送到`stderr`。

## 選項 {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList  <span class="varname"> listFile  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定包含影像檔案清單的單獨文本檔案。 每個檔案一條記錄。 如果包含<span class="codeph"> -fileList </span>，則不能指定<span class="varname"> sourceFile </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels  </span> </p> </td> 
  <td class="stentry"> <p>啟用整個影像檔案的驗證。 預設情況下，僅驗證影像標題。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile  </span> </p> </td> 
  <td class="stentry"> <p>驗證嵌入的顏色配置檔案是否有效。 預設情況下不會檢查配置檔案主體。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent  </span> </p> </td> 
  <td class="stentry"> <p> 拒絕每個影像元件16位的影像。 驗證遠程源映像時，始終由映像伺服器指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose  </span> </p> </td> 
  <td class="stentry"> <p> 如果影像無效，則打印更多資訊。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> 靜默  </span> </p> </td> 
  <td class="stentry"> <p>禁用<span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span>輸出。 僅傳回狀態。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError  </span> </p> </td> 
  <td class="stentry"> <p>在檔案驗證失敗時終止處理，即使其他檔案尚未驗證亦然。 依預設，驗證錯誤發生時，處理會繼續 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -版本 </span> </p> </td> 
  <td class="stentry"> <p>傳回此公用程式的版本資訊。 不使用其他選項指定。 </p> </td> 
 </tr> 
</table>
