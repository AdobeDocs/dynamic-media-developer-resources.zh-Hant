---
title: 暈映
description: 暈映是使用Dynamic Media Image Authoring編寫的影像，以搭配影像演算使用。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 5e1be99c-58c0-4e3c-bc57-7be5fa25ccef
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '622'
ht-degree: 0%

---

# 暈映{#vignettes}

暈映是使用Dynamic Media Image Authoring編寫的影像，以搭配影像演算使用。

IR支援兩種基本型別的暈映： *2D* 和 *三維*. 房間場景通常是3D暈映，可以呈現反射，而大多數其他場景，例如服裝或室內裝飾，通常是沒有反射演算能力的2D暈映。

暈映包含 *檢視* 和階層 *物件*.

檢視是主要影像、共用照明地圖、共用反射地圖以及與整個影像關聯的其他資料的容器。

物件階層包括 *物件群組*， *標準物件*、和 *重疊物件*.

每個標準物件都控制檢視影像的某個區域（以灰階定義） *遮色片*. 標準物件的遮色片從不重疊。 標準物件無法直接隱藏，但可能被重疊物件部分或完全覆蓋。 一般暈映中的大部分或所有物件都是標準物件。

重疊檢視影像上方的物件圖層。 重疊的順序是由指定給物件的z值所定義。 當場景的某些部分必須動態顯示或隱藏時，重疊物件很有用。

支援幾種物件型別（標準和重疊），每種型別都有其各自不同的用途：

* **平面物件** （3D暈映）和 **平面物件** （在2D暈映中）接受可重複的材質材質。 它們通常用於地板、檯面和其他只需要透視對映的平坦曲面。
* **Flowline物件** 平滑形狀的彎曲表面（例如裝飾物）有時也用於服裝物件。 它們可同時用於2D和3D暈映，而且如果完全製作，可以參與反射演算。
* **不可紋理的物件** 僅允許顏色變更。 2D和3D暈映均允許使用。 它們或是原本就不可紋理，或是設定了特殊「無紋理」旗標的平面或流程線物件。 此方法在3D暈映中很有用，可讓物件參與反射彩現，即使物件只接受純色材質。
* **草繪物件** 最適合用於具有褶皺和皺紋的布料物件，例如服飾專案。 如同流程線物件，它們可以用於2D和3D暈映，不過在3D暈映中的應用是有限的。
* **壁物件** 類似於平面物件，僅支援3D暈映。 它們有特殊的版面配置資訊，可套用兩種不同的壁裝飾（上層和下層）和最多三個壁框線材料。 如果製作得當，套用至牆壁的材料就能在相鄰牆壁之間準確且順暢地流動，適用於逼真的壁紙/牆壁邊框應用程式。 壁物件不支援紋理旋轉。
* **封包物件** 僅允許在3D暈映中使用。 它們用於編寫具有複雜佈局要求的廚房和浴室櫥櫃。 封包物件接受可重複的紋理並特別製作 *封包樣式檔案* 包含可調整大小的封包面板影像。

除了基本物件型別之外，還支援兩種特殊型別的重疊物件：

* **靜態重疊物件** 是不接受材料的物件。 2D和3D暈映均允許使用。 它們適用於室內場景中的卸除式配件、可轉譯重疊物件後的陰影，以及類似的應用程式。
* **視窗涵蓋框架物件** 提供套用視窗覆蓋樣式檔案的位置資訊，這些檔案是獨立於暈映編寫的，可以在暈映之間共用。

物件會收集到 *物件群組*，類似於檔案系統。 群組通常是以它們所代表的實體物件結構為基礎（例如，「所有檔案櫃」群組可能包含「基本檔案櫃」和「壁檔案櫃」）。 允許任何數量的群組層級。 群組支援將材質套用到多個類似物件。

* [場景座標](c-ir-scene-coordinates.md)
* [材質解析度](c-ir-material-resolution.md)
