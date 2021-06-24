---
description: 影像轉譯提供以規則運算式比對和替代規則為基礎的簡單要求預處理器。
solution: Experience Manager
title: 要求預先處理*
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 0%

---

# 要求預先處理*{#request-pre-processing}

影像轉譯提供以規則運算式比對和替代規則為基礎的簡單要求預處理器。

規則集合（規則集）可附加至每個材料目錄，包括預設目錄。 規則是使用XML格式的檔案指定的。

請求預處理規則可以在影像呈現解析器處理請求之前修改請求的路徑和查詢部分，包括操作路徑、添加命令、更改命令值以及應用模板或宏。 規則也可用來設定和覆寫通常僅以目錄屬性控制的特定功能，例如設定預設的回覆影像大小或將HTTP服務限制在特定用戶端IP位址。

請求預處理規則適用於多種應用程式，其中有些列於下列：

* 實作&#x200B;*虛擬路徑*&#x200B;機制，可將要求路徑重新對應至檔案、FTP和HTTP路徑。
* 不允許使用CPU密集型命令來防止伺服器濫用。
* 根據請求路徑或影像名稱控制影像品質設定（例如JPEG品質或銳利化）。

有關建立、使用和管理規則集的詳細資訊，可在「規則集參考」中找到。

另請參閱規則集參考，屬性：:RuleSetFile
