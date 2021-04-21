---
description: 「影像伺服」提供以規則運算式比對和替代規則為基礎的簡單請求預處理器。
solution: Experience Manager
title: 要求預處理
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---


# 請求預處理{#request-preprocessing}

「影像伺服」提供以規則運算式比對和替代規則為基礎的簡單請求預處理器。

規則集合（規則集）可附加至每個影像目錄，包括預設目錄。 規則是使用XML格式的檔案來指定。

請求預處理規則可修改請求的路徑和查詢部分，然後再由平台伺服器的剖析器處理，包括控制路徑、新增命令、變更命令值，以及套用範本或巨集。 規則也可用來設定和覆寫某些通常只受目錄屬性控制的安全功能，例如請求模糊化、水標籤，以及將HTTP服務限制在特定用戶端IP位址。

請求預處理規則適用於多種應用程式，其中有些應用程式列於下列：

* 實作&#x200B;*虛擬路徑*&#x200B;機制，允許將請求路徑重新對應至檔案、FTP和HTTP路徑。
* 選擇性強制執行安全功能，例如依影像名稱或路徑篩選的浮水印。
* 從特定IP位址存取伺服器時，省略浮水印或其他安全性功能。
* 強制將命令（例如`defaultImage=`）應用於所有請求或在URL路徑或查詢字串中顯示特定模式的請求。
* 不允許使用CPU密集型命令來防止伺服器濫用。
* 允許在HTTP或FTP伺服器上放置來源影像，同時仍在請求路徑上指定這些影像，而非使用`src=`。
* 根據請求路徑或影像名稱，控制影像品質設定（例如JPEG品質或銳利化）。

有關建立、使用和管理規則集的詳細資訊，請參閱[規則集參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)。

## 另請參閱 {#see-also}

[規則集參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)，屬 [性：:RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
