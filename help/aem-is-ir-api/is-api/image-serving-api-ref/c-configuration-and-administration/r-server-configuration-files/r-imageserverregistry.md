---
description: 包含影像伺服器組態設定。
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員、商業從業人員
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '172'
ht-degree: 0%

---


# ImageServerRegistry.xml{#imageserverregistry-xml}

包含影像伺服器組態設定。

修改此XML檔案時，請務必保留有效的XML語法，否則影像伺服器可能會無法啟動。

要使更改生效，請在編輯此檔案後重新啟動映像伺服器。 僅支援下列元素值進行修改。 只有在Dynamic Media技術支援人員告知時，才能編輯此檔案的任何其他內容。

>[!NOTE]
>
>請勿變更`<imageserverregistry>`的結構，包括元素順序。 編輯此檔案時請小心，否則可能會無法啟動映像伺服器。

以下說明哪些元素可以變更。 其他元素不得變更。 以下元素的順序並不反映檔案中元素必須出現的順序。

```
<imageserverregistry>
    <TcpPort> 27345 </TcpPort>    
    <RootPath ./images </RootPath>
    <TempDirectory ./temp </TempDirectory>
    <Log> ./logs/ImageServer.log </Log>
    <TraceClient> 2 </TraceClient>
    <TraceStatsInterval> 600 </TraceStatsInterval>
    <PhysicalMemory> 20 </PhysicalMemory>
    <WorkerThreads> 0 </WorkerThreads>
    <SVGTcpPort> 27346 </SVGTcpPort>
    <MaxRenderRgnPixels> 16 </MaxRenderRgnPixels>
    <MaxSavePixels> 100 </MaxSavePixels>
    <MaxMessageSize> 16 </MaxMessageSize>
    <CacheServerUrl> http://localhost:8080/is/cache/secondary </CacheServerUrl>
    <NumberOfTextServers> 0 </NumberOfTextServers>
    <TextServerTcpPortRange> 27347-27380 </TextServerTcpPortRange>
    <SaveDirectory> ./ </SaveDirectory>
    <RemoteUrlDefaultExpiration> 36000 </RemoteUrlDefaultExpiration>
    <RemoteUrlTimeout> 60 </RemoteUrlTimeout>
    <MaxNonDsfSize> 4 </MaxNonDsfSize>
</imageserverregistry>
```

## 附註 {#section-7217f011f69f41e7af4f3983d7776d6f}

可能存在多個`<RootPath>`元素（每個源資料檔案資料夾各一個）。 影像伺服器會依指定順序搜尋根路徑，以尋找特定來源檔案。
