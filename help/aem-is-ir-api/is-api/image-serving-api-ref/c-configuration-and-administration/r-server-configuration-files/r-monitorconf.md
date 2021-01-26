---
description: 包含監視／警報系統的設定。
seo-description: 包含監視／警報系統的設定。
seo-title: monitor.conf
solution: Experience Manager
title: monitor.conf
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 31949797-df2c-4b7c-841b-4c623299a228
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 2%

---


# monitor.conf{#monitor-conf}

包含監視／警報系統的設定。

此檔案是JAVA屬性檔案。 必須注意遵守適當的公約；否則平台伺服器可能無法啟動。 請注意，在Windows檔案路徑中，必須使用雙反斜線&#39;\\&#39;或單正斜線&#39;/&#39;，而非反斜線&#39;\&#39;，因為反斜線是此類檔案中的轉義字元。

此檔案的變更會在儲存檔案後不久生效。

<table id="simpletable_91557E1162FF4FEC8BE1722D6656CFEE"> 
 <tr class="strow"> 
  <td class="stentry"> <p>一般 </p> </td> 
  <td class="stentry"> <p> <span class="codeph"> monitorAlertGenerator.enableGlobalAlerting=false  </span> </p> <p> <span class="codeph"> mailSender.host=127.0.0.1  </span> </p> <p> <span class="codeph"> mailSender.port=25  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageTo=noone@scene7.com  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.messageFrom=noone@scene7.com  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.alertInterval=600000  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.heapSpaceResetInterval=600000  </span> </p> <p> <span class="codeph"> monitorAlertGenerator.minTrafficForAlerts=0.0  </span> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>警報臨界值 </p> </td> 
  <td class="stentry"> <p> monitorAlertGenerator.maxAverageResponseTime=200 </p> <p> monitorAlertGenerator.maxErrorRate=0.05 </p> <p> monitorAlertGenerator.minRequestRate=0.0 </p> <p> monitorAlertGenerator.minFreeHeapSpace=52428800 </p> <p> monitorAlertGenerator.maxOverlap=20 </p> <p> monitorAlertGenerator.lockedThreshold=60000 </p> </td> 
 </tr> 
</table>

