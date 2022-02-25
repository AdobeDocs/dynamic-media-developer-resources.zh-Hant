---
title: 設定資產
description: 用於基本縮放查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 71525aac-b8ca-4f5a-a770-268857ddae4f
source-git-commit: 7eddc50fb9803eacdd1f513c6132380793b6f88d
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 3%

---

# 設定資產{#setasset}

用於基本縮放查看器的JavaScript API參考。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資產</span> </span> </p> </td> 
   <td colname="col2"> <p>{ 0}<span class="codeph"> 字串</span>}新資產id，在「？」後附加可選IS修飾符 </p> <p> 此查看器不支援使用IR（影像呈現）或UGC（用戶生成的內容）的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定新資產。 可以在任何時間（在之前或之後）調用此參數 `init()`。 如果在 `init()`，查看器在運行時交換資產。

另請參閱 [初始化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-basic-zoom-viewer-about/c-html5-20-basic-zoom-viewer-javascriptapiref/r-html5-basic-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

單個影像引用：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

銳化修飾符添加到集中的所有影像：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B?op_sharpen=1")
```
