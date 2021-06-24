---
description: 更新資產的發佈內容狀態。
solution: Experience Manager
title: ContextStateUpdate
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 4e450d28-ec79-4540-824b-b0121b72c857
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '59'
ht-degree: 15%

---

# ContextStateUpdate{#contextstateupdate}

更新資產的發佈內容狀態。

語法

## 參數 {#section-9f747df071854c6896fdbb95684ad947}

使用`setAssetsContextState`設定資產的發佈內容狀態。

<table id="table_FD172CEA4EFE44E08ADA22D090DC06CA">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 名稱 </th>
   <th colname="col2" class="entry"> 類型 </th>
   <th colname="col3" class="entry"> 說明 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> contextHandle</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string </span></td>
   <td colname="col3"> 處理發佈內容。 </td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> publishState</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:string</span></td>
   <td colname="col3">針對指定的發佈內容更新資產的已發佈狀態。 包括： 
    <ul id="ul_CF6019C4CA3648B687C252F1A7C2EAAF">
     <li id="li_4367D7A058F045D98CDF58009E2AC7BC"><span class="codeph"> MarkedForPublish</span></li>
     <li id="li_EEFC6A76C1014C6D9D5E66F271B68606"><span class="codeph"> NotMarkedForPublish</span></li>
     <li id="li_5145CFA39F5249C48DBD0A37543AF055"><span class="codeph"></span></li>
    </ul></td>
  </tr>
 </tbody>
</table>

>[!MORELIKETHIS]
>
>* [發佈狀態](../../string-constants/c-string-constants/r-publish-state.md#reference-a9d80231514b4272b39d10c1a7aadca8)

