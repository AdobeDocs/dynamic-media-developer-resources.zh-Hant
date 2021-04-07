---
description: 所有檢視器通用的參數。
solution: Experience Manager
title: config
feature: Dynamic Media經典，檢視器，SDK/API
role: 開發人員，商業從業人員
exl-id: 503a1fc6-7a6b-4f55-bad1-11f22435276f
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '261'
ht-degree: 2%

---

# config{#config}

所有檢視器通用的參數。

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId  </span> </span> </p> </td> 
   <td colname="col2"> <p>檢視器設定的目錄/ID。 </p> <p> 指定包含<span class="codeph">目錄：:UserData </span>中的查看器配置屬性的映像目錄條目。 當此命令出現時，檢視器會傳送<span class="codeph"> configId </span>的<span class="codeph"> req=userdata </span>命令至伺服器，並從回覆擷取屬性。 屬性用於初始化檢視器。 如果URL字串指定相同的屬性，則會覆寫<span class="codeph">目錄：:UserData </span>中的值。 </p> </td> 
  </tr> 
 </tbody> 
</table>

所有可在`catalog::UserData`中指定的查看器命令都期望`asset`、`serverUrl`、`contentUrl`、`searchServerUrl`和`config`本身。

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選填。

## 預設 {#section-d411e450028c460392cb8508f8ccc5d9}

無。

## 範例1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

名為2020的映像目錄包含`preset-oct`條目。 此目錄條目的`catalog::UserData`欄位包含以下資料：

```
style=customStyle.css
```

使用下列命令載入檢視器：

```
config=2020/preset-oct
```

這等同於URL中明確指定的下列命令：

```
style=customStyle.css
```

## 範例2 {#section-577fce5ddbee43fc96d88b2055df47aa}

名為2019的影像目錄包含`spin-oct`項目。 此目錄條目的`catalog::UserData`欄位包含以下資料：

```
zoomStep=3 
maxZoom=200
```

使用下列命令載入檢視器：

```
config=2019/spin-oct
```

這等同於URL中明確指定的下列命令：

```
zoomStep=3&maxZoom=200
```

## 範例3 {#section-2b3a42c3926e4eb19fa14434def9195f}

名為`Shoppable_Banner`的檢視器預設集包含下列資料：

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

使用下列命令載入檢視器：

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

這等同於URL中明確指定的下列命令：

`style=etc/dam/presets/css/html5_interactiveimage.css`

## 範例4 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

名為`Shoppable_Video_Dark`的檢視器預設集包含下列資料：

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

使用下列命令載入檢視器：

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

這等同於URL中明確指定的下列命令：

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## 範例5 {#section-19b988551d1d492a9079948e0b04b38f}

名為`Carousel_Dotted_light`的檢視器預設集：

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

使用下列命令載入檢視器：

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

這等同於URL中明確指定的下列命令：

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```
