---
title: SpinView.doubleclick
description: SpinView.doubleclick
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Spin Sets
role: Developer,User
exl-id: 2e9b8f8e-aa36-4b47-a36d-7b7036e8722f
TQID: 'https://experienceleague.adobe.com/RzYRPsMpjXnUZtayjQNF52QgGU8Mz0nHm4ZDDT37d1Q'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 94
ht-degree: 3%

---

# SpinView.doubleclick{#spinview-doubleclick}

`[SpinView.|<containerId>_spinView.]doubleclick=none|zoom|reset|zoomReset`

<table id="table_E314540D347D47699C04EB80D20C0721"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> none|zoom|reset|zoomReset </span> </p> </td> 
   <td colname="col2"> <p> 設定按兩下/點選以迴轉動作的對應。 設定為<span class="codeph">無</span>會停用按兩下/點選迴轉。 如果設定為<span class="codeph">縮放</span>，請按一下影像在一個迴轉步驟中旋轉；按住Ctrl鍵並按一下滑鼠可旋轉一個迴轉步驟。 設定為<span class="codeph">重設</span>會導致在影像上按一下滑鼠，即可將迴轉重設為初始迴轉等級。 對於<span class="codeph"> zoomReset </span>，如果目前迴轉因數達到或超過指定限制，則會套用重設，否則會套用迴轉。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-924163cb2f6542499f49894becef7fb5}

選擇性.

## 預設 {#section-7a2128fd488941948aff18421f533ccf}

案頭電腦上的`reset`；觸控裝置上的`zoomReset`。

## 範例 {#section-622348a84fbe4ff4b5dd7eb53b044d83}

`doubleclick=zoom`
