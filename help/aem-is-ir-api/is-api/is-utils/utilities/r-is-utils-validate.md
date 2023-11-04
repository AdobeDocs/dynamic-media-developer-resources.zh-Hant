---
description: 影像驗證公用程式。 此命令列公用程式會驗證影像檔案，以確保它們有效，而且可由「影像伺服」輕鬆讀取。
solution: Experience Manager
title: 驗證
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 78d50fe9-95c6-4335-98d8-3322839ee02d
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '278'
ht-degree: 1%

---

# 驗證{#validate}

影像驗證公用程式。 此命令列公用程式會驗證影像檔案，以確保它們有效，而且可由「影像伺服」輕鬆讀取。

所有非PTIFF影像檔案都必須通過驗證，檔案才能供「影像伺服」作為來源影像使用。 PTIFF影像在複製操作可能不可靠後應該進行驗證。

## 使用 {#usage}

` validate *`檔案型別`* [ *`選項`*] [ *`來源檔案`* [ … ]]`

<table id="simpletable_D2C6B20E1007433AB4184A73046A44F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 檔案型別 </span> </span> </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> -jpeg | -ptif | -any </span> </p> <p>來源檔案型別；至少必須指定一種（ — any允許與IC支援的影像檔案型別相同）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 選項 </span> </span> </p> </td> 
  <td class="stentry"> <p>其他命令選項（請參閱下文）。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> <span class="varname"> 來源檔案 </span> </span> </p> </td> 
  <td class="stentry"> <p> 影像檔案。 全部或更多，以空格分隔。 </p> </td> 
 </tr> 
</table>

## 傳回 {#section-67a7cf7c53144fbb8f24b818f4a10901}

如果成功，則為0。 如果發生錯誤，則會傳回非零值並將錯誤詳細資料傳送至 `stderr`.

## 選項 {#section-9df8334b46cb4e90901505af59e4600e}

<table id="simpletable_004B1A29BDFD40A9B89E4CBD23119B3F"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -fileList <span class="varname"> listFile </span> </span> </p> </td> 
  <td class="stentry"> <p>指定包含影像檔清單的個別文字檔。 每個檔案有一筆記錄。 如果 <span class="codeph"> -fileList </span> 包含、 <span class="varname"> 來源檔案 </span> 不可指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -readPixels </span> </p> </td> 
  <td class="stentry"> <p>啟用整個影像檔案的驗證。 依預設，僅驗證影像標題。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -validatecolorprofile </span> </p> </td> 
  <td class="stentry"> <p>驗證內嵌色彩設定檔是否有效。 依預設，不會核取設定檔內文。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -reject16BitPerComponent </span> </p> </td> 
  <td class="stentry"> <p> 拒絕每個影像元件含16位元的影像。 影像伺服器驗證遠端來源影像時，一律會指定。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -verbose </span> </p> </td> 
  <td class="stentry"> <p> 如果影像無效，列印更多資訊。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -silent </span> </p> </td> 
  <td class="stentry"> <p>停用 <span class="codeph"> stdout </span>/ <span class="codeph"> stderr </span> 輸出。 僅傳回狀態。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -stopOnError </span> </p> </td> 
  <td class="stentry"> <p>當檔案驗證失敗時，即使尚未驗證其他檔案，也會終止處理。 根據預設，當發生驗證錯誤時，處理會繼續 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -版本 </span> </p> </td> 
  <td class="stentry"> <p>傳回此公用程式的版本資訊。 指定而不使用其他選項。 </p> </td> 
 </tr> 
</table>
