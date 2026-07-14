---
description: TableOfContents.border
solution: Experience Manager
title: TableOfContents.border
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: d8b88ea2-38fe-41b8-89cb-c3603c513142
TQID: 'https://experienceleague.adobe.com/LSZTGA6CTiPoNdKYO481BFXT-ApEDcF4QOf1nsh-8fo'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 939895a2a379b02e733e48932434433bfa9663e1
workflow-type: tm+mt
source-wordcount: 164
ht-degree: 1%

---

# TableOfContents.border{#tableofcontents-bearing}

[!DNL `[TableOfContents.|<containerId>_tableOfContents.]bearing=[fit-lateral|fit-vertical][, *`autoHideDelay`*]`]

<table id="table_5151E6EA076C4AAD8D952A09E1F17C44"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"> fit-lateral|fit-vertical</span> </p> </td> 
   <td> <p> 控制下拉式面板外觀的方向。 </p> <p>設定為<span class="codeph"> fit-vertical</span>時，元件會先將基礎面板位置移至其按鈕底部，並嘗試從基礎位置向右或向左轉出面板。 在每次嘗試時，元件都會檢查面板是否被外部容器裁剪。 如果所有嘗試都失敗，元件會嘗試將基礎面板位置移至頂端，並向右和向左重複轉出嘗試。 </p> <p>當設定為<span class="codeph"> fit-lateral</span>時，元件會使用類似的邏輯，但會先將基底向右移動，然後嘗試向下和向上轉出方向。 然後，它會將基底向左移動，嘗試向下和向上轉出方向。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> autoHideDelay</span></span> </p> </td> 
   <td> <p> 設定下拉式自動隱藏計時器的延遲秒數，以在使用者閒置時隱藏面板。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 屬性 {#section-55436ddd78b04f538dbb9a7a8463feae}

選擇性.

## 預設 {#section-049d3f94c9794510906c6f81d6cc5485}

[!DNL `fit-vertical,2`]

## 範例 {#section-68ff51c4e2b740c995fc5109cc0063bd}

[!DNL `bearing=fit-vertical,0.5`]
