---
title: 自訂全景檢視器
description: 全景檢視器的所有視覺化自訂和大部分的行為自訂，都是透過建立自訂CSS來完成。
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 0%

---

# 自定義Video360查看器{#customizing-video-viewer}

所有視覺化自訂和大部分的行為自訂都是透過建立自訂CSS來完成。

建議的工作流程是為適當的檢視器取用預設的CSS檔案、將其複製至不同位置、自訂，以及在 `style=` 命令。

您可以在下列位置找到預設的CSS檔案：

`<s7viewers_root>/html5/PanoramicViewer.css`

自訂CSS檔案必須包含與預設檔案相同的類聲明。 如果省略類聲明，則查看器無法正常工作，因為它不提供用戶介面元素的內置預設樣式。

提供自訂CSS規則的替代方式，是直接在網頁或其中一個連結的外部CSS規則中使用內嵌樣式。

建立自訂CSS時，請記住檢視器指派 `.s7panoramicviewer` 類別至其容器DOM元素。 如果您使用的是外部CSS檔案，則會與 `style=` 命令，使用 `.s7panoramicviewer` 類別作為CSS規則的子體選取器中的上層類別。 如果您要在網頁上執行內嵌樣式，請額外以容器DOM元素的ID限定此選取器，如下所示：

`#<containerId>.s7panoramicviewer.`


## 一般樣式附註與建議 {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS內所有外部資產的路徑都會根據CSS位置而非檢視器HTML頁面位置進行解析。 將預設CSS複製到不同位置時，請考量下列事項：您也可能需要複製預設資產或更新自訂CSS內的路徑。
* CSS支援的顏色值可以使用各種格式。 如果需要透明， `rgba(R,G,B,A)` 格式。 否則，不需要透明度 `#RRGGBB` 可供使用。

使用CSS自訂檢視器UI時，請使用 `!IMPORTANT` 樣式檢視器元素不支援規則。 特別是， `!IMPORTANT` 規則不應用來覆寫檢視器或檢視器SDK所提供的任何預設或執行階段樣式，因為它可能會影響正確的元件行為。 相反地，應使用具有適當特性的CSS選取器來設定本參考指南中記錄的CSS屬性。

## 全景檢視器CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

**主觀看者區域**
主視圖區域是全景影像所佔用的區域。  通常在未指定大小時設定為適合可用的裝置畫面。

檢視區域的外觀由CSS類別選取器控制：
`.s7panoramicviewer`

適用的CSS屬性包括：

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 檢視器的寬度； </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 觀看者的高度； </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：設定大小為1024 x 512像素的檢視器。

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**全景視圖**
主視圖由全景影像組成。

主檢視的外觀由CSS類別選取器控制：
`.s7panoramicviewer .s7panoramicview`

適用的CSS屬性包括：
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景顏色 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 主視圖的背景顏色； </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：要使主視圖透明：

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
