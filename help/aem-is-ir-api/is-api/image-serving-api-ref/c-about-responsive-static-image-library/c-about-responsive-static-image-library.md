---
description: 回應式影像庫是JavaScript模組，可動態調整從Dynamic Media提供並內嵌至回應式網頁的影像品質。 此外，它在具有高密度螢幕的裝置上，提供改善的影像品質。 程式庫也可以回應性地轉換智慧型裁切和智慧型色票的結果。
solution: Experience Manager
title: 關於自適應影像庫
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '925'
ht-degree: 0%

---


# 關於自適應影像庫{#about-responsive-image-library}

回應式影像庫是JavaScript模組，可動態調整從Dynamic Media提供並內嵌至回應式網頁的影像品質。 此外，它在具有高密度螢幕的裝置上，提供改善的影像品質。 程式庫也可以回應性地轉換智慧型裁切和智慧型色票的結果。

## 示範URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

回應式影像庫最簡單的使用案例是定義影像寬度的斷點值清單。 此清單可確保在重新調整影像大小時，會載入和顯示適當的轉譯，因為網頁版面配置會隨著使用者調整瀏覽器視窗大小或變更裝置方向而改變。 程式庫會持續監控螢幕上的影像大小，而且每次達到新的斷點寬度時，都會從Dynamic Media擷取新的影像轉譯。

<table id="table_3D3D3991B802461A888E1093C1217D26"> 
 <thead> 
  <tr> 
   <th colname="col01" class="entry"> </th> 
   <th colname="col1" class="entry"> <p>示範URL </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col01"> <p>1 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html" scope="external" format="https"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-simple.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>以下是回應式影像位於網頁寬度50%的容器中的簡單範例。 每次調整瀏覽器視窗大小時，容器寬度就會變更。 當影像寬度達到設定的中斷點之一時，就會下載並顯示新的轉譯。 目的是避免載入不必要的大型影像，並節省網路頻寬。 </p> <p>按一下URL以開啟網頁、調整瀏覽器視窗大小並監控網路流量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/responsive-static-image-bootstrap.html  </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>下列Bootstrap範例說明網頁中的相同使用案例。 根據BootstrapCSS，加入回應式影像的版面儲存格可取得下列其中一種寬度：360、720和940像素。 這些值會作為中斷點傳遞至「自適應影像庫」。 因此，Dynamic Media公司確保客戶端的網路頻寬得到有效利用。 此外，它還可確保影像以所需的大小顯示，而不會因縮放用戶端瀏覽器而產生任何視覺不自然現象。 </p> <p>按一下URL以開啟網頁、調整瀏覽器視窗大小以達到不同的版面中斷點，並監控網路流量。 </p> <p>更進階的使用案例包括將不同的「影像預設集」或「影像伺服」指令（或兩者）與不同的斷點值產生關聯。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/image-presets.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>在下一個範例中，會針對不同的中斷點大小使用不同影像品質和格式的影像預設集。 對於小斷點，會套用低品質預設集，強制「影像伺服」僅傳回壓縮為6色的GIF影像。 中斷點使用為高壓縮的JPEG配置的影像預設集。 最大斷點與使用無損PNG的高質量影像預設相關聯。 這種方法基於具有較大螢幕的設備具有更大頻寬和處理能力的假設，確保將高質量影像傳送到這種設備。 </p> <p>按一下URL以開啟網頁、將網頁瀏覽器視窗從大小調整大小，並注意影像品質的降低。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/crops.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>除了「影像預設集」外，還可將特定的「影像伺服」指令與中斷點建立關聯。 下列範例說明如何隨著螢幕影像大小變小，逐漸將橫幅影像裁切至感興趣的區域。 在這裡，最大的斷點根本沒有任何「影像服務」命令，因此橫幅影像是完全可見的。 在中斷點處，會套用中度裁切，只會顯示文字為「執行中」的執行者。 在小斷點處，會套用更多裁切，以便只顯示產品。 </p> <p>按一下URL以開啟網頁並調整瀏覽器視窗大小。 請注意，隨著影像從大到小，影像會逐漸裁切。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html" format="https" scope="external"> https://marketing.adobe.com/resources/help/en_US/s7/is_ir_api/is_api/samples/template.html  </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>您也可以搭配使用影像伺服指令和影像伺服範本，根據影像大小控制特定範本參數。 在下個範例中，會使用「影像伺服範本」，其中文字覆蓋的字型大小是使用<span class="codeph"> $fontsize </span>參數進行參數化的。 回應式影像的設定是使用較大的字型大小來縮小影像大小，以確保文字永遠可讀： </p> </td> 
  </tr> 
 </tbody> 
</table>

## 系統需求 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**伺服器硬體與軟體**

* Dynamic Media影像服務6.0.1或更新版本。

**用戶端瀏覽器最低需求**

* Microsoft® Windows® 7或更新版本；Mac OS X 10.8或更新版本。
* Firefox 23、Safari 6、Chrome 29、IE 9或更新版本。
* iOS 6或更新版本。
* 已在iPhone3GS或更新版本以及iPad2或更新版本上取得認證（僅限原生瀏覽器）。
* Android OS 2.3或更新版本。
* 目前不支援行動裝置上的Internet Explorer。

