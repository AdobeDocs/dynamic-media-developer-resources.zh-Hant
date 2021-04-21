---
description: 「影像轉換」提供以規則運算式比對和替代規則為基礎的簡單請求預處理器。
solution: Experience Manager
title: 要求預先處理*
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: d0bc88f55f857762b3bab4c76d1e3f3dd2733d60
workflow-type: tm+mt
source-wordcount: '218'
ht-degree: 0%

---


# 請求預處理*{#request-pre-processing}

「影像轉換」提供以規則運算式比對和替代規則為基礎的簡單請求預處理器。

規則集合（規則集）可附加到每個物料目錄，包括預設目錄。 規則是使用XML格式的檔案來指定。

請求預處理規則可修改請求的路徑和查詢部分，然後再由影像轉換解析器處理，包括控制路徑、新增命令、變更命令值，以及套用範本或巨集。 規則也可用來設定和覆寫通常僅以目錄屬性控制的特定功能，例如設定預設的回覆影像大小或將HTTP服務限制在特定用戶端IP位址。

請求前處理規則適用於多種應用程式，其中有些應用程式列於下列：

* 實作&#x200B;*虛擬路徑*&#x200B;機制，允許將請求路徑重新對應至檔案、FTP和HTTP路徑。
* 不允許使用耗用大量CPU的指令來防止伺服器濫用。
* 根據請求路徑或影像名稱，控制影像品質設定（例如JPEG品質或銳利化）。

有關建立、使用和管理規則集的詳細資訊，請參閱規則集參考。

另請參閱規則集參考，屬性：:RuleSetFile
