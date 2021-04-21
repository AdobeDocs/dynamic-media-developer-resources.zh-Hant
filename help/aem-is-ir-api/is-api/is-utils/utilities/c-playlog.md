---
description: playlog實用程式可用於預生成HTTP響應快取的內容。
solution: Experience Manager
title: 「playlog」實用程式
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '429'
ht-degree: 1%

---


# &#39;playlog&#39;實用程式{#the-playlog-utility}

playlog實用程式可用於預生成HTTP響應快取的內容。

現有的影像伺服HTTP回應快取在主要版本升級後（當版本號碼的第一或第二位數變更時）無法保證可用。 如果伺服器在升級後要進入全負載狀態，則伺服器可能會過載處理快取未命中請求的前幾個小時，直到快取被合理填充並且快取命中率增加。

為避免此初始載入尖峰，`playlog`公用程式可用來預先產生HTTP回應快取的內容。 `playlog` 從現有訪問日誌檔案中提取HTTP請求，並將其發送到伺服器以生成快取條目。對於一般的使用情形，只要播放包含全天流量的單一存取記錄檔即可。

除了在安裝升級後啟動HTTP響應快取外，在向負載平衡環境添加新伺服器時，該實用程式還用於預生成快取內容；只要從其他伺服器中播放最近的記錄檔即可。

`playlog` 可以配置為支援由舊版映像服務生成的大多數訪問日誌檔案。

## 使用 {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p首 <span class="varname"> 碼  </span> </span> </p> </td> 
  <td class="stentry"> <p>根URL，附加至從記錄檔擷取的請求之前。 </p> <p>預設值：<span class="filepath"> http://localhost:8080/is </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n列 <span class="varname"> 表  </span> </span> </p> </td> 
  <td class="stentry"> <p>欄位（列）號，在日誌記錄中包含請求；基於1。 </p> <p>預設值：16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s分 <span class="varname"> 隔符  </span> </span> </p> </td> 
  <td class="stentry"> <p>欄位分隔符號；規則運算式模式。 </p> <p>預設: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m標 <span class="varname"> 記  </span> </span> </p> </td> 
  <td class="stentry"> <p>請求標籤；識別記錄檔中應播放的請求；規則運算式模式。 </p> <p>預設值：<span class="codeph">請求：</span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x字 <span class="varname"> 尾  </span> </span> </p> </td> 
  <td class="stentry"> <p>尾碼，附加到從日誌檔案提取的請求中；可用來將播放請求與記錄檔中的即時請求分開；'?' 或自動插入'&amp;'分隔符；尾碼可以按大括弧內的位置引用任何日誌欄位，預設值與md5簽名欄位相對應。 </p> <p>預設值：<span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v  </span> </p> </td> 
  <td class="stentry"> <p>詳細模式下，將生成的請求URL打印到<span class="codeph"> stdout </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h  </span> </p> </td> 
  <td class="stentry"> <p>將總覽列印為<span class="codeph"> stdout </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method —— 要使用的HTTP請求方法(<span class="codeph"> get|post|head|smart </span>)。 </p> <p>預設值：<span class="codeph"> smart </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos —— 記錄檔中的pos，從中擷取原始方法。 </p> <p>預設值：15 </p> </td> 
 </tr> 
</table>

對於Windows，檔案名為[!DNL playlog.bat] ，在Linux上為[!DNL playlog.sh]。

## 範例 {#section-716e5c35e9fa4ee3a4b0687381fcea40}

以下示例將重放由Linux上的Image Serving建立的訪問日誌檔案中的所有請求：

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

以下命令會回放在Windows上映像服務建立的跟蹤日誌檔案中找到的所有請求：

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
