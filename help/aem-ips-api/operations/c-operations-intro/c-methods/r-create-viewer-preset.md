---
description: 建立預設檢視，以決定使用者可看見的內容。 檢視器可以是IPS中任何類型的。 預設檢視會在資產發佈時套用。
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Administrator
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
translation-type: tm+mt
source-git-commit: b4344397f82eb7d2d61020909f4acc7fddea210b
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 12%

---

# createViewerPreset{#createviewerpreset}

建立預設檢視，以決定使用者可看見的內容。 檢視器可以是IPS中任何類型的。 預設檢視會在資產發佈時套用。

語法

## 授權用戶類型{#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-aa6dc37e327541ebbfed7685cd8071ff}

**輸入(createViewerPresetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`companyHandle`*` | `xsd:string` | 是 | 包含檢視器預設集和資產的公司控制代碼。 |
| `*`folderHandle`*` | `xsd:string` | 是 | 包含資產的資料夾的控制代碼。 |
| `*`名稱`*` | `xsd:string` | 是 | 檢視器名稱。 |
| `*`類型`*` | `xsd:string` | 是 | 檢視器類型. |
| `*`configSettingArray`*` | `types:ConfigSettingArray` | 否 | 包含您要套用預設集之影像名稱、值和處理點的陣列。 |

**輸出(createViewerPresetReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`viewerPresetHandle`*` | `xsd:string` | 是 | 預設集的控制代碼給檢視器。 |

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
