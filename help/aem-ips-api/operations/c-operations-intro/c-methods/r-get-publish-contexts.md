---
description: getPublishContexts
solution: Experience Manager
title: getPublishContexts
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 7b26e659-71b9-40c4-9df4-94e78c3e4baf
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '85'
ht-degree: 24%

---

# getPublishContexts{#getpublishcontexts}

語法

## 授權用戶類型 {#section-1a3a50349b5640dd8e498ff9e9c37340}

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
>* 用戶必須具有讀權限才能返回資產。
>* 所有用戶都有權訪問共用公司。
>


## 參數 {#section-d08e2175d3f84774b55b91bc590b8b3f}

**輸入(getPublishContextsParam)**

<table id="table_4A505A067586464B99F8F68E3B1BE75E"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> 名稱 </th> 
   <th colname="col2" class="entry"> 類型 </th> 
   <th colname="col3" class="entry"> 必要 </th> 
   <th colname="col4" class="entry"> 說明 </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 公司句柄</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 把手交給公司。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 上下文類型</span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string</span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4">要返回的發佈上下文的類型。 包括： 
    <ul id="ul_21EDF8F0026E402EAE8226A0CADEE652">
     <li id="li_06DB502952D943198F16C06C59816268"><span class="codeph"> 影像服務</span></li>
     <li id="li_E67A42934E8F4689A148CE125F7372AE"><span class="codeph"> 影像呈現</span></li>
     <li id="li_3CB3A9C4E7AB4A71819567A9566E396C"><span class="codeph"> 視訊</span></li>
     <li id="li_27E3DB89B53B4B50B2231622A157A228"><span class="codeph"> 伺服器目錄</span></li>
    </ul></td> 
  </tr> 
 </tbody> 
</table>

**輸出(getPublishContextsReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| publishContextArray | 類型：PublishContextArray | 是 | 公司的發佈上下文陣列，如果需要，按上下文類型篩選。 |

## 範例 {#section-23fb7d6a15004b7eb4c3d3bcb37ceb04}

**請求**

```java
<getPublishContextsParam xmlns="http://www.scene7.com/IpsApi/xsd/2011-11-04">
  <companyHandle>c|301</companyHandle>
</getPublishContextsParam>
```

**回答**

```java
<getPublishContextsReturn xmlns="http://www.scene7.com/IpsApi/xsd">
  <publishContextArray>
    <items>
      <contextHandle>pc|3001</contextHandle>
      <contextName>ImageRendering</contextName>
      <contextType>ImageRendering</contextType>
    </items>
    <items>
      <contextHandle>pc|3002</contextHandle>
      <contextName>ImageServing</contextName>
      <contextType>ImageServing</contextType>
    </items>
    <items>
      <contextHandle>pc|3003</contextHandle>
      <contextName>ServerDirectory</contextName>
      <contextType>ServerDirectory</contextType>
    </items>
    <items>
      <contextHandle>pc|3004</contextHandle>
      <contextName>Video</contextName>
      <contextType>Video</contextType>
    </items>
  </publishContextArray>
</getPublishContextsReturn>
```
