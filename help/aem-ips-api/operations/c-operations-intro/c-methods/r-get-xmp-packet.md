---
description: 檢索指XMP定資產的元資料包。
solution: Experience Manager
title: getXMPPacket
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: 76e595bd-e598-40e8-aba3-b270fcf4d800
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '69'
ht-degree: 23%

---

# getXMPPacket{#getxmppacket}

檢索指XMP定資產的元資料包。

語法

## 授權用戶類型 {#section-7cb9c26045214f01b1d6b6948b6c6a18}

* `IpsUser`
* `IpsAdmin`
* `IpsCompanyAdmin`
* `ImagePortalAdmin`
* `ImagePortalUser`
* `ImagePortalContrib`
* `ImagePortalContribUser`

## 參數 {#section-b4075df0e4414b00b961d978d5471db9}

**輸入(getXMPPacketParam**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 公司句柄 | `xsd:string` | 是 | 公司處理要返回的資料包(例如， `c|656`)。 |
| 資產句柄 | `xsd:string` | 是 | 應檢索包XMP的資產。 |

**輸出(getXMPPacketReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| 壓縮資料包 | `xsd:Base 64 binary` | 是 | [!DNL zlib-compressed] 包XMP。 |

## 範例 {#section-d681af49122e4ca9bcd04110a2e98e6f}

**請求**

```java
<ns:getXMPPacketParam>
   <ns:companyHandle>c|680</ns:companyHandle>
   <ns:assetHandle>a|918567</ns:assetHandle>
</ns:getXMPPacketParam>
```

**回答**

```java
<getXMPPacketReturn xmlns="http://www.scene7.com/IpsApi/xsd/2010-01-31">
   <compressedPacket>H4sIAAAAAAAAAAGqAVX+eNqNU9FumzAUfc9XWN5rwTbpUGNBpC3RtpdqU9NOe3XABTRsU9sM8vezMUUp6qQhhDg+
      955zfX2djXQUneCWgVG00tAxh6xUZ07dv19GEEwh9ncOP3kC/Lr/AQ5Kc/AxxlGBUwxSEpPtLUm3NyDBeIdIghISkTuKU3qLwfzA/QZkunymD8
      cvs5lDOayt7ShCwzDEwzZWukJkt9sh7ESSyEVE5iItGyNpPniJoHHkptBNZxslgcfsrHqbQ7jxTkG8q5VVplbdYiFNPO0tLpRAC4
      1IjNF1YlksGV2v26mkskC85YJLa1w8CfGLBH3SFZfFJYfbFXFgllKO+bn/ZpqrFv+xsS519WKO1mX9y/yoHppveRXrgWTlxX9qJk0ojHG9eaBP3
      PtKnNaNRNJ kq6lNC8bO5/sugbVa5/4Hnd05blc9y1zmGCCI0zcO50PyK40+q4LbWPt3IqGmykqnONnVgUUYNvsdfOH6wzN6C03OMd6zQb0KpSh
      /3LPyoIWfgNKX1Vz4i8rx5MSHHyX/D3L1+gMvRUL7NWE+sFH8+TvNxla7t+8xdjuhqNPERMBaoBAAA=
   </compressedPacket>
</getXMPPacketReturn>
```
