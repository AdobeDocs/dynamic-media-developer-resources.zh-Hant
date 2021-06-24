---
description: 擷取指定資產的XMP中繼資料封包。
solution: Experience Manager
title: getXMPPacket
feature: Dynamic Media Classic,SDK/API
role: Developer,Administrator
exl-id: 76e595bd-e598-40e8-aba3-b270fcf4d800
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '74'
ht-degree: 21%

---

# getXMPPacket{#getxmppacket}

擷取指定資產的XMP中繼資料封包。

語法

## 授權的使用者類型 {#section-7cb9c26045214f01b1d6b6948b6c6a18}

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
| `*`companyHandle`*` | `xsd:string` | 是 | 公司使用您要傳回的資料包處理（例如`c|656`）。 |
| `*`assetHandle`*` | `xsd:string` | 是 | 應擷取XMP封包的資產。 |

**輸出(getXMPPacketReturn)**

| 名稱 | 類型 | 必要 | 說明 |
|---|---|---|---|
| `*`compressedPacket`*` | `xsd:Base 64 binary` | 是 | [!DNL zlib-compressed] XMP封包。 |

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
