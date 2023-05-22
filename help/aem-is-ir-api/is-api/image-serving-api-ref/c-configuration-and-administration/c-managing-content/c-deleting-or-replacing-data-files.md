---
description: 雖然添加新資料檔案是簡單而直接的，但替換伺服器主動使用的現有資料檔案時必須特別小心。 建議不要簡單地替換這些檔案，而是給替換檔案一個新名稱（例如，在檔案名中附加一個版本尾碼）。 新檔案生效後，舊版本可以刪除。
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

雖然添加新資料檔案是簡單而直接的，但替換伺服器主動使用的現有資料檔案時必須特別小心。 建議不要簡單地替換這些檔案，而是給替換檔案一個新名稱（例如，在檔案名中附加一個版本尾碼）。 新檔案生效後，舊版本可以刪除。

>[!NOTE]
>
>在影像服務活動使用期間，不應替換或刪除資料檔案。 否則可能會發生錯誤甚至伺服器崩潰。

無論如何，記住 [!DNL Platform Server] 在客戶端看到更新的資料之前，快取和客戶端快取項必須過時。 可以使用 `cache=validate` 的子菜單。

快取管理器不直接跟蹤對字型檔案和ICC配置檔案的更改。 如果修改了此類資源而未更改其ID，則伺服器快取將不知道該更改， `cache=validate` 不會導致更新快取項。 `cache=update` 可用於強制重新生成此類快取條目。

為避免替換檔案的複雜性，建議為替換檔案指定新名稱並更新相應的目錄條目。 這將允許在伺服器處於活動狀態時替換任何資料檔案，並導致伺服器快取項立即失效而不需要額外干預。 此方法可用於ICC配置檔案、字型和所有由影像目錄管理的影像。
