---
description: InfoPanelPopup.template
solution: Experience Manager
title: InfoPanelPopup.template
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog Search
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '212'
ht-degree: 3%

---


# InfoPanelPopup.template{#infopanelpopup-template}

`[InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`範本`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> 範本</span></span> </p> </td> 
   <td> <p>從資訊伺服器傳回的資料會合併到的內容範本。 </p> <p>內容模板是遵循此DTD的XML: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>內容範本的實際語法如下： </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]&gt;
      &lt;/info&gt;</code> </p> <p>也就是說，範本必須以<span class="codeph"> &lt;info&gt;</span>元素開頭，該元素可能包含可選的預設<span class="codeph"> &lt;var&gt;</span>元素。 範本內容本身<span class="codeph"> TEMPLATE_CONTENT</span>是HTML文字。 此外，內容範本可包含<span class="codeph"> $</span>字元中的變數名稱。 這些字元會以資訊伺服器傳回的變數值或預設值取代。 </p> <p>範本中定義的預設變數可以是全域變數（如果未設定變換屬性）或特定變換索引鍵（如果存在變換屬性）。 </p> <p>在範本處理期間，滾過按鍵的特定變數優先於全域變數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>請注意，當您設定「資訊面板彈出畫面」時，傳送至「資訊面板」的HTML程式碼和JavaScript程式碼會在用戶端的電腦上執行。 因此，請確定此類HTML程式碼和JavaScript程式碼是安全的。

## 屬性 {#section-6dd7785357d740d095fa9f7fd0f67da4}

選填。

## 預設 {#section-cd5db06d08aa4de49e37d6c938b41570}

無。

## 範例 {#section-16d184665c484964af9a22f79ff3f840}

假設資訊伺服器回應會以變數`$1$`傳回產品名稱，而產品影像URL會以變數`$2$`傳回。

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
