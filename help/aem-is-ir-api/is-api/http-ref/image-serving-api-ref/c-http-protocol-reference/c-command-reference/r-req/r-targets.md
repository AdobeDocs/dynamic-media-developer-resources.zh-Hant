---
description: 縮放影像目錄中的目標資料。 返回在URL路徑中指定的影像目錄條目的縮放目標資料。
solution: Experience Manager
title: 目標
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 58f7b1ad-8762-4d23-b320-6f69e75ecf63
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '181'
ht-degree: 2%

---

# 目標{#targets}

縮放影像目錄中的目標資料。 返回在URL路徑中指定的影像目錄條目的縮放目標資料。

`req=targets[,text|{xml[, *`編碼`*]}|{json[&id= *`reqId`*]}]`

<table id="simpletable_D64E706258FD4A9C9C8026D97B472FCC"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> 編碼</span> </span> </p> </td> 
  <td class="stentry"> <p><span class="codeph"> UTF-8 | UTF-16 | UTF-16LE | UTF-16BE | ISO-8859-1</span> </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"><span class="varname"> reqId</span></span> </p></td> 
  <td class="stentry"> <p>唯一請求標識符。 </p></td> 
 </tr> 
</table>

內容 `catalog::Targets` 的子菜單。 請求「text」格式時， `??` 在 `catalog::Targets` 替換為線終結器和單線終結器( `CR/LF`)。 如果URL路徑未解析為有效的目錄條目，則響應僅由單行終結器組成。 請求「xml」或「json」格式時應用適當的格式。

請求字串中的其他命令將被忽略。

HTTP響應可以與基於的TTL進行快取 `catalog::Expiration`。

支援JSONP響應格式的請求允許您使用擴展語法指定JS回調處理程式的名稱 `req=` 參數：

`req=...,json [&handler = reqHandler ]`

`<reqHandler>` 是JSONP響應中存在的JS處理程式的名稱。 只允許使用a-z、A-Z和0-9個字元。 選擇性. 預設為 `s7jsonResponse`.
