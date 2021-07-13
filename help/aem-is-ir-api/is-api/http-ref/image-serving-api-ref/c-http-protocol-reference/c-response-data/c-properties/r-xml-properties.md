---
description: 如果將xml指定為響應格式，則回復資料將格式化為XML文檔，該文檔可由任何標準XML解析器分析。
solution: Experience Manager
title: XML屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '114'
ht-degree: 0%

---

# XML屬性{#xml-properties}

如果將xml指定為響應格式，則回復資料將格式化為XML文檔，該文檔可由任何標準XML解析器分析。

典型屬性響應文檔具有以下一般結構：

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

`<prop-group>`元素用作最外層的容器，用於分組屬性。 如果組名稱為，該名稱與Java/JavaScript對象名稱相對應。

>[!NOTE]
>
>可以為某些`req=`類型指定字元編碼。 有關詳細資訊，請參閱特定`req=`命令的說明。
