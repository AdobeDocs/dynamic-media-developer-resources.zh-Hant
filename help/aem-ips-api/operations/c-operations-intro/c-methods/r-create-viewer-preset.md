---
description: 建立預設集檢視，決定使用者可看見的內容。 檢視器可以是IPS中可用的任何類型。 資產發佈時，會套用預設集檢視。
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic, SDK/API，檢視器預設集
role: Developer,Administrator
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 12%

---

# createViewerPreset{#createviewerpreset}

建立預設集檢視，決定使用者可看見的內容。 檢視器可以是IPS中可用的任何類型。 資產發佈時，會套用預設集檢視。

語法

## 授權的使用者類型 {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-aa6dc37e327541ebbfed7685cd8071ff}

**輸入(createViewerPresetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含檢視器預設集和資產的公司控點。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 包含資產之資料夾的控點。 |
| `*`名稱`*` | `xsd:string` | 是 | 檢視器名稱。 |
| `*`類型`*` | `xsd:string` | 是 | 檢視器類型. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | 否 | 陣列，包含要應用預設集的影像的名稱、值和句柄。 |

**輸出(createViewerPresetReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`viewerPresetHandle`*` | `xsd:string` | 是 | 對檢視器處理預設集。 |

## 範例 {#section-c88ea63536f3461cbe4677ba53f875dd}

此程式碼範例會建立視訊播放器預設集。 回應會傳回控制代碼至預設集。

```java
<createViewerPresetParam xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <companyHandle>c|0</companyHandle>
   <folderHandle>Scene7SharedAssets/</folderHandle>
   <name>eVideo4</name>
   <type>VideoPlayer</type>
   <configSettingArray>
      <items>
         <name>Video Bit Rate</name>
         <value>393334.6508779093</value>
      </items>
      <items>
         <name>Audio Sample Rate</name>
         <value>44100</value>
      </items>
      ...
      <items>
         <name>vidPaneWidth</name>
         <value>0</value>
      </items>
   </configSettingArray>
</createViewerPresetParam>
```

**回答**

```java
<createViewerPresetReturn xmlns="http://www.scene7.com/IpsApi/xsd/2008-01-15">
   <viewerPresetHandle>a|151760|40|151760</viewerPresetHandle>
</createViewerPresetReturn>
```
