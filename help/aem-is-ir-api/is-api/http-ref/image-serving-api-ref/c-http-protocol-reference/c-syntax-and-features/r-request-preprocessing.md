---
description: 「影像伺服」會根據規則運算式相符和替代規則，提供簡單的要求前置處理器。
solution: Experience Manager
title: 要求預先處理
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: f855c36f-29f2-4ada-a103-1eb9b7b0c1a0
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '283'
ht-degree: 0%

---

# 要求預先處理{#request-preprocessing}

「影像伺服」會根據規則運算式相符和替代規則，提供簡單的要求前置處理器。

可以將規則集合（規則集）附加到每個影像目錄，包括預設目錄。 規則是以XML格式檔案指定的。

要求前置處理規則可在[!DNL Platform Server]的剖析器處理要求之前，修改要求的路徑和查詢部分，包括操作路徑、新增命令、變更命令值，以及套用範本或巨集。 規則也可用來設定和覆寫某些安全性功能，這些功能通常僅由目錄屬性控制，例如要求模糊化、標籤水印，以及將HTTP服務限製為特定使用者端IP位址。

要求預先處理規則適用於多種應用程式，其中有些應用程式列示如下：

* 實作&#x200B;*虛擬路徑*&#x200B;機制，允許將請求路徑重新對應到檔案、FTP和HTTP路徑。
* 選擇性地強制實施安全性功能，例如依影像名稱或路徑篩選的浮水印。
* 從特定IP位址存取伺服器時，省略浮水印或其他安全性功能。
* 強制套用命令（例如`defaultImage=`）至所有要求或在URL路徑或查詢字串中顯示特定模式的要求。
* 禁止使用CPU密集型命令來防止伺服器濫用。
* 允許來源影像位於HTTP或FTP伺服器上，同時仍在請求路徑上指定這些影像，而不是使用`src=`。
* 根據請求路徑或影像名稱控制影像品質設定(例如JPEG品質或銳利化)。

有關建立、使用和管理規則集的詳細資訊，請參閱[規則集參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)。

## 另請參閱 {#see-also}

[規則集參考](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-rule-set-reference/c-rule-set-reference.md#concept-3e5058cf3507470b82cac638df23ea8e)，[屬性：：RuleSetFile](../../../../../is-api/image-catalog/image-serving-api-ref/c-image-catalog-reference/c-overview/c-file-formats/r-rule-set-files.md#reference-3e54cb5f4d74411a84889fed056ac093)
