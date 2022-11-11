---
description: Image Serving根據規則運算式比對和替代規則提供簡單請求預處理器。
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

Image Serving根據規則運算式比對和替代規則提供簡單請求預處理器。

規則集合（規則集）可附加至每個影像目錄，包括預設目錄。 規則是使用XML格式的檔案指定的。

請求預處理規則可在由 [!DNL Platform Server]s解析器，包括操作路徑、添加命令、更改命令值以及應用模板或宏。 規則也可用來設定和覆寫某些安全功能，這些功能通常僅限目錄屬性控制，例如要求模糊化、加水標籤，以及將HTTP服務限制在特定用戶端IP位址。

請求預處理規則適用於多種應用程式，其中有些如下所列：

* 實作 *虛擬路徑* 機制，可將要求路徑重新對應至檔案、FTP和HTTP路徑。
* 選擇性地強制執行安全功能，例如由影像名稱或路徑篩選的水印。
* 從特定IP地址訪問伺服器時省略水印或其他安全功能。
* 強制應用命令，例如 `defaultImage=`，傳至URL路徑或查詢字串中顯示特定模式的所有要求或要求。
* 不允許使用CPU密集型命令來防止伺服器濫用。
* 允許在HTTP或FTP伺服器上放置來源影像，同時仍在請求路徑上指定來源影像，而非透過 `src=`.
* 根據請求路徑或影像名稱，控制影像品質設定(例如JPEG品質或銳利化)。

有關建立、使用和管理規則集的詳細資訊，請參閱 [規則集參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e).

## 另請參閱 {#see-also}

[規則集參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e), [屬性：:RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
