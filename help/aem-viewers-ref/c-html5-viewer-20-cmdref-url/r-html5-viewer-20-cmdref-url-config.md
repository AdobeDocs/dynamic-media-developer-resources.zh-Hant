---
title: config
description: 所有查看器通用的參數。
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API
role: Developer,User
exl-id: 503a1fc6-7a6b-4f55-bad1-11f22435276f
source-git-commit: c99aac44711852d8ac661878e11ce0b19d3dbf60
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 2%

---

# config{#config}

所有查看器通用的參數。

` config= *`配置ID`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> 配置ID </span> </span> </p> </td> 
   <td colname="col2"> <p>查看器配置的目錄/ID。 </p> <p> 指定包含中的查看器配置屬性的影像目錄條目 <span class="codeph"> 目錄：:UserData </span>。 當此命令存在時，查看器將發送 <span class="codeph"> req=userdata </span> 命令 <span class="codeph"> 配置ID </span> 從回復中提取屬性。 屬性用於初始化查看器。 如果URL字串指定相同的屬性，則它們將覆蓋 <span class="codeph"> 目錄：:UserData </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

可在中指定的所有查看器命令 `catalog::UserData` 預期 `asset`。 `serverUrl`。 `contentUrl`。 `searchServerUrl`, `config` 本身。

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選擇性.

## 預設 {#section-d411e450028c460392cb8508f8ccc5d9}

無。

## 範例 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

名為2020的影像目錄包含該條目 `preset-oct`。 的 `catalog::UserData` 此目錄條目的欄位包含以下資料：

```
style=customStyle.css
```

使用以下命令載入查看器：

```
config=2020/preset-oct
```

此示例等效於在URL中顯式指定的以下命令：

```
style=customStyle.css
```

## 示例2 {#section-577fce5ddbee43fc96d88b2055df47aa}

名為2019的影像目錄包含該條目 `spin-oct`。 的 `catalog::UserData` 此目錄條目的欄位包含以下資料：

```
zoomStep=3 
maxZoom=200
```

使用以下命令載入查看器：

```
config=2019/spin-oct
```

此示例等效於在URL中顯式指定的以下命令：

```
zoomStep=3&maxZoom=200
```

## 示例3 {#section-2b3a42c3926e4eb19fa14434def9195f}

名為的查看器預設 `Shoppable_Banner` 包括以下資料：

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

使用以下命令載入查看器：

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

此示例等效於在URL中顯式指定的以下命令：

`style=etc/dam/presets/css/html5_interactiveimage.css`

## 示例4 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

名為的查看器預設 `Shoppable_Video_Dark` 包含以下資料：

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

使用以下命令載入查看器：

```
config=/etc/dam/presets/viewer/Shoppable_Video_Dark
```

此示例等效於在URL中顯式指定的以下命令：

```
style=etc/dam/presets/css/html5_interactivevideo_dark.css
```

## 示例5 {#section-19b988551d1d492a9079948e0b04b38f}

名為的查看器預設 `Carousel_Dotted_light` 以下資料：

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```

使用以下命令載入查看器：

```
config=/etc/dam/presets/viewer/Carousel_Dotted_light
```

此示例等效於在URL中顯式指定的以下命令：

```
style= etc/dam/presets/css/html5_carouselviewer_dotted_light.css
```
