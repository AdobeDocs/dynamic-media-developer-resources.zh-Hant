---
title: getComponent
description: eCatalog檢視器的JavaScript API參考
solution: Experience Manager
feature: Dynamic Media Classic,Viewers,SDK/API,eCatalog
role: Developer,User
exl-id: 86f0802c-a53e-426d-9f64-21d8002b8b69
source-git-commit: edc127dc6e2ae2d9bd5feed08c8bc896c8c39747
workflow-type: tm+mt
source-wordcount: '237'
ht-degree: 0%

---

# getComponent{#getcomponent}

eCatalog檢視器的JavaScript API參考

`getComponent(componentId)`

傳回檢視器所使用之檢視器SDK元件的參考。 網頁可使用此方法來延伸或自訂現成可用的檢視器的行為。 只有在執行`initComplete`檢視器回呼之後，才呼叫此方法，否則檢視器邏輯可能尚未建立元件。

## 參數 {#section-4fb77a645fdd45b3aaa5079c31e3bb05}

`*`componentID`*` - `{String}`檢視器所使用的檢視器SDK元件識別碼。 此檢視器支援下列元件ID：

<table id="table_7B5DD9303EF44ADD847B13FFEAD135D9"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>元件ID </p> </th> 
   <th colname="col2" class="entry"> <p>檢視器SDK元件類別名稱 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> parameterManager </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.ParameterManager </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">容器</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Container </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">媒體集</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.MediaSet </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> pageView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.PageView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> primaryControls </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">次要控制項</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ControlBar </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> gridView </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.ThumbnailGridView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">目錄目錄</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.set.TableOfContents </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> infoPanelPopup </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.info.InfoPanelPopup </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> imageMapEffect </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.image.ImageMapEffect </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> leftButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> rightButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomInButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomInButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomOutButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomOutButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> zoomResetButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> secondaryZoomResetButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ZoomResetButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> thumbnailPageButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.ThumbnailPageButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> fullScreenButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.FullScreenButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toolBarLeftButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> toolBarRightButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> firstPageButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> secondaryFirstPageButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanLeftButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> lastPageButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> secondaryLastPageButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.PanRightButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> closeButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.CloseButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> socialShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.SocialShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> twitterShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.TwitterShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> facebookShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.FacebookShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> linkShare </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.LinkShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">電子郵件共用</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.EmailShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">內嵌共用</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.EmbedShare </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">列印</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.share.Print </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">下載</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.common.Download </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">我的最愛效果</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.FavoritesEffect </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">我的最愛檢視</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.FavoritesView </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">我的最愛功能表</span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.FavoritesMenu </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> addFavoriteButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.AddFavoriteButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> removeFavoriteButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.RemoveFavoriteButton </span> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> viewAllFavoriteButton </span> </p> </td> 
   <td colname="col2"> <p> <span class="codeph"> s7sdk.favorites.ViewAllFavoriteButton </span> </p> </td> 
  </tr> 
 </tbody> 
</table>

使用SDK API時，請務必使用正確的完整SDK名稱空間，如[檢視器SDK名稱空間](../../../c-html5-s7-aem-asset-viewers/c-html5-20-ecatalog-viewer-about/c-html5-20-ecatalog-html5-viewer-sdk-namespace.md#concept-16ce67bfbdc64ffc8fc7ad174f208f05)所述。

如需特定元件的詳細資訊，請參閱&#x200B;*檢視器SDK API*&#x200B;檔案。

## 傳回 {#section-1d3cf85bc7cc4dfe9670e038d02b9101}

`{Object}`檢視器SDK元件的參考。 如果`componentId`不是支援的檢視器元件，或檢視器邏輯尚未建立元件，則方法會傳回`null`。

## 範例 {#section-9e9332aa86b74a5fb321375c03fdc5b3}

```
<instance>.setHandlers({ 
 "initComplete":function() { 
  var pageView = <instance>.getComponent("pageView"); 
} 
})
```
