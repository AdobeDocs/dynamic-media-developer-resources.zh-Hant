---
description: 包含影像伺服器組態設定。
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
source-git-commit: 38afaf2ed0f01868f02e236e941b23eed5b790aa
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

包含影像伺服器組態設定。

修改此XML檔案時，必須注意要維持有效的XML語法，否則「影像伺服器」可能無法啟動。

若要讓變更生效，請在編輯此檔案後重新啟動影像伺服器。 僅支援以下列出的元素值以進行修改。 只有在Dynamic Media技術支援提供建議時，才能編輯此檔案的任何其他內容。

>[!NOTE]
>
>請勿變更`<imageserverregistry>`的結構，包括元素的順序。 請謹慎編輯此檔案，否則影像伺服器可能無法啟動。

以下說明哪些元素可以變更。 存在其他不可變更的元素。 下列元素的順序並未反映它們必須出現在檔案中的順序。

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

可能有多個`<RootPath>`元素（每個來源資料檔案資料夾各一個）。 Image Server會依指定的順序搜尋根路徑，以尋找特定的來源檔案。
