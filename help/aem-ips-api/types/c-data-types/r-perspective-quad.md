---
description: getPhotoshopPath操作返回的影像位置坐標。
solution: Experience Manager
title: 透視四
feature: Dynamic Media Classic,SDK/API
role: Developer,Admin
exl-id: dae44565-083d-47f5-8a08-2567590315a4
source-git-commit: 77c88d5fe20e048f6fad2bb23cb1abe090793acf
workflow-type: tm+mt
source-wordcount: '72'
ht-degree: 19%

---

# 透視四{#perspectivequad}

getPhotoshopPath操作返回的影像位置坐標。

語法

## 參數 {#section-59792c446366456d90de7f5875bad1b0}

| 名稱 | 類型 | 說明 |
|---|---|---|
| x0 | `xsd:double` | 左上X軸坐標。 |
| 0 | `xsd:double` | 左上Y軸坐標。 |
| x1 | `xsd:double` | 右上X軸坐標。 |
| y1 | `xsd:double` | 右上Y軸坐標。 |
| x2 | `xsd:double` | 右下X軸坐標。 |
| y2 | `xsd:double` | 右下Y軸坐標。 |
| x3 | `xsd:double` | 左下X軸坐標。 |
| y3 | `xsd:double` | 左下Y軸坐標。 |

## 範例 {#section-19ed4409ff3a41c9b52a9c9424612927}

的 `PerspectiveQuad` 類型按此順序返回資料：

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

