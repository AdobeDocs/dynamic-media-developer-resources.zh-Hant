---
description: 建立可以具有多個文本和影像層的分層影像。
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '197'
ht-degree: 10%

---

# createTemplate{#createtemplate}

建立可以具有多個文本和影像層的分層影像。

`urlModifier`參數指定儲存在應用於URL上任何用戶提供的命令之前的映像伺服器目錄中的映像伺服器協定命令。 `urlPostApplyModifier`參數指定在任何URL命令之後應用的協定命令，這將覆蓋用戶提供的任何衝突設定。

## 授權的使用者類型 {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**輸入(createTemplateParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 範本所屬的公司。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 表示模板所在資料夾的資料夾句柄。 |
| `*`名稱`*` | `xsd:string` | 是 | 範本名稱。 |
| `*`類型`*` | `xsd:string` | 是 | 範本類型。 |
| `*`urlModifier`*` | `xsd:string` | 是 | 指定儲存在IS目錄中的Image Server命令，這些命令在URL上任何用戶提供的命令之前應用。 |
| `*`urlPostApplyModifier`*` | `xsd:string` | 否 | 指定在任何URL命令之後應用的協定命令，這將覆蓋任何衝突的用戶提供的設定。 |

**輸出(createTemplateParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`assetHandle`*` | `xsd:string` | 是 | 範本的控點。 |

## 範例 {#section-09adb4d2f0c944af875c4463a461f55d}

此代碼示例在由句柄指定的資料夾中建立模板，名稱為`APIcreateTemplate`、`urlModifier`和`urlPostApplyModifier`。 回應會將控點傳回至新建立的範本。

**請求**

```java
<createTemplateParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|21</companyHandle>
   <folderHandle>ApiTestCo/</folderHandle>
   <name>APIcreateTemplate</name>
   <type>Template</type>
   <urlModifier>url=Modifier</urlModifier>
   <urlPostApplyModifier>urlPostApply=Modifier</urlPostApplyModifier>
</createTemplateParam>
```

**回答**

```java
<createTemplateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|153393|2|2061</assetHandle>
</createTemplateReturn>
```
