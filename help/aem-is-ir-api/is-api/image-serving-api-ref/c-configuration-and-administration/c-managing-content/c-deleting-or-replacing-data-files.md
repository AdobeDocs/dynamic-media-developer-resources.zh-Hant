---
description: 雖然新增資料檔案既簡單又直接，但取代伺服器主動使用的現有資料檔案時，必須格外小心。 建議不要簡單地替換這些檔案，而是為替換檔案指定新名稱（例如，在檔案名中附加版本尾碼）。 新檔案上線後，舊版可以刪除。
solution: Experience Manager
title: 刪除或替換資料檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '331'
ht-degree: 0%

---


# 刪除或替換資料檔案{#deleting-or-replacing-data-files}

雖然新增資料檔案既簡單又直接，但取代伺服器主動使用的現有資料檔案時，必須格外小心。 建議不要簡單地替換這些檔案，而是為替換檔案指定新名稱（例如，在檔案名中附加版本尾碼）。 新檔案上線後，舊版可以刪除。

>[!NOTE]
>
>在影像伺服作用中時，絕不應取代或刪除資料檔案。 否則可能會發生錯誤，甚至伺服器當機。

在所有情況下，請記住，Platform Server快取和用戶端快取項目必須過時，客戶端才會看到更新的資料。 使用`cache=validate`命令可立即更新特定的快取條目。

快取管理員不會直接追蹤字型檔案和ICC描述檔的變更。 如果在未更改其ID的情況下修改了此類資源，則伺服器快取將不知道該更改，並且`cache=validate`將不會導致快取條目更新。 `cache=update` 可用於強制重新生成此類快取條目。

為避免替換檔案的複雜性，建議為替換檔案指定新名稱並更新相應的目錄項。 這可讓伺服器上線時取代任何資料檔案，並導致伺服器快取項目立即失效，毋需額外干預。 此方法可用於ICC描述檔、字型和由影像目錄管理的所有影像。
