---
description: getPhotoshopPath操作返回的影像位置座標。
solution: Experience Manager
title: PerspectiveQuad
feature: Dynamic Media經典，SDK/API
role: 開發人員、管理員
translation-type: tm+mt
source-git-commit: 052bfcbcf1bd4ccf60afa7e3325bf58dd07cba85
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 17%

---


# PerspectiveQuad{#perspectivequad}

getPhotoshopPath操作返回的影像位置座標。

語法

## 參數 {#section-59792c446366456d90de7f5875bad1b0}

| 名稱 | 類型 | 說明 |
|---|---|---|
| `*`x0`*` | `xsd:double` | 左上x軸坐標。 |
| `*`y0`*` | `xsd:double` | 左上Y軸坐標。 |
| `*`x1`*` | `xsd:double` | 右上x軸坐標。 |
| `*`y1`*` | `xsd:double` | 右上Y軸坐標。 |
| `*`x2`*` | `xsd:double` | 右下x軸坐標。 |
| `*`y2`*` | `xsd:double` | 右下Y軸坐標。 |
| `*`x3`*` | `xsd:double` | 左下x軸共軸。 |
| `*`y3`*` | `xsd:double` | 左下Y軸坐標。 |

## 範例 {#section-19ed4409ff3a41c9b52a9c9424612927}

`PerspectiveQuad`類型會依下列順序傳回資料：

```
<complexType name="PerspectiveQuad">
        <sequence>
            <element name="x0" type="xsd:double"/>
            <element name="y0" type="xsd:double"/>
            <element name="x1" type="xsd:double"/>
            <element name="y1" type="xsd:double"/>
            <element name="x2" type="xsd:double"/>
            <element name="y2" type="xsd:double"/>
            <element name="x3" type="xsd:double"/>
            <element name="y3" type="xsd:double"/>
        </sequence>
```

>[!MORELIKETHIS]
>
>* [getPhotoshopPath](../../operations/c-operations-intro/c-methods/r-get-photoshop-path.md#reference-545f902f84194951ac04e947fdc803b9)

