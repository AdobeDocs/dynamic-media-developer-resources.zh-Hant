---
description: 取得與指定資產相關聯的資產，以及其關係的詳細資訊。
seo-description: 取得與指定資產相關聯的資產，以及其關係的詳細資訊。
seo-title: getAssociatedAssets
solution: Experience Manager
title: getAssociatedAssets
topic: Scene7 Image Production System API
uuid: 70c2f8aa-9104-42b0-b85b-14f90f1ead52
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# getAssociatedAssets{#getassociatedassets}

取得與指定資產相關聯的資產，以及其關係的詳細資訊。

語法

## 授權使用者類型 {#section-453cc706400345778713cda249bfac16}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `TrialSiteAdmin`
* `TrialSiteUser`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-d11d0dab59e94e89b466123a0ebfa82e}

**輸入(getAssociatedAssetsParam)**

<table id="table_DBB97A6507EB48479FFFD2184FF8F07C"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名稱 </p> </th> 
   <th colname="col2" class="entry"> <p>類型 </p> </th> 
   <th colname="col3" class="entry"> <p>必要 </p> </th> 
   <th colname="col4" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 公 <span class="varname"> 司控制</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>對擁有資產的公司進行處理。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> 資 <span class="varname"> 產控制代碼</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> xsd:string</span> </p> </td> 
   <td colname="col3"> <p>是 </p> </td> 
   <td colname="col4"> <p>資產控制代碼。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> <span class="varname"> responseFieldArray</span></span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：StringArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>所需的回應欄位陣列。 請參閱簡介中的response- FieldArray/excludeFieldArray。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p><span class="codeph"> excludeFieldArray <span class="varname"> (排除欄位陣列</span> ) </span> </p> </td> 
   <td colname="col2"> <p><span class="codeph"> 類型：StringArray</span> </p> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>已排除的響應欄位的陣列。 請參閱簡介中的response- FieldArray/excludeFieldArray。 </p> </td> 
  </tr> 
 </tbody> 
</table>

**輸出(getAssociatedAssetsReturn)**

<table id="table_B894B4B6EFA24359A0250A8A4523EA8D"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>名稱 </p> </th> 
   <th colname="col2" class="entry"> <p>類型 </p> </th> 
   <th colname="col3" class="entry"> <p>必要 </p> </th> 
   <th colname="col4" class="entry"> <p>說明 </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 容 <span class="varname"> 器陣列</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>包含指定資產的集合和範本資產陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> memberArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>指定集合或範本資產所包含的資產陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> layerReferenceArray <span class="varname"> (圖層參考陣列</span> ) </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>圖層或範本URL中參考的資產陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> ownerArray <span class="varname"></span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>擁有指定資產的資產陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> 衍 <span class="varname"> 生陣列</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：AssetArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>用來產生指定資產的資產陣列。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> generatorArray <span class="varname"> (產生器陣列</span> ) </span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>generatorArray <span class="codeph"> 會列出</span> 此資產的建立方式。 例如，如果 <span class="codeph"> assetHandler</span> 是PDF的影像頁面，則會包含PDF處理器工具並參考PdfFile資產。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> generatedArray</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：GenerationInfoArray</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>產生的 <span class="codeph"> 陣列</span> ，會反轉此資產的建立方式。 例如，如果 <span class="codeph"> 是PdfFile資產</span> ，則產生的Array可包含從此 <span class="codeph"> assetHandler</span> 產生的影像清單。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <span class="codeph"> <span class="varname"> thumbAsset</span></span> </td> 
   <td colname="col2"> <span class="codeph"> 類型：資產</span> </td> 
   <td colname="col3"> <p>否 </p> </td> 
   <td colname="col4"> <p>與請求資產相關聯的拇指資產資訊。 如果未指派拇指資產，則回應中會省略欄位。 </p> </td> 
  </tr> 
 </tbody> 
</table>

您可以使用參 `responseFieldArray` 數或 `excludeFieldArray` 限制回應大小。 尤其是，傳回 `GenerationInfo` 或預設的項 `generatorArray` 目， `generatedArray` 會同時包含原始和產生的資產記錄。 對於PDF資產類型，此行為會在回應中產生多份不想要的「原始人」PDF資產記錄。 您可以透過新增至來消除此 `generatedArray/items/originator` 問題 `excludeFieldArray`。 或者，您可以指定要包含在中的明確回應欄位清單 `responseFieldArray`。

## 範例 {#section-8946ea4b9cb94912a8408249c897f192}

以下基本範例是對從PDF擷取之影像產生器控制代碼的要求。 它包含一 `containerArray` 個長度的項目，包含PDF `assetHandle` 的項目。

**請求**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|197</beta:assetHandle>
         <beta:responseFieldArray>
            <beta:items>containerArray/items/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**回答**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <containerArray>
            <items>
               <assetHandle>a|207</assetHandle>
            </items>
         </containerArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

上述範例的反面是：

**請求**

```java
<soap:Envelope xmlns:soap="http://www.w3.org/2003/05/soap-envelope" xmlns:beta="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
   <soap:Body>
      <beta:getAssociatedAssetsParam>
         <beta:companyHandle>c|11</beta:companyHandle>
         <beta:assetHandle>a|177</beta:assetHandle>
        <beta:responseFieldArray>
           <beta:items>generatedArray/items/originator/assetHandle</beta:items>
         </beta:responseFieldArray>
      </beta:getAssociatedAssetsParam>
   </soap:Body>
</soap:Envelope>
```

**回答**

```java
<soapenv:Envelope xmlns:soapenv="http://www.w3.org/2003/05/soap-envelope">
   <soapenv:Body>
      <getAssociatedAssetsReturn xmlns="http://www.scene7.com/IpsApi/xsd/2013-08-29-beta">
         <generatedArray>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
            <items>
               <originator>
                  <assetHandle>a|177</assetHandle>
               </originator>
            </items>
         </generatedArray>
      </getAssociatedAssetsReturn>
   </soapenv:Body>
</soapenv:Envelope>
```

在下一個範例中，群組會新增至具有的公司 `groupHandleArray`。 此範例僅使用一個群組。

**請求**

```java
<ns1:addGroupMembershipParam xmlns:ns1="http://www.scene7.com/IpsApi/xsd">
   <ns1:companyHandle>47</ns1:companyHandle>
   <ns1:groupHandleArray><ns1:items>225</ns1:items></ns1:groupHandleArray>
</ns1:addGroupMembershipParam>
```

**回答**

無。
