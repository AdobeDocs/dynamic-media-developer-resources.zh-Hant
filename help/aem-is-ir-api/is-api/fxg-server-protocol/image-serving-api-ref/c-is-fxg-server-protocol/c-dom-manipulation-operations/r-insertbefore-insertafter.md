---
description: 在節點之前或之後設定XML。
seo-description: 在節點之前或之後設定XML。
seo-title: insertBefore,insertAfter
solution: Experience Manager
title: insertBefore,insertAfter
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 5ac0f675-333b-4f85-abe0-642cf96de425
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '62'
ht-degree: 3%

---


# insertBefore,insertAfter{#insertbefore-insertafter}

在節點之前或之後設定XML。

`insertBefore=<xml>, insertAfter=<xml>`

如果FXG節點元素已定義`s7:elementID`，我們可以使用此命令在該節點之前或之後添加XML片段。

## 範例 {#section-1fc8d4135ef94b60b838391e1568e70e}

如果我們有這樣的群組標籤：

`<Group visible="true" s7:elementID="inner_shape">`

然後:

`insertBefore.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

結果：

`<Rect height="75" rotation="0" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" width="75" x="74.354" y="182.762"><fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill></Rect><Group s7:elementID="inner_shape" visible="true">`

`insertAfter.inner_shape=<Rect x="74.354" y="182.762" width="75" height="75" s7:fillOverprint="false" s7:fillOverprintMode="true" visible="true" rotation="0"><fill><SolidColor color="%23ffffff" s7:cmykColor="%2300000000"/></fill></Rect>`

結果：

`<Group s7:elementID="inner_shape" visible="true"> <Rect ai:knockout="0" d:userLabel="Background" height="392.581" visible="true" width="319.953" x="0.75" y="0.75"> <fill><SolidColor color="#ffffff" s7:cmykColor="#00000000"/></fill> </Rect>`
