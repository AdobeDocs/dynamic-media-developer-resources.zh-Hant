---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,User
exl-id: b792cddb-f3d2-4609-95b7-105d76fb3d6f
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 1%

---

# InfoPanelPopup.template{#infopanelpopup-template}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`範本`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname">範本</span></span> </p> </td> 
   <td> <p>自資訊伺服器傳回的資料所要合併到的內容範本。 </p> <p>內容範本是此DTD之後的XML： </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;&lbrack;
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      &rbrack;&gt;</code> </p> <p>內容範本的實際語法如下： </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&gt;
      &lt;!&lbrack;CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]&gt;
      &lt;/info&gt;</code> </p> <p>也就是說，範本必須以<span class="codeph"> &lt;info&gt;</span>專案開頭，這些專案可能包含選用的預設<span class="codeph"> &lt;var&gt;</span>專案。 範本內容本身<span class="codeph"> TEMPLATE_CONTENT</span>是HTML文字。 此外，內容範本可能包含以<span class="codeph"> $</span>字元括住的變數名稱。 這些字元會取代為資訊伺服器傳回的變數值，或使用預設值。 </p> <p>範本中定義的預設變數可以是全域（如果未設定滑鼠指向效果屬性），或是特定滑鼠指向效果索引鍵的特定變數（如果有滑鼠指向效果屬性）。 </p> <p>在範本處理期間，專用於滑鼠指向鍵的變數會優先於全域變數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>請注意，當您設定資訊面板快顯視窗時，傳遞給資訊面板的HTML代碼和JavaScript代碼會在使用者端電腦上執行。 因此，請確定此類HTML程式碼和JavaScript程式碼是安全的。

## 屬性 {#section-6dd7785357d740d095fa9f7fd0f67da4}

選擇性.

## 預設 {#section-cd5db06d08aa4de49e37d6c938b41570}

無。

## 範例 {#section-16d184665c484964af9a22f79ff3f840}

假設資訊伺服器回應傳回產品名稱做為變數`$1$`，而產品影像URL則做為變數`$2$`傳回。

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
