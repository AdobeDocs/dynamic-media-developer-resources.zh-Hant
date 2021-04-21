---
description: 映像驗證實用程式。 此命令行實用程式會驗證映像檔案，以確保它們有效，並且通過映像服務可以無困難地讀取。
solution: Experience Manager
title: 驗證
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '288'
ht-degree: 1%

---


# 驗證{#validate}

映像驗證實用程式。 此命令行實用程式會驗證映像檔案，以確保它們有效，並且通過映像服務可以無困難地讀取。

所有非PTIFF影像檔案必須先通過驗證，才能將檔案提供給「影像伺服」做為來源影像。 PTIFF影像應在可能不可靠的復製作業後進行驗證。

## 使用 {#usage}

` validate *`檔`* [ *``*] [ *`案類型來源檔案`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> fileType  </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any  </span> </p> <p>源檔案類型；至少必須指定一個（-any允許IC支援的相同影像檔案類型）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 選項  </span> </span> </p> </td> 
  <td class="stentry"> <p>其他命令選項（請參見下面）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> sourceFile  </span> </span> </p> </td> 
  <td class="stentry"> <p> 影像檔。 無或更多，以空格分隔。 </p> </td> 
 </tr> 
</table>

## 傳回{#section-67a7cf7c53144fbb8f24b818f4a10901}

0（如果成功）。 如果發生錯誤，則會傳回非零值，並將錯誤詳細資料傳送至`stderr`。

## 選項 {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList  <span class="varname"> listFile  </span> </span> </p> </td> 
  <td class="stentry"> <p>指定包含影像檔案清單的單獨文本檔案。 每個檔案一條記錄。 如果包含<span class="codeph"> -fileList </span>，則不能指定<span class="varname"> sourceFile </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels  </span> </p> </td> 
  <td class="stentry"> <p>啟用整個映像檔案的驗證。 依預設，只會驗證影像標題。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile  </span> </p> </td> 
  <td class="stentry"> <p>驗證嵌入的色彩描述檔是否有效。 預設情況下，不選中截面梁主體。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent  </span> </p> </td> 
  <td class="stentry"> <p> 拒絕每個影像元件16位元的影像。 驗證遠程源映像時，始終由映像伺服器指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose  </span> </p> </td> 
  <td class="stentry"> <p> 如果影像無效，則列印更多資訊。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent  </span> </p> </td> 
  <td class="stentry"> <p>禁用<span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span>輸出。 只會傳回狀態。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError  </span> </p> </td> 
  <td class="stentry"> <p>在發生檔案驗證失敗時終止處理，即使其他檔案尚未驗證亦然。 依預設，當發生驗證錯誤時，處理會繼續進行 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -版本 </span> </p> </td> 
  <td class="stentry"> <p>返回此實用程式的版本資訊。 不使用其他選項指定。 </p> </td> 
 </tr> 
</table>

