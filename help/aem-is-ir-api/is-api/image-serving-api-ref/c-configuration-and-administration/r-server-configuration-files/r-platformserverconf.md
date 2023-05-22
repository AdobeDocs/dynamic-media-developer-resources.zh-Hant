---
description: 包含 [!DNL Platform Server] 的子菜單。
solution: Experience Manager
title: PlatformServer.conf
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 00d55453-e7e6-4242-be83-7efa12764e5d
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---

# PlatformServer.conf{#platformserver-conf}

包含 [!DNL Platform Server] 的子菜單。

此檔案是JAVA屬性檔案。 必須注意遵守適當的公約；否則， [!DNL Platform Server] 可能無法啟動。 在Windows檔案路徑中，使用雙反斜線「\\」或單正斜線「/」，而不是反斜線「\」。 反斜線用作此類檔案中的轉義字元。

對此檔案的更改在保存檔案後生效。

只能在中更改下面列出的設定 [!DNL PlatformServer.conf]。 如果缺少特定設定，則可以在檔案的任何位置添加該設定。 每個設定只能有一個實例。

<table id="simpletable_38244750F50A46E5B0077F5F860B125C"> 
 <tr class="strow"> 
  <td class="stentry"> <p>常規 [!DNL Platform Server] 設定 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cache.rootPaths=../快取 </span> </p> <p> <span class="codeph"> cache.maxEntries=100000 </span> </p> <p> <span class="codeph"> cache.maxSize=1073741824 </span> </p> <p> <span class="codeph"> isConnection.port=27345 </span> </p> <p> <span class="codeph"> allowDefaultCatalogRequsts=true </span> </p> <p> <span class="codeph"> saveToFile.saveTimeout=60000 </span> </p> <p> <span class="codeph"> staticContent.rootPaths=。/static內容 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>快取群集配置 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> cluster.hosts=&lt;empty&gt; </span> </p> <p> <span class="codeph"> cacheCluster.queryTimeout=50 </span> </p> <p> <span class="codeph"> cacheCluster.fetchTimeout=10000 </span> </p> <p> <span class="codeph"> cacheCluster.updateLocalCache=true </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>重定向配置錯誤 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> errorRedirect.rootUrl=&lt;empty&gt; </span> </p> <p> <span class="codeph"> errorRedirect.connectTimeout=1000 </span> </p> <p> <span class="codeph"> errorRedirect.socketTimeout=30000 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>SVG配置 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> SvgProvider.rootPaths=../影像 </span> </p> <p> <span class="codeph"> svgProvider.SVGFileSizeLimit=1024 </span> </p> <p> <span class="codeph"> SVGProvider.port=8080 </span> </p> <p> <span class="codeph"> SvgProvider.fontRoot=../影像 </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>媒體集響應 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> fvctx.useCatalogRecordValidation=false </span> </p> <p> <span class="codeph"> fvctx.netsingLimit=10 </span> </p> <p> <span class="codeph"> fvctx.brochureLimit=20 </span> </p> </td> 
 </tr> 
</table>
