---
title: 自訂全景檢視器
description: 全景檢視器的所有視覺化自訂和大部分行為自訂都是透過建立自訂CSS完成的。
keywords: 回應式
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Panoramic
role: Developer,User
exl-id: c9dda4e8-2781-4870-9ccb-707823c56490
source-git-commit: 7a3ba1cbe063603733a8ff03e8ef1277ec632ec5
workflow-type: tm+mt
source-wordcount: '466'
ht-degree: 0%

---

# 自訂Video360檢視器{#customizing-video-viewer}

所有視覺化自訂和大多數行為自訂都是透過建立自訂CSS完成的。

建議的工作流程是取得適當檢視器的預設CSS檔案、將其複製到其他位置、自訂該檔案，並在`style=`命令中指定自訂檔案的位置。

可以在以下位置找到預設的CSS檔案：

`<s7viewers_root>/html5/PanoramicViewer.css`

自訂CSS檔案必須包含與預設檔案相同的類別宣告。 如果省略類別宣告，則檢視器無法正常運作，因為它沒有為使用者介面元素提供內建的預設樣式。

提供自訂CSS規則的替代方式是直接在網頁上或其中一個連結的外部CSS規則中使用內嵌樣式。

建立自訂CSS時，請記得檢視器將`.s7panoramicviewer`類別指派給其容器DOM元素。 如果您使用透過`style=`命令傳遞的外部CSS檔案，請在CSS規則的子系選取器中使用`.s7panoramicviewer`類別作為父類別。 如果您在網頁上執行內嵌樣式，請另外使用容器DOM元素的ID來限定此選取器，如下所示：

`#<containerId>.s7panoramicviewer.`


## 一般樣式注意事項和建議 {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS內指向外部資產的所有路徑都是根據CSS位置而不是檢視器HTML頁面位置來解析。 將預設CSS複製到不同位置時，請考量這一點：您可能需要同時複製預設資產或更新自訂CSS內的路徑。
* CSS支援的色彩值可使用多種格式。 如果需要透明度，建議使用`rgba(R,G,B,A)`格式。 否則，不需要透明度`#RRGGBB`可以使用。

使用CSS自訂檢視器UI時，樣式檢視器元素不支援使用`!IMPORTANT`規則。 尤其是`!IMPORTANT`規則不應用來覆寫檢視器或檢視器SDK提供的任何預設或執行階段樣式，因為它可能會影響正確的元件行為。 相反地，應使用具有適當特性的CSS選取器來設定本參考指南中記錄的CSS屬性。

## 全景檢視器CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

**主要檢視器區域**
主檢視區域是全景影像所佔用的區域。  若未指定大小，通常會設定以符合可用的裝置熒幕。

檢視區域的外觀可透過CSS類別選取器來控制：
`.s7panoramicviewer`

適用的CSS屬性包括：

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">寬度</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">檢視器的寬度；</span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">高度</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">檢視器的高度；</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：
若要設定大小為1024 x 512畫素的檢視器。

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**全景檢視**
主檢視由全景影像組成。

主檢視的外觀可透過CSS類別選取器來控制：
`.s7panoramicviewer .s7panoramicview`

適用的CSS屬性包括：
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">背景色彩</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph">主要檢視的背景色彩；</span> </p> </td> 
  </tr> 
 </tbody> 
</table>

範例：
若要讓主檢視透明：

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
