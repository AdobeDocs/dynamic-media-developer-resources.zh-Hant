---
title: 自定義全景查看器
description: 全景查看器的所有可視自定義和大多數行為自定義都通過建立自定義CSS來完成。
keywords: 響應
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

所有可視自定義和大多數行為自定義都通過建立自定義CSS來完成。

建議的工作流是為相應的查看器獲取預設CSS檔案，將其複製到其他位置，對其進行自定義，並在 `style=` 的子菜單。

預設CSS檔案可在以下位置找到：

`<s7viewers_root>/html5/PanoramicViewer.css`

自定義CSS檔案必須包含與預設類聲明相同的類聲明。 如果省略了類聲明，則查看器將無法正常工作，因為它不提供用戶介面元素的內置預設樣式。

提供自定義CSS規則的替代方法是直接在網頁或連結的外部CSS規則之一中使用嵌入樣式。

建立自定義CSS時，請記住查看器指定 `.s7panoramicviewer` 類到其容器DOM元素。 如果使用與 `style=` 命令，使用 `.s7panoramicviewer` 類作為CSS規則的後代選擇器中的父類。 如果要在網頁上執行嵌入樣式，請另外使用容器DOM元素的ID限定此選擇器，如下所示：

`#<containerId>.s7panoramicviewer.`


## 一般樣式說明和建議 {#section-95855dccbbc444e79970f1aaa3260b7b}

* CSS內到外部資產的所有路徑都根據CSS位置而不是查看器HTML頁位置進行解析。 將預設CSS複製到其他位置時，請考慮以下因素：可能需要複製預設資產或更新自定義CSS中的路徑。
* 可以對CSS支援的顏色值使用各種格式。 如果需要透明， `rgba(R,G,B,A)` 的上界。 否則，不需要透明 `#RRGGBB` 可使用。

使用CSS自定義查看器UI時，使用 `!IMPORTANT` 樣式查看器元素不支援規則。 特別是， `!IMPORTANT` 規則不應用於覆蓋查看器或查看器SDK提供的任何預設或運行時樣式，因為它可能會影響正確的元件行為。 相反，應使用具有適當特異性的CSS選擇器來設定本參考指南中記錄的CSS屬性。

## 全景查看器CSS {#section-9b6d8d601cb441d08214dada7bb4eddc}

**主查看器區域**
主視區是全景影像所佔用的區域。  它通常設定為在未指定大小時適合可用設備螢幕。

查看區域的外觀由CSS類選擇器控制：
`.s7panoramicviewer`

適用的CSS屬性包括：

<table id="table_panA68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> width </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 觀眾的寬度； </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> height </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 觀眾身高； </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

示例：設定大小為1024 x 512像素的查看器。

```
.s7panoramicviewer {
	width: 1024px;
	height: 500px;	
}
```

**全景**
主視圖由全景影像組成。

主視圖的外觀由CSS類選擇器控制：
`.s7panoramicviewer .s7panoramicview`

適用的CSS屬性包括：
<table id="table_pann68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 背景色 </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> 主視圖的背景色； </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

示例：要使主視圖透明：

```
.s7panoramicviewer .s7panoramicview {
	background-color: transparent;
}
```
