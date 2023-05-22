---
description: 包含映像伺服器配置設定。
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

包含映像伺服器配置設定。

修改此XML檔案時，必須注意維護有效的XML語法，否則映像伺服器可能無法啟動。

要使更改生效，請編輯此檔案後重新啟動映像伺服器。 只支援以下列出的元素值進行修改。 僅在Dynamic Media技術支援建議時編輯此檔案的任何其他內容。

>[!NOTE]
>
>不更改 `<imageserverregistry>`，包括元素順序。 編輯此檔案時請小心，否則映像伺服器可能無法啟動。

下面說明了可以更改的元素。 存在其他不能更改的元素。 以下元素的順序不能反映它們必須出現在檔案中的順序。

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

多重 `<RootPath>` 元素可能存在（每個源資料檔案資料夾一個）。 Image Server按指定查找特定源檔案的順序搜索根路徑。
