---
description: 如果將xml指定為響應格式，則將回覆資料格式化為XML文檔，該文檔可由任何標準XML解析器解析。
solution: Experience Manager
title: XML屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '117'
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

