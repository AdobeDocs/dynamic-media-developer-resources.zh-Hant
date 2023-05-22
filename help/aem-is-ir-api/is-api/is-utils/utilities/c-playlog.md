---
description: 可以使用playlog實用程式為HTTP響應快取預生成內容。
solution: Experience Manager
title: 「playlog」實用程式
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: e0213978-3a1d-44b4-82bf-4527b980b29e
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 1%

---

# 「playlog」實用程式{#the-playlog-utility}

可以使用playlog實用程式為HTTP響應快取預生成內容。

在主版本升級後（當版本號的第一位或第二位更改時），不能保證現有的Image Serving HTTP響應快取可用。 如果在升級後伺服器要處於全負載狀態，則伺服器可能會過載處理最初幾個小時的快取未命中請求，直到合理填充快取並且快取命中率增加。

為避免此初始載入峰值， `playlog` 實用程式可用於預生成HTTP響應快取的內容。 `playlog` 從現有訪問日誌檔案中提取HTTP請求，並將其發送到伺服器以生成快取項。 對於典型的使用情形，只要播放包含全天流量的單個訪問日誌檔案就足夠了。

除了在升級安裝後啟動HTTP響應快取外，該實用程式還用於在將新伺服器添加到負載平衡環境中時預生成快取內容；只需從其他伺服器中回放最近的日誌檔案即可。

`playlog` 可以配置為支援由以前版本的Image Serving生成的大多數訪問日誌檔案。

## 使用 {#section-daa126ec469b4a9d90d59def4fdaacdd}

` playlog *[!DNL logFile]* [-n *[!DNL col]*] [-s *[!DNL separator]*] [-m *[!DNL marker]*] [-p *[!DNL prefix]*] [-x *[!DNL suffix]*] [-v] [-h] [-r *[!DNL request method]*] [-o *[!DNL position]*]`

<table id="simpletable_39B9638BCB0F4244B5155C958C044C31"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -p <span class="varname"> 前置詞 </span> </span> </p> </td> 
  <td class="stentry"> <p>根URL，用於預置到從日誌檔案提取的請求。 </p> <p>預設值： <span class="filepath"> http://localhost:8080/is </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -n <span class="varname"> 上 </span> </span> </p> </td> 
  <td class="stentry"> <p>欄位（列）號，其中包含日誌記錄中的請求；基於1。 </p> <p>預設值：16 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -s <span class="varname"> 分離器 </span> </span> </p> </td> 
  <td class="stentry"> <p>欄位分隔符；規則運算式模式。 </p> <p>預設: <span class="codeph"> [ ]+ </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -m <span class="varname"> 標籤 </span> </span> </p> </td> 
  <td class="stentry"> <p>請求標籤；標識日誌檔案中應回放的請求；規則運算式模式。 </p> <p>預設值： <span class="codeph"> 請求： </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -x <span class="varname"> 尾碼 </span> </span> </p> </td> 
  <td class="stentry"> <p>尾碼，附加到從日誌檔案中提取的請求；可用於將回放請求與日誌檔案中的即時請求分離；「？」 或「&amp;」分隔符自動插入；尾碼可以按大括弧內的位置引用任何日誌欄位，預設值與md5簽名欄位相對應。 </p> <p>預設值： <span class="codeph"> playlog={25} </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -v </span> </p> </td> 
  <td class="stentry"> <p>詳細模式，將生成的請求URL打印到 <span class="codeph"> 施圖 </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -h </span> </p> </td> 
  <td class="stentry"> <p>將簡要說明打印到 <span class="codeph"> 施圖 </span>。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -r </span> </p> </td> 
  <td class="stentry"> <p>request-method — 要使用的HTTP請求方法( <span class="codeph"> get|post|head|smart </span>)。 </p> <p>預設值： <span class="codeph"> 智慧 </span>) </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <span class="codeph"> -o </span> </p> </td> 
  <td class="stentry"> <p>request-method-pos - pos在日誌檔案中從中獲取原始方法。 </p> <p>預設值：15 </p> </td> 
 </tr> 
</table>

對於Windows，檔案名為 [!DNL playlog.bat] 在Linux上 [!DNL playlog.sh]。

## 範例 {#section-716e5c35e9fa4ee3a4b0687381fcea40}

以下示例將回放Linux上Image Serving建立的訪問日誌檔案中的所有請求：

`> cd /usr/local/Scene7/ImageServing/logs`

`> ../bin/playlog.sh access-2007-01-01.log -n 18 -s ' ' -m . -p http://localhost:8080`

以下命令將回放在Windows上的Image Serving建立的跟蹤日誌檔案中找到的所有請求：

`> "\Program Files\Scene7\ImageServing\bin\playlog.bat" d:\logs/access-2006-09-01.log`
