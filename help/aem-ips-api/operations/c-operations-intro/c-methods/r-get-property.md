---
description: 取得與影像入口網站相關之系統屬性的字串值。
solution: Experience Manager
title: getProperty
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 2297b785-28c7-49c6-8891-00986f35ea88
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '132'
ht-degree: 10%

---

# getProperty{#getproperty}

取得與影像入口網站相關之系統屬性的字串值。

支援的系統屬性包括：

* `IpsVersion`： IPS版本號碼。
* `IpsImageServerUrl`： IPS影像伺服器的完整外部URL首碼。
* `VideoRootUrl`
* `swfRootUrl`
* `SvgRenderRootUrl`：轉譯SVG資產的URL首碼。
* `SvgRenderEnabled`：如果`SvgRenderRootUrl`可以轉譯SVG資產，則為True。

* `UploadPostMaxFileSize`：上傳[!DNL POST]中允許的檔案資料大小上限（位元組）。 系統會拒絕大於最大限制的檔案。

## 授權的使用者型別 {#section-2cd36bbd46ed414b8753569d5895530e}

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
| name | `xsd:string` | 是 | 要取得的屬性名稱。 |

**輸出(getPropertyReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 價值 | `xsd:string` | 是 | 屬性值。 |

## 範例 {#section-3f80a78dd60c404181b34d3a912d7a36}

此程式碼範例使用IPS屬性字串常數傳回特定值。 在此範例中，IPS屬性是IPS伺服器的版本。

**要求**

```java
<ns1:getPropertyParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:name>IpsVersion</ns1:name>
</ns1:getPropertyParam>
```

**回應**

```java
<getPropertyReturn xmlns="http://www.scene7.com/IpsApi/xsd">
   <value>3.8.0</value>
</getPropertyReturn>
```
