---
description: 建立可以包含多個文字和影像圖層的圖層影像。
solution: Experience Manager
title: createTemplate
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 228b4228-8c42-4e42-9fb1-d6aea61b9c4a
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '190'
ht-degree: 10%

---

# createTemplate{#createtemplate}

建立可以包含多個文字和影像圖層的圖層影像。

`urlModifier`引數會指定儲存在影像伺服器目錄中的影像伺服器通訊協定命令，這些命令會先於使用者在URL上提供的任何命令套用。 `urlPostApplyModifier`引數指定在任何URL命令之後套用的通訊協定命令，這會覆寫任何衝突的使用者提供的設定。

## 授權的使用者型別 {#section-9fb615d8e75f452eab2893cc3decfbe6}

* `IpsUser`
* `IpsAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-f54870f07d1d48fb8749ba7a4b43b6cb}

**輸入(createTemplateParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 範本所屬的公司。 |
| folderHandle | `xsd:string` | 是 | 代表範本所在資料夾的資料夾控制代碼。 |
| name | `xsd:string` | 是 | 範本名稱。 |
| type | `xsd:string` | 是 | 範本型別。 |
| urlModifier | `xsd:string` | 是 | 指定儲存在IS目錄中的「影像伺服器」命令，這些命令會先於使用者在URL上提供的任何命令套用。 |
| urlPostApplyModifier | `xsd:string` | 否 | 指定在任何URL命令之後套用的通訊協定命令，這會覆寫任何衝突的使用者提供的設定。 |

**輸出(createTemplateParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| assetHandle | `xsd:string` | 是 | 範本的控制代碼。 |

## 範例 {#section-09adb4d2f0c944af875c4463a461f55d}

這個程式碼範例會在控制代碼指定的資料夾中建立範本，名稱為`APIcreateTemplate`、`urlModifier`和`urlPostApplyModifier`。 回應會將控制代碼傳回至新建立的範本。

**要求**

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

**回應**

```java
<createTemplateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <assetHandle>a|153393|2|2061</assetHandle>
</createTemplateReturn>
```
