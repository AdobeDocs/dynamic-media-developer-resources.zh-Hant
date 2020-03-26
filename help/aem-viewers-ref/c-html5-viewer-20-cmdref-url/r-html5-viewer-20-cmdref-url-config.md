---
description: 所有檢視器通用的參數。
seo-description: 所有檢視器通用的參數。
seo-title: config
solution: Experience Manager
title: config
topic: Dynamic media
uuid: 9e9bb580-a33a-4405-b05c-56962d702145
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# config{#config}

所有檢視器通用的參數。

` config= *`configId`*`

<table id="table_9B98C97485DD4DEB8A6ECBCE8DF6B886"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> configId </span></span> </p> </td> 
   <td colname="col2"> <p>檢視器設定的目錄/ID。 </p> <p> 指定包含目錄：:UserData中的查看器配置屬 <span class="codeph"> 性的影像目錄條目 </span>。 當此命令出現時，檢視器會傳送 <span class="codeph"> configId的req=userdata </span> 命令至 <span class="codeph"> 伺服器，並 </span> 從回覆擷取屬性。 屬性用於初始化檢視器。 如果URL字串指定相同的屬性，則會覆寫目錄：:UserData <span class="codeph"> 中的值 </span>。 </p> </td> 
  </tr> 
 </tbody> 
</table>

所有可在預期、、、 `catalog::UserData` 和本身中指 `asset`定的檢視器 `serverUrl``contentUrl``searchServerUrl``config` 命令。

## 屬性 {#section-10ee45d637134e0fbcd943c62578cb78}

選填。

## 預設 {#section-d411e450028c460392cb8508f8ccc5d9}

無。

## Example 1 {#section-a8afbf76f8384aa0a83ed1feeccd5b9a}

名為2020的影像目錄包含該項目 `preset-oct`。 此目 `catalog::UserData` 錄條目的欄位包含以下資料：

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

## Example 2 {#section-577fce5ddbee43fc96d88b2055df47aa}

名為2019的影像目錄包含該項目 `spin-oct`。 此目 `catalog::UserData` 錄條目的欄位包含以下資料：

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

## Example 3 {#section-2b3a42c3926e4eb19fa14434def9195f}

名為的檢視器預 `Shoppable_Banner` 設集包含下列資料：

```
style=etc/dam/presets/css/html5_interactiveimage.css
```

使用下列命令載入檢視器：

```
config=/etc/dam/presets/viewer/Shoppable_Banner
```

這等同於URL中明確指定的下列命令：

`style=etc/dam/presets/css/html5_interactiveimage.css`

## Example 4 {#section-98dd1cc6b2a24375a1bd572fa83be35c}

名為的檢視器預 `Shoppable_Video_Dark` 設集包含下列資料：

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

## Example 5 {#section-19b988551d1d492a9079948e0b04b38f}

名為下列資料 `Carousel_Dotted_light` 的檢視器預設集：

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

