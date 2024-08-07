---
title: 暈映
description: 暈映是指以Dynamic Media Image Authoring製作而成的影像，可與Image Rendering搭配使用。
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

暈映是指以Dynamic Media Image Authoring製作而成的影像，可與Image Rendering搭配使用。

IR支援兩種基本型別的暈映： *2D*&#x200B;和&#x200B;*3D*。 房間場景通常是3D暈映，可以呈現反射，而大多數其他場景，例如服裝或室內裝飾，通常是沒有反射彩現功能的2D暈映。

暈映包含&#x200B;*檢視*&#x200B;和&#x200B;*物件*&#x200B;的階層。

檢視是主要影像、共用照明地圖、共用反射地圖以及與整個影像關聯的其他資料的容器。

物件階層包含&#x200B;*物件群組*、*標準物件*&#x200B;和&#x200B;*重疊物件*。

每個標準物件控制檢視影像的區域，以灰階&#x200B;*遮色片*&#x200B;定義。 標準物件的遮色片從不重疊。 標準物件無法直接隱藏，但可能會部分或完全由重疊物件覆蓋。 一般暈映中的大部分或所有物件都是標準物件。

重疊物件圖層於檢視影像上方，彼此重疊。 重疊的順序是由指定給物件的z值所定義。 重疊物件在必須動態顯示或隱藏場景部分時非常有用。

支援幾種物件型別（標準和重疊），每種型別都有其各自不同的用途：

* **平面物件** （3D暈映）和&#x200B;**平面物件** （2D暈映）接受可重複的紋理材料。 它們通常用於地板、檯面和其他只需要透視對映的平坦曲面。
* **Flowline物件**&#x200B;會對映平滑形狀的曲面，例如裝飾品，偶爾也會用於服裝物件。 它們可用於2D和3D暈映，如果完全製作，則參與反射彩現。
* **不可紋理的物件**&#x200B;只允許色彩變更。 2D和3D暈映均允許使用。 它們或是原本就不可紋理，或是具有特殊「無紋理」旗標設定的平面或流程線物件。 此方法在3D暈映中非常有用，可讓物件參與反射彩現，即使物件只接受純色材質。
* **素描物件**&#x200B;最適合用於具有褶皺和皺紋的織物物件，例如服裝專案。 如同流程線物件，它們可以用於2D和3D暈映，不過在3D暈映中的應用是有限的。
* **壁物件**&#x200B;與平面物件類似，僅支援3D暈映。 它們具有特殊的版面配置資訊，可應用兩種不同的牆面塗飾方式（上層和下層）以及最多三個牆面邊界材料。 如果製作得當，套用至牆壁的材質就能在相鄰牆壁之間準確且順暢地流動，適用於逼真的牆紙/牆壁邊框應用程式。 壁物件不支援紋理旋轉。
* **封包物件**&#x200B;只允許在3D暈映中使用。 它們用於製作具有複雜佈局要求的廚房和浴室櫥櫃。 封包物件接受可重複的紋理以及特別編寫的&#x200B;*封包樣式檔案*，其中包含可調整大小的封包面板影像。

除了基本物件型別外，還支援兩種特殊型別的重疊物件：

* **靜態重疊物件**&#x200B;是不接受材料的物件。 2D和3D暈映均允許使用。 它們對於室內場景中的卸除式配件、可轉譯重疊物件後的陰影以及類似應用程式非常有用。
* **視窗涵蓋範圍框架物件**&#x200B;提供套用視窗涵蓋範圍樣式檔案的位置資訊，這些檔案是獨立於暈映所撰寫，可以在暈映之間共用。

物件會收集到&#x200B;*物件群組*，類似於檔案系統。 群組通常是以它們所代表的實體物件結構為基礎（例如，「所有檔案櫃」群組可能包含「基本檔案櫃」和「壁檔案櫃」）。 允許任何數量的群組層級。 群組支援將材質套用到多個類似物件。

* [場景座標](c-ir-scene-coordinates.md)
* [材質解析度](c-ir-material-resolution.md)
