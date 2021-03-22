---
description: 如果將xml指定為響應格式，則將回覆資料格式化為XML文檔，該文檔可由任何標準XML解析器解析。
seo-description: 如果將xml指定為響應格式，則將回覆資料格式化為XML文檔，該文檔可由任何標準XML解析器解析。
seo-title: XML屬性
solution: Experience Manager
title: XML屬性
uuid: 9d169ad2-e466-4ab3-8900-ea9c6125edad
feature: Dynamic Media經典，SDK/API
role: 開發人員，商業從業人員
translation-type: tm+mt
source-git-commit: 469d1a5c43a972116a8a2efb0de5708800130a99
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---


# XML屬性{#xml-properties}

如果將xml指定為響應格式，則將回覆資料格式化為XML文檔，該文檔可由任何標準XML解析器解析。

典型的屬性響應文檔具有以下一般結構：

```
<?xml version="1.0" encoding="UTF-8" ?>
<prop-group>
   <prop-group name="
<varname>
  objectName
</varname>">
       <property name="
<varname>
  propertyName
</varname>" value="
<varname>
  propertyValue
</varname>" />
       ...
    </prop-group>
 ...
</prop-group>
```

`<prop-group>`元素用作最外層的容器，並用於分組屬性。 如果組被命名，則名稱與Java/JavaScript物件名稱相對應。

>[!NOTE]
>
>某些`req=`類型可以指定字元編碼。 有關詳細資訊，請參閱特定`req=`命令的說明。

