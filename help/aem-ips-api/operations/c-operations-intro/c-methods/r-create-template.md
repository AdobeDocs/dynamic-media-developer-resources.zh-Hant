---
description: 建立可具有多個文本和影像圖層的分層影像。
solution: Experience Manager
title: 建立模板
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '192'
ht-degree: 10%

---

# 建立模板{#createtemplate}

建立可具有多個文本和影像圖層的分層影像。

的 `urlModifier` 參數指定在URL上任何用戶提供的命令之前應用的Image Server目錄中儲存的Image Server協定命令。 的 `urlPostApplyModifier` 參數指定在任何URL命令後應用的協定命令，這將覆蓋任何衝突的用戶提供的設定。

## 授權用戶類型 {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**輸入(createTemplateParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 模板所屬的公司。 |
| folderHandle | `xsd:string` | 是 | 表示模板所在資料夾的資料夾句柄。 |
| 名稱 | `xsd:string` | 是 | 模板名稱。 |
| type | `xsd:string` | 是 | 模板類型。 |
| url修飾符 | `xsd:string` | 是 | 指定在IS目錄中儲存的在URL上任何用戶提供的命令之前應用的影像伺服器命令。 |
| urlPostApplyModifier | `xsd:string` | 否 | 指定在任何URL命令後應用的協定命令，這將覆蓋任何衝突的用戶提供的設定。 |

**輸出(createTemplateParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 資產句柄 | `xsd:string` | 是 | 模板的句柄。 |

## 範例 {#section-09adb4d2f0c944af875c4463a461f55d}

此代碼示例在句柄指定的資料夾中建立一個模板，名稱為 `APIcreateTemplate`的 `urlModifier`的 `urlPostApplyModifier`。 響應將句柄返回到新建立的模板。

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
