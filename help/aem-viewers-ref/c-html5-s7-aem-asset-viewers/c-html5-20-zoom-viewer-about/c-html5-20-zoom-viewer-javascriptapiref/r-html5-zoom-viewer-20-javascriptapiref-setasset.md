---
title: 設定資產
description: 視頻查看器的JavaScript API參考。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,Zoom
role: Developer,User
exl-id: 4fc94f30-e330-4c8a-b6da-d870e4f8e4ab
source-git-commit: ec2a15e2e76bae5da4fbabc9b6912b12dc080f66
workflow-type: tm+mt
source-wordcount: '135'
ht-degree: 2%

---

# 設定資產{#setasset}

視頻查看器的JavaScript API參考。

` setAsset( *`asset`*)`

<table id="table_896DFF34A68A403DB93A6D597461A573"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 資產 </span> </span> </p> </td> 
   <td colname="col2"> <p>{ 0} <span class="codeph"> 字串 </span>}新資產id、顯式影像集或顯式影像集，其中包含特定於幀的Image Service修飾符，並在「？」後附加可選全局Image Service修飾符。 </p> <p> 此查看器不支援使用IR（影像呈現）或UGC（用戶生成的內容）的影像。 </p> </td> 
  </tr> 
 </tbody> 
</table>

設定新資產。 可以在任何時間（在之前或之後）調用此參數 `init()`。 如果在 `init()`，查看器在運行時交換資產。

另請參閱 [初始化](../../../c-html5-s7-aem-asset-viewers/c-html5-20-zoom-viewer-about/c-html5-20-zoom-viewer-javascriptapiref/r-html5-zoom-viewer-20-javascriptapiref-init.md#reference-aee94dd92a28410784f7a1792e28683b)。

## 返回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

無。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

單映像引用如下：

```
 <instance>.setAsset("Scene7SharedAssets/Backpack_B")
```

對目錄中定義的影像集的單個引用如下：

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample")
```

顯式影像集如下所示：

```
<instance>.setAsset("Scene7SharedAssets/Backpack_B,Scene7SharedAssets/Backpack_C")
```

使用特定於幀的Image Service修飾符的顯式影像集如下所示：

```
 <instance>.setAsset("(Scene7SharedAssets/Backpack_B?op_colorize=255%2C0%2C0,Scene7SharedAssets/Backpack_B?op_colorize=0x00ff00)")
```

銳化修飾符添加到集中的所有影像，如下所示：

```
 <instance>.setAsset("Scene7SharedAssets/ImageSet-Views-Sample?op_sharpen=1")
```
