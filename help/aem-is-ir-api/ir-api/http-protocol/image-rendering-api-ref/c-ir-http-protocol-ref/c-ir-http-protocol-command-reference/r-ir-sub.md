---
description: 子選項。 允許將不同材料應用於所選對象或組的不同區域，並可移除先前應用的材料。
solution: Experience Manager
title: sub
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '162'
ht-degree: 7%

---


# sub{#sub}

子選項。 允許將不同材料應用於所選對象或組的不同區域，並可移除先前應用的材料。

`sub=0|1|2|3|4|5`

<table id="simpletable_F6BF91BD2C4B47BF8A28032E392D37F0"> 
 <tr class="strow"> 
  <td class="stentry"> <p>0 </p> </td> 
  <td class="stentry"> <p>選擇整個壁。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>1 </p> </td> 
  <td class="stentry"> <p>選擇牆的上半部。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>2 </p> </td> 
  <td class="stentry"> <p>選擇牆的下半部。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>3 </p> </td> 
  <td class="stentry"> <p>選擇頂壁邊框區域。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>4 </p> </td> 
  <td class="stentry"> <p>選擇中間壁邊框區域。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>5 </p> </td> 
  <td class="stentry"> <p>選擇底壁邊框區域。 </p> </td> 
 </tr> 
</table>

目前僅支援牆狀物件。 終止前面的MSS，並啟動要應用於指定子選擇的材料的新MSS。

為上壁或下壁指定的材料將應用於整個壁，除非另一半壁的材料也已指定。

## 屬性 {#section-b202139d6d0847cc8d520a154104ab9d}

選取命令；MSS分隔字元。

## 預設 {#section-5b45a167a17c451596e4c59b7d53c368}

`sub=0`

## 另請參閱 {#section-1a993ee24f144d4fb8baef0cc431b53b}

[obj=](../../../../../ir-api/http-protocol/image-rendering-api-ref/c-ir-http-protocol-ref/c-ir-http-protocol-command-reference/r-ir-obj.md#reference-31e7dac7931b4e0eb3c7589f120a1e6a)
