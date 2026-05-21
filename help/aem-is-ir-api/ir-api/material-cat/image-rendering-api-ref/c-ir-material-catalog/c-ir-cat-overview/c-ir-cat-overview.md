---
title: 材質目錄概觀
description: 材質目錄會提供暈映、材質和支援資料（例如ICC設定檔）的相關資訊給伺服器。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: d26371da-e992-4f63-a5be-190ce60eca2f
TQID: 'https://experienceleague.adobe.com/wMShsstpVRBE4JNSUshejo0Qn6NXVB85YbLx5Pf9PEI'
product_v2: id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2: id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 413
ht-degree: 0%

---

# 材質目錄概觀{#material-catalog-overview}

材質目錄會提供暈映、材質和支援資料（例如ICC設定檔）的相關資訊給伺服器。

每個材質目錄都包含必要的&#x200B;*目錄屬性檔案*&#x200B;和一組選用的&#x200B;*目錄資料檔案*：

* 暈映對映檔案，可逐項列出暈映和範本及其關聯的中繼資料。
* 材質資料檔案，可逐項列出材質並指定關聯的紋理影像檔案和中繼資料。
* 巨集定義檔案，提供要求巨集的定義。
* 設定檔對映檔案，其中列舉ICC色彩設定檔。

目錄資料檔案與材料目錄相關聯，其方式為目錄屬性檔案中的檔案參照。 多個材料目錄可以共用相同的目錄資料檔案。

目錄屬性檔案必須有[!DNL `.ini`]個檔案字尾，而且必須位於影像轉譯&#x200B;*目錄資料夾* ( [!DNL PlatformServer::ir.catalogRootPath])中。 目錄資料檔案可以在相同的資料夾或呈現伺服器可存取的任何其他資料夾中。

**正在更新材料目錄**

伺服器持續監視目錄資料夾。 當它偵測到主目錄屬性檔案已變更時，會自動重新載入材料目錄，包括關聯的目錄資料檔案。 因此，若要更新伺服器上的材質目錄，請先取代所有需要變更的目錄資料檔案，然後取代（或「接觸」）目錄屬性檔案以觸發目錄重新載入。

**預設目錄**

預設型錄為所有材料型錄的所有型錄屬性提供預設值。 如果在特定材質目錄中找不到特定屬性，則伺服器會改用預設目錄中的對應值。 同樣地，預設目錄可用於為特定目錄資料記錄（材料和ICC設定檔）提供預設值。 如果在特定資料目錄中找不到特定資料記錄，則伺服器會嘗試在預設目錄中尋找該記錄。 如此可讓材質目錄稀疏填入，並簡化全域屬性和資料（例如共用範本、巨集和字型）的管理。

此外，預設型錄會在作業中不包含特定材料型錄時，提供所有屬性和資料記錄（ICC設定檔）。

若要讓轉譯伺服器正確運作，預設目錄的目錄屬性檔案必須命名為[!DNL default.ini]。 它也必須永遠存在於目錄資料夾中，而且必須填入所有必要的屬性，不包括`attribute::RootId`和各種目錄資料檔的參照，這些都是選擇性的。

<!--
 **See also**

`PlatformServer::ir.catalogRootPath`
-->
