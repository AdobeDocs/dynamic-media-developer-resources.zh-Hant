---
description: 雖然新增資料檔案簡單且直接，但取代伺服器目前主動使用的現有資料檔案時，必須特別小心。 建議不要簡單地替換這些檔案，而是為替換檔案提供新名稱（例如在檔案名中附加版本尾碼）。 新檔案上線後，即可刪除舊版本。
solution: Experience Manager
title: 刪除或替換資料檔案
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin,User
exl-id: 1624e1b5-ba79-45db-8309-457a44fddab8
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '319'
ht-degree: 0%

---

# 刪除或替換資料檔案{#deleting-or-replacing-data-files}

雖然新增資料檔案簡單且直接，但取代伺服器目前主動使用的現有資料檔案時，必須特別小心。 建議不要簡單地替換這些檔案，而是為替換檔案提供新名稱（例如在檔案名中附加版本尾碼）。 新檔案上線後，即可刪除舊版本。

>[!NOTE]
>
>影像伺服作用中使用時，資料檔案絕不應被取代或刪除。 錯誤或甚至伺服器當機可能會發生。

在所有情況下，請記住 [!DNL Platform Server] 快取和客戶端快取條目必須過時，客戶端才能看到更新的資料。 可使用 `cache=validate` 命令。

快取管理器不會直接追蹤字型檔案和ICC設定檔檔案的變更。 如果修改了此類資源而未更改其ID，則伺服器快取將不知道該更改， `cache=validate` 不會更新快取項目。 `cache=update` 可用於強制重新生成這樣的快取條目。

為避免替換檔案的複雜性，建議為替換檔案指定新名稱並更新相應的目錄條目。 這將允許在伺服器上線時替換任何資料檔案，並導致伺服器快取項立即過期，而不需進行額外干預。 此方法可用於由影像目錄管理的ICC配置檔案、字型和所有影像。
