---
description: 如果將xml指定為回應格式，回覆資料會格式化為XML檔案，任何標準的XML剖析器都可以剖析該檔案。
solution: Experience Manager
title: XML屬性
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 84cae0cd-d13b-409e-bd65-71c7e973d4b8
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 0%

---

# XML屬性{#xml-properties}

如果將xml指定為回應格式，回覆資料會格式化為XML檔案，任何標準的XML剖析器都可以剖析該檔案。

典型的屬性回應檔案具有此一般結構：

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

`<prop-group>`元素會作為最外層的容器，並用於群組屬性。 如果群組已命名，則該名稱會對應至Java/JavaScript物件名稱。

>[!NOTE]
>
>可以為某些`req=`型別指定字元編碼。 如需詳細資訊，請參閱特定`req=`命令的描述。
