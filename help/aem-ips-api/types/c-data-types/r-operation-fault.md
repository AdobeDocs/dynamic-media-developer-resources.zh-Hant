---
description: 對CDN無效請求中提供的一個URL作出響應的詳細消息。
solution: Experience Manager
title: 操作故障
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: e1fa7f66-f9d9-45cd-a9b3-d0ff344b137d
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '49'
ht-degree: 12%

---

# 操作故障{#operationfault}

對CDN無效請求中提供的一個URL作出響應的詳細消息。

**自**

4.5.0，修補程式2011-02

## 參數 {#section-cf4b0c923cef4c14869319af73ace58b}

| ** 名稱** | ** 類型** | ** 說明** |
|---|---|---|
| 代碼 | `xsd:int` | 從CDN提供的錯誤代碼 |
| 原因 | `xsd:string` | 從CDN提供的錯誤消息 |
