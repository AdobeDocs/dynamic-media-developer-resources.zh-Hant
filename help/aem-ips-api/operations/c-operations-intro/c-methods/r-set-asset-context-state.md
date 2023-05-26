---
description: 設定或更新一或多個資產的發佈狀態。 您可以為公司中的每個發佈內容設定個別的發佈狀態。
solution: Experience Manager
title: setAssetsContextState
feature: Dynamic Media Classic,SDK/API,Asset Management
role: Developer,Admin
exl-id: 28d0a67b-3e36-43fc-800d-17c841dca3a0
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 11%

---

# setAssetsContextState{#setassetscontextstate}

設定或更新一或多個資產的發佈狀態。 您可以為公司中的每個發佈內容設定個別的發佈狀態。

## 授權的使用者型別 {#section-815eb031f85143278c1560c18c5e3431}

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
>使用者必須擁有讀取存取權才能傳回資產。

## 參數 {#section-009b9006de8e4c16ad657c47f28ace9f}

**輸入(setAssetsContextStateParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| companyHandle | `xsd:string` | 是 | 處理公司。 |
| assetsContextHandle | `types:AssetsContextStateUpdateArray` | 是 | 一系列資產及其新發佈狀態。 |

**輸出(setAssetsContexStateReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| successCount | `xsd:int` | 是 | 已成功變更的資產數量。 |
| warningCount | `xsd:int` | 是 | 作業嘗試修改資產時產生的警告數目。 |
| errororcount | `xsd:int` | 是 | 作業嘗試修改資產時產生的錯誤數。 |
| warningDetailArray | `types:AssetOperationFaultArray` | 否 | 作業嘗試修改資產時資產產生的錯誤陣列。 |

## 範例 {#section-283a073f3cb14bcda5abed863c538aa4}

此程式碼範例使用來設定資產的發佈狀態 `NotMarkedForPublish`.

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
