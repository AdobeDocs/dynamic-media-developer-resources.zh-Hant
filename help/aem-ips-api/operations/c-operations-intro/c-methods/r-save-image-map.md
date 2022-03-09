---
description: 建立新影像映射或編輯現有映射。
solution: Experience Manager
title: saveImageMap
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 91e40549-9b26-41f2-a3ab-7e9bec8f9ba7
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '253'
ht-degree: 16%

---

# saveImageMap{#saveimagemap}

建立新影像映射或編輯現有映射。

語法

## 授權用戶類型 {#section-9ef194a67b3546fb82ed7bb294bc2714}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalContrib`
* `ImagePortalContribUser`

>[!NOTE]
>
>用戶必須具有對資產的讀寫權限。

## 參數 {#section-64f7f5fd8f954fba9fa30eeee556863a}

**輸入(saveImageMapParam)**

<table id="table_49649036F46941D2B1F28515674E533B"> 
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
   <td colname="col1"> <span class="codeph"> <span class="varname"> 公司句柄 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:string </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 包含要保存的影像映射的公司的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 資產句柄 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 影像映射所屬的影像資產的句柄。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> imageMapHandle </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串 </span> </td> 
   <td colname="col3"> 否 </td> 
   <td colname="col4"> 影像映射的句柄。 如果為NULL，則建立影像映射。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 名稱 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 建立或保存的影像映射的名稱。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 形狀類型 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 選擇區域形狀。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 區域 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 定義區域的以逗號分隔的點清單。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 動作 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd：字串 </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> <p>的 <span class="codeph"> href </span> 與IPS介面中指定的影像映射關聯的值。 </p> <p>獲取 <span class="codeph"> href </span> 值，按一下IPS介面中的影像，將URL複製並貼上到此元素中，然後將IPS URL格式化為正確的URL。 比如說， <span class="codeph"> &amp; </span> 變成 <span class="codeph"> &amp;amp; </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 位置 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:int </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"> 影像映射清單（Z軸）中的順序。 </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> 啟用 </span> </span> </td> 
   <td colname="col2"> <span class="codeph"> xsd:boolean </span> </td> 
   <td colname="col3"> 是 </td> 
   <td colname="col4"></td> 
  </tr> 
 </tbody> 
</table>

**輸出(saveImageMapReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| imageMapHandle | `xsd:string` | 是 | 新影像映射或已編輯影像映射的句柄。 |

## 範例 {#section-fdac488b640f427c8aa3d549c5032851}

此代碼示例為資產建立新的影像映射。 它使用由區域形狀字串常數確定的形狀類型，並將句柄返回到新影像映射。

**請求**

```
<saveImageMapParam xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <companyHandle>47</companyHandle> 
   <assetHandle>24266|1|17062</assetHandle> 
   <name>My Image Map</name> 
   <shapeType>Rectangle</shapeType> 
   <region>0,10,0,10</region> 
   <action>http://s7oslo.macromedia.com/scene7/browse/MoreInfo.jsp?assetID=24266&amp; 
   iRow=1&iRows=1&amp;strSearchType=image</action> 
   <position>0</position> 
</saveImageMapParam>
```

**回答**

```
<saveImageMapReturn xmlns="http://www.scene7.com/IpsApi/xsd"> 
   <imageMapHandle>34191|8|554</imageMapHandle> 
</saveImageMapReturn>
```
