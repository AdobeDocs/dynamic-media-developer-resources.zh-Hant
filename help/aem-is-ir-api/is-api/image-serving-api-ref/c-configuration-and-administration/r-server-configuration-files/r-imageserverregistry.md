---
description: 包含映像伺服器配置設定。
solution: Experience Manager
title: ImageServerRegistry.xml
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,User
exl-id: 4483c5e8-5123-4d0f-bf9a-4ef8d8cec5a9
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 0%

---

# ImageServerRegistry.xml{#imageserverregistry-xml}

包含映像伺服器配置設定。

修改此XML檔案時，必須注意維護有效的XML語法，否則影像伺服器可能無法啟動。

要使更改生效，請在編輯此檔案後重新啟動映像伺服器。 修改僅支援下列元素值。 只有在Dynamic Media技術支援提供建議時，才編輯此檔案的任何其他內容。

>[!NOTE]
>
>請勿變更`<imageserverregistry>`的結構，包括元素順序。 編輯此檔案時請小心，否則影像伺服器可能無法啟動。

以下說明可以變更的元素。 其他元素存在，且不可變更。 以下元素的順序不反映檔案中必須呈現的順序。

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

可能存在多個`<RootPath>`元素（每個源資料檔案資料夾各一個）。 Image Server按指定的順序搜索根路徑以查找特定源檔案。
