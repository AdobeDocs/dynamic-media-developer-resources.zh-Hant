---
description: 建立一個預設視圖，確定用戶可以看到的內容。 查看器可以是IPS中可用的任何類型。 發佈資產時應用預設視圖。
solution: Experience Manager
title: createViewerPreset
feature: Dynamic Media Classic,SDK/API,Viewer Presets
role: Developer,Admin
exl-id: b24536d9-df66-4c94-8467-6f46e66a1b36
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '158'
ht-degree: 13%

---

# createViewerPreset{#createviewerpreset}

建立一個預設視圖，確定用戶可以看到的內容。 查看器可以是IPS中可用的任何類型。 發佈資產時應用預設視圖。

語法

## 授權用戶類型 {#section-0b8b1322ebea4a7ea24d516e080b7367}

* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `ImagePortalAdmin`

## 參數 {#section-aa6dc37e327541ebbfed7685cd8071ff}

**輸入(createViewerPresetParam)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 包含查看器預設和資產的公司句柄。 |
| folderHandle | `xsd:string` | 是 | 包含資產的資料夾的句柄。 |
| name | `xsd:string` | 是 | 查看器名稱。 |
| type | `xsd:string` | 是 | 檢視器類型. |
| configSettingArray | `types:ConfigSettingArray` | 否 | 包含要應用預設的影像的名稱、值和句柄的陣列。 |

**輸出(createViewerPresetReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 查看器PresetHandle | `xsd:string` | 是 | 將預設的句柄提供給查看器。 |

## 範例 {#section-c88ea63536f3461cbe4677ba53f875dd}

此代碼示例建立視頻播放器預設。 響應將句柄返回到預設。

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
