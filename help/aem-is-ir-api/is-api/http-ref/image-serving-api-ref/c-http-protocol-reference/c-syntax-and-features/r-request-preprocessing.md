---
description: Image Service基於規則運算式匹配和替換規則提供簡單的請求預處理器。
solution: Experience Manager
title: 請求預處理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# 請求預處理{#request-preprocessing}

Image Service基於規則運算式匹配和替換規則提供簡單的請求預處理器。

規則（規則集）的集合可以附加到每個影像目錄，包括預設目錄。 規則由XML格式的檔案指定。

請求預處理規則可以在請求由 [!DNL Platform Server]s解析器，包括操作路徑、添加命令、更改命令值以及應用模板或宏。 規則還可用於配置和覆蓋某些通常僅通過目錄屬性控制的安全功能，例如請求混淆、水標籤，以及將HTTP服務限制到特定客戶端IP地址。

請求預處理規則適用於各種應用程式，其中有些如下：

* 實施 *虛擬路徑* 機制，允許將請求路徑重新映射到檔案、FTP和HTTP路徑。
* 有選擇地強制按影像名稱或路徑過濾的安全特徵，如水印。
* 在從特定IP地址訪問伺服器時省略水印或其他安全功能。
* 強制應用命令，如 `defaultImage=`、到URL路徑或查詢字串中顯示特定模式的所有請求或請求。
* 不允許使用CPU密集型命令來防止伺服器濫用。
* 允許源映像位於HTTP或FTP伺服器上，同時仍在請求路徑上指定，而不是使用 `src=`。
* 根據請求路徑或影像名稱控制影像質量設定(如JPEG質量或銳化)。

有關建立、使用和管理規則集的詳細資訊，請參見 [規則集引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)。

## 另請參閱 {#see-also}

[規則集引用](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)。 [屬性：:RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
