---
description: 如果指定文字做為回應格式，回覆資料的格式會設定為Java屬性以供讀取。
solution: Experience Manager
title: 文字(Java)屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 46f5dbc8-fbdc-4204-a6a0-60f34378c3e1
TQID: 'https://experienceleague.adobe.com/WNIuNvCPLdbeweHB5gkcFfeZu2WDDUk53us6SHtmO-A'
product_v2:
  - id: fd1f54a9-f50c-467d-8956-cebbaf4f3eb8
feature_v2:
  - id: a01bfd36-4ab8-4bf8-9dc0-5b45b890552e
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: 2ff64206b7448a1a122696facd2669be68b6b9ff
workflow-type: tm+mt
source-wordcount: 100
ht-degree: 0%

---

# 文字(Java)屬性{#text-java-properties}

如果指定文字做為回應格式，回覆資料的格式會設定為Java屬性以供讀取。

典型的文字屬性回應具有此一般結構：

```
#S7Z OK
#
<varname>
  timeStamp
</varname>
<varname>
  objectName.propertyName
</varname>=
<varname>
  propertyValue
</varname>
...
```

*`propertyValue`*&#x200B;可能為空白。 每行開頭和結尾以及=分隔符號前後的空白字元為選用。 單引號或雙引號可用來將字串值括住，但並非必要。

字串值可包含JAVA樣式的逸出字元，例如`\n`、`\t`、`\:`或`\\`。
