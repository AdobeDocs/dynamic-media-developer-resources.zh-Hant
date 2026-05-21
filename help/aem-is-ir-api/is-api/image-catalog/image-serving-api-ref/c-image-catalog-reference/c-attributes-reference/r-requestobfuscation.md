---
description: 要求模糊化模式。 指定必須套用至有效要求的模糊化型別。
solution: Experience Manager
title: 要求模糊化
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: c330c8de-9539-442f-a52a-786f882873cf
TQID: 'https://experienceleague.adobe.com/IF7qVWoidj-WvoY-wR-D8uqkiTV3X44C7i4YzeyBbTI'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 66
ht-degree: 1%

---

# 要求模糊化{#requestobfuscation}

要求模糊化模式。 指定必須套用至有效要求的模糊化型別。

## 屬性 {#section-0819432615324e259f24717e16835427}

列舉。 設為0可停用請求模糊化，或設為1可選取base64編碼。 目前不支援其他模糊化方法。

## 預設 {#section-e7f49493d9a940acb4f7938df7cac44d}

如果未定義或空白，則繼承自`default::RequestObfuscation`。
