---
description: 獲取與Image Portal相關的系統屬性的字串值。
seo-description: 獲取與Image Portal相關的系統屬性的字串值。
seo-title: getProperty
solution: Experience Manager
title: getProperty
topic: Scene7 Image Production System API
uuid: 38ea08a6-c948-4a01-bc9a-d1609197224e
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 9%

---


# getProperty{#getproperty}

獲取與Image Portal相關的系統屬性的字串值。

支援的系統屬性包括：

* `IpsVersion`:IPS版本號。
* `IpsImageServerUrl`:IPS Image Server的完整外部URL前置詞。
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`:用於轉譯SVG資產的URL首碼。
* `SvgRenderEnabled`:如果SVG資產可由轉譯，則為 `SvgRenderRootUrl`true。

* `UploadPostMaxFileSize`:上傳中允許的檔案資料大小上限（以位元組為單位） [!DNL POST]。系統拒絕大於最大限制的檔案。

## 授權用戶類型{#section-2cd36bbd46ed414b8753569d5895530e}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-e3d389d183b244c2a5ef39c0ec331b5e}

**輸入(getPropertyParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`名稱`*` | `xsd:string` | 是 | 要獲取的屬性的名稱。 |

**輸出(getPropertyReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| ` *`值`*` | `xsd:string` | 是 | 屬性值。 |

## 範例 {#section-3f80a78dd60c404181b34d3a912d7a36}

此代碼示例使用IPS屬性字串常數來返回特定值。 在此示例中，IPS屬性是IPS伺服器的版本。

**請求**

```java
<ns1:getPropertyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:name>IpsVersion</ns1:name>
</ns1:getPropertyParam>
```

**回答**

```java
<getPropertyReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <value>3.8.0</value>
</getPropertyReturn>
```

