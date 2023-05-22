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
ht-degree: 3%

---

# InfoPanelPopup.template{#infopanelpopup-template}

` [InfoPanelPopup.|<containerId>_infoPanelPopup.]template= *`範本`*`

<table id="table_A6B1B446A7AE4A4A8B552C07EC88E518"> 
 <tbody> 
  <tr> 
   <td> <p> <span class="codeph"><span class="varname"> 範本</span></span> </p> </td> 
   <td> <p>從資訊伺服器返回的資料合併到的內容模板中。 </p> <p>內容模板是遵循此DTD的XML: </p> <p> <code>&lt;!DOCTYPE&nbsp;info&nbsp;[
      &lt;!ELEMENT&nbsp;info&nbsp;(var&nbsp;#PCDATA)
      &lt;!ELEMENT&nbsp;var&nbsp;(#PCDATA)&gt;
      &lt;!ATTLIST&nbsp;var&nbsp;
      name&nbsp;CDATA&nbsp;#REQUIRED
      rollover&nbsp;CDATA&nbsp;#IMPLIED&nbsp;&gt;
      ]&gt;</code> </p> <p>內容模板的實際語法如下： </p> <p> <code>&lt;info&gt;
      &lt;var&nbsp;name='VAR_NAME'&nbsp;rollover='ROLLOVER_KEY'&gt;&lt;!CDATA[&nbsp;VAR_VALUE&nbsp;]]&gt;
      &lt;![CDATA[&nbsp;TEMPLATE_CONTENT&nbsp;]]&gt;
      &lt;/info&gt;</code> </p> <p>即，模板必須以 <span class="codeph"> &lt;info&gt;</span> 可能包含可選預設值的元素 <span class="codeph"> &lt;var&gt;</span> 元素。 模板內容本身， <span class="codeph"> 模板內容</span> 是HTML文本。 此外，內容模板可包含包含在 <span class="codeph"> $</span> 替換為資訊伺服器返回的變數值或預設值的字元。 </p> <p>在模板中定義的預設變數可以是全局變數（如果未設定滾動更新屬性），也可以是特定於某個滾動更新鍵（如果存在滾動更新屬性）。 </p> <p>在模板處理過程中，特定於滾動項的變數優先於全局變數。 </p> </td> 
  </tr> 
 </tbody> 
</table>

>[!NOTE]
>
>配置「資訊面板」彈出菜單時，傳遞給「資訊面板」的HTML代碼和JavaScript代碼將在客戶端電腦上運行。 因此，請確保此類HTML代碼和JavaScript代碼是安全的。

## 屬性 {#section-6dd7785357d740d095fa9f7fd0f67da4}

選擇性.

## 預設 {#section-cd5db06d08aa4de49e37d6c938b41570}

無。

## 範例 {#section-16d184665c484964af9a22f79ff3f840}

假定資訊伺服器響應將產品名稱返回為變數 `$1$` 並且產品影像URL作為變數返回 `$2$`。

`template=<info><![CDATA[Product description:$1$<br>Product image:<img src="$2$">]]></info>`
