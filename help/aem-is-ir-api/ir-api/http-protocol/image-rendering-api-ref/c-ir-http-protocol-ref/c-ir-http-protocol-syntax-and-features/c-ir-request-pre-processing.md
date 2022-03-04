---
title: 請求預處理
description: 「影像渲染」提供基於規則運算式匹配和替換規則的簡單請求預處理器。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 79a358db-0fd6-4327-a305-b0b38ad62050
source-git-commit: 20f4922402bd31c71ae650a01597b574220809fa
workflow-type: tm+mt
source-wordcount: '210'
ht-degree: 0%

---

# 請求預處理{#request-pre-processing}

「影像渲染」提供基於規則運算式匹配和替換規則的簡單請求預處理器。

規則（規則集）的集合可以附加到每個物料目錄，包括預設目錄。 規則由XML格式的檔案指定。

請求預處理規則可以在請求由影像呈現分析器處理之前修改其路徑和查詢部分。 本方案包括操作路徑、添加命令、更改命令值以及應用模板或宏。 規則還可用於配置和覆蓋通常僅使用目錄屬性控制的某些功能，例如設定預設的應答影像大小或將HTTP服務限制到特定的客戶端IP地址。

請求預處理規則適用於各種應用程式，其中一些如下：

* 實施 *虛擬路徑* 機制，允許將請求路徑重新映射到檔案、FTP和HTTP路徑。
* 禁止使用CPU密集型命令來防止伺服器濫用。
* 根據請求路徑或影像名稱控制影像質量設定(如JPEG質量或銳化)。

有關建立、使用和管理規則集的詳細資訊，請參閱規則集參考。

另請參閱規則集引用，屬性：:RuleSetFile
