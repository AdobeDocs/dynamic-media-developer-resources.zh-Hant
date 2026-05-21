---
title: 縮放模式
description: 設定縮放互動的型別。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Mixed Media Sets
role: Developer,User
exl-id: a399ed5e-acc3-4c45-9c84-9fa572667489
TQID: 'https://experienceleague.adobe.com/Joa1KBx6spGvXsMkjxSCPn-23cICUffLJ9CWOQ-BRwo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 132
ht-degree: 2%

---

# 縮放模式{#zoommode}

設定縮放互動的型別。

`zoomMode=continuous|inline|auto`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">個連續|內嵌|自動</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> continuous </span>可啟用傳統縮放，當您在主檢視中按一下、點兩下或夾住時，影像會逐漸放大。 若要回到初始檢視，請縮小或重設縮放狀態。 類別 </p> <p> <span class="codeph">內嵌</span>可啟用立即縮放，當您在案頭上暫留主檢視或觸控並按住觸控裝置時，會立即顯示縮放的影像。 當您從檢視中移動滑鼠或放開手指之後，影像會自動回覆為初始狀態。 在<span class="codeph">內嵌</span>模式中，巢狀影像集會平面化並顯示為個別縮圖。 類別<span class="codeph">自動</span>會在桌上型電腦上啟用內嵌模式，並在觸控裝置上啟用連續模式。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-65be9301796240e38f31818229da7acc}

選擇性.

## 預設 {#section-bd374ffc5182484faa77a7a3c8fa70f2}

`continuous`

## 範例 {#section-bd6c4249bccf44aab13fee8552f5a8b3}

`zoomMode=auto`
