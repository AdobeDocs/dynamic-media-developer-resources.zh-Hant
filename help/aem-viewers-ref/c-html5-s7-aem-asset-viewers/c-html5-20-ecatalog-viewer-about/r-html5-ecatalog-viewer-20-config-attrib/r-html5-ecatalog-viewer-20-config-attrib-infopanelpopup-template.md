---
title: InfoPanelPopup.template
description: InfoPanelPopup.template
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 20618017-2f73-4951-baa9-2063a0f4efcb
source-git-commit: a919130f0940d81a221b79563b6b3e41533ba788
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 2%

---

# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`範本`*`

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
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]&rbrack;&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>也就是說，範本必須以<span class="codeph"> &lt;info&gt;</span>專案開頭，這些專案可能包含選用的預設<span class="codeph"> &lt;var&gt;</span>專案。 範本內容本身<span class="codeph"> TEMPLATE_CONTENT</span>是HTML文字。 此外，內容範本可能包含以<span class="codeph"> $</span>字元括住的變數名稱，這些變數名稱會由資訊伺服器傳回的變數值或預設值取代。 </p> <p>範本中定義的預設變數可以是全域（如果未設定滑鼠指向效果屬性），或是特定滑鼠指向效果索引鍵的特定變數（如果有滑鼠指向效果屬性）。 </p> <p>在範本處理期間，專用於滑鼠指向鍵的變數會優先於全域變數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>當您設定資訊面板快顯視窗時，傳遞給資訊面板的HTML代碼和JavaScript代碼會在使用者端電腦上執行。 因此，請確定此類HTML程式碼和JavaScript程式碼是安全的。

## 屬性 {#section-6dd7785357d740d095fa9f7fd0f67da4}

選擇性.

## 預設 {#section-cd5db06d08aa4de49e37d6c938b41570}

無。

## 範例 {#section-16d184665c484964af9a22f79ff3f840}

假設資訊伺服器回應傳回產品名稱做為變數`$1$`，而產品影像URL則做為變數`$2$`傳回。

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
