---
description: 設定或更新一或多個資產的發佈狀態。 您可以為公司中的每個發佈上下文設定個別的發佈狀態。
solution: Experience Manager
title: setAssetsContextState
feature: Dynamic Media經典，SDK/API，資產管理
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 10%

---


# setAssetsContextState{#setassetscontextstate}

設定或更新一或多個資產的發佈狀態。 您可以為公司中的每個發佈上下文設定個別的發佈狀態。

## 授權用戶類型{#section-815eb031f85143278c1560c18c5e3431}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>使用者必須擁有讀取存取權，才能傳回資產。

## 參數 {#section-009b9006de8e4c16ad657c47f28ace9f}

**輸入(setAssetsContextStateParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 為公司負責。 |
| `*`assetsContextHandle`*` | `types:AssetsContextStateUpdateArray` | 是 | 一系列資產及其新的發佈狀態。 |

**輸出(setAssetsContexStateReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`successCount`*` | `xsd:int` | 是 | 成功變更的資產數。 |
| `*`warningCount`*` | `xsd:int` | 是 | 嘗試修改資產時產生的警告數。 |
| `*`errorCount`*` | `xsd:int` | 是 | 嘗試修改資產時產生的錯誤數。 |
| `*`warningDetailArray`*` | `types:AssetOperationFaultArray` | 否 | 資產嘗試修改資產時產生的錯誤陣列。 |

## 範例 {#section-283a073f3cb14bcda5abed863c538aa4}

此程式碼範例會使用`NotMarkedForPublish`設定資產的發佈狀態。

**請求**

```java
<setAssetsContextStateParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
  <assetsContextStateUpdateArray>
    <items>
      <assetHandle>a|27007</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
    <items>
      <assetHandle>a|27008</assetHandle>
      <contextStateUpdateArray>
        <items>
          <contextHandle>pc|3001</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3002</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3003</contextHandle>
          <publishState>NotMarkedForPublish</publishState>
        </items>
        <items>
          <contextHandle>pc|3004</contextHandle>
          <publishState>MarkedForPublish</publishState>
        </items>
      </contextStateUpdateArray>
    </items>
  </assetsContextStateUpdateArray>
</setAssetsContextStateParam>
```

**回答**

```java
<setAssetsContextStateReturn xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04-beta">
  <successCount>8</successCount>
  <warningCount>0</warningCount>
  <errorCount>0</errorCount>
</setAssetsContextStateReturn>
```

