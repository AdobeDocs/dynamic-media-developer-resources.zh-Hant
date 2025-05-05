---
description: 回應式影像庫是JavaScript模組，可動態調整Dynamic Media提供並嵌入回應式網頁的影像品質。 此外，它還可改善高密度熒幕裝置上的影像品質。 資料庫也可以回應式地呈現智慧型裁切和智慧型色票的結果。
solution: Experience Manager
title: 關於Responsive影像庫
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f853b9b4-917c-4744-b2a5-25fde2532356
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '804'
ht-degree: 0%

---

# 關於Responsive影像庫{#about-responsive-image-library}

回應式影像庫是JavaScript模組，可動態調整Dynamic Media提供並嵌入回應式網頁的影像品質。 此外，它還可改善高密度熒幕裝置上的影像品質。 資料庫也可以回應式地呈現智慧型裁切和智慧型色票的結果。

## 示範URL {#section-4f72c1dc38bf4e03acfa5205733a05a5}

Responsive影像庫最簡單的使用案例是定義影像寬度的中斷點值清單。 此清單可確保在因網頁版面配置變更而導致使用者調整瀏覽器視窗大小或變更裝置方向而調整影像大小時載入及顯示適當的轉譯。 資料庫會持續監視熒幕上的影像大小，而每當達到新的中斷點寬度時，就會從Dynamic Media擷取新的影像轉譯。

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
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html?lang=zh-Hant" scope="external" format="https"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-simple.html?lang=zh-Hant </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-simple.htm--> </p> </td> 
   <td colname="col2"> <p>以下是簡單範例，其中回應式影像位於取用網頁寬度50%的容器中。 每次調整瀏覽器視窗大小時，容器寬度都會變更。 當影像寬度達到其中一個設定的中斷點（設定為200、400、600和800畫素以用於說明用途）時，就會下載並顯示新的轉譯。 目標是避免載入不必要的大型影像，並節省網路頻寬。 </p> <p>按一下URL以開啟網頁、調整瀏覽器視窗大小及監視網路流量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>2 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html?lang=zh-Hant" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/responsive-static-image-bootstrap.html?lang=zh-Hant </a> </p> <p> 
     <!-- http://sasha.s7qa.com/jira-bugs/S7-7729/responsive-static-image-bootstrap.htm--> </p> </td> 
   <td colname="col2"> <p>以下Bootstrap範例說明網頁中的相同使用案例。 根據BootstrapCSS，要新增回應式影像的版面配置儲存格可以採用下列其中一個寬度： 360、720和940畫素。 這些值正是以中斷點形式傳遞至Responsive影像資料庫的內容。 因此，Dynamic Media可確保有效使用使用者端的網路頻寬。 此外，它也能確保影像依目前網頁版面配置以所需大小顯示，而不會因縮放使用者端瀏覽器而產生任何視覺上的不自然感。 </p> <p>按一下URL以開啟網頁、調整瀏覽器視窗大小以點選不同的配置中斷點，以及監控網路流量。 </p> <p>更進階的使用案例包括將不同的影像預設集或「影像伺服」命令（或兩者）與不同的中斷點值建立關聯。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>3 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html?lang=zh-Hant" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/image-presets.html?lang=zh-Hant</a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/image-presets.html--> </p> </td> 
   <td colname="col2"> <p>在下個範例中，會針對不同中斷點大小使用不同影像品質和格式的影像預設集。 對於小型中斷點，會套用低品質的預設集，以強制「影像伺服」將壓縮為僅六種顏色的GIF影像傳回。 中中斷點正在使用為高壓縮JPEG設定的影像預設集。 最大中斷點與使用不失真PNG的高品質影像預設集相關聯。 根據具有較大熒幕的裝置具有較大頻寬和較大處理能力的假設，這種方法可確保將高品質的影像傳送給這類裝置。 </p> <p>按一下URL以開啟網頁、將網頁瀏覽器視窗的大小從大到小調整，並注意影像品質如何降低。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>4 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html?lang=zh-Hant" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/crops.html?lang=zh-Hant </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/crops.html--> </p> </td> 
   <td colname="col2"> <p>除了影像預設集之外，您也可以將特定的「影像伺服」命令與中斷點建立關聯。 下列範例說明當熒幕影像大小變小時，如何逐步將橫幅影像裁切至感興趣區域。 在此，最大的中斷點完全沒有影像伺服命令，因此橫幅影像完全可見。 在中斷點處會套用溫和裁切，只顯示文字為「執行中」的行銷程式。 在小中斷點，會套用更多裁切，以便只顯示產品。 </p> <p>按一下URL，開啟網頁並調整瀏覽器視窗大小。 請注意影像如何從大到小逐漸裁切。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col01"> <p>5 </p> </td> 
   <td colname="col1"> <p> <a href="https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html?lang=zh-Hant" format="https" scope="external"> https://experienceleague.adobe.com/tools/dynamic-media-demo/is-api/template.html?lang=zh-Hant </a> </p> <p> 
     <!--http://sasha.s7qa.com/jira-bugs/S7-7729/template.html--> </p> </td> 
   <td colname="col2"> <p>您也可以搭配「影像伺服」範本使用「影像伺服」命令，根據影像大小控制特定範本引數。 在下個範例中，使用「影像伺服」範本，其中文字覆蓋的字型大小是使用<span class="codeph"> $fontsize </span>引數引數引數化。 回應式影像設定為對較小的影像使用較大的字型大小，以確保文字永遠保持可讀性： </p> </td> 
  </tr> 
 </tbody> 
</table>

## 系統需求 {#section-35ea9e9c79cc43d7bcefdc240340fba4}

**伺服器硬體與軟體**

* Dynamic Media Image Serving 6.0.1或更新版本。

**使用者端瀏覽器最低需求**

* Microsoft® Windows® 7或更新版本；macOS X 10.8或更新版本。
* Firefox 23、Safari 6、Chrome 29、IE 9或更新版本。
* iOS 6或更新版本。
* 通過iPhone3GS或更新版本以及iPad2或更新版本的認證（僅限原生瀏覽器）。
* Android™ OS 2.3或更新版本。
* 目前不支援行動裝置上的Internet Explorer。
