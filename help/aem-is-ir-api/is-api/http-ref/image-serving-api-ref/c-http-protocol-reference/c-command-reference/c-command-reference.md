---
title: 命令參考
description: 本節介紹HTTP協定命令。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 187de979d7d1f7ce92b7b4c8b7661a787ab6889f
workflow-type: tm+mt
source-wordcount: '322'
ht-degree: 6%

---

# 命令參考{#command-reference}

本節介紹HTTP協定命令。

>[!TIP]
>
>請試用並探索Dynamic Media影像修飾元和智慧影像處理的優點，使用Dynamic Media [_快照_](https://snapshot.scene7.com/).
>
> Snapshot是視覺化的示範工具，旨在說明Dynamic Media在最佳化和動態影像傳送方面的強大功能。 試用測試影像或Dynamic Media URL，以視覺化方式觀察各種Dynamic Media影像修飾元的輸出，並針對下列項目最佳化智慧型影像：
>* 檔案大小（使用WebP和AVIF傳送）
>* 網路頻寬
>* DPR（裝置像素比率）
>
>要了解使用快照有多簡單，請播放 [快照培訓視頻](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=en) （3分17秒）。


**僅適用於Adobe Experience Manager中的Dynamic Media**  — 除了使用者介面提供的基本影像設定以外， [!DNL Dynamic Media] 在AEM中( [!DNL Adobe Experience Manager])支援許多進階影像修改，您可以在 **影像修飾元** 欄位。 這些參數定義如下。 但請注意，AEM中的Dynamic Media不支援下列功能。

* 顏色校正命令： `icc=` 和 `iccEmbed=`.
* 基本模板和文本呈現命令： `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` 和 `textPs=`.
* 本地化命令： `locale=` 和 `req=xlate`.
* `req=set` 無法用於一般用途。
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* 非核心Dynamic Media服務：SVG、影像轉譯和網路印刷。

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

另見Dynamic Media [影像預設集選項](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic) 在AEM 6.5檔案中。

* [對齊](r-align.md)
* [錨記](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [快取](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [色彩](r-color-commandref.md)
* [農作物](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [效果](r-effect.md)
* [effectMask](r-effectmask.md)
* [延伸](r-extend.md)
* [擬合](r-fit.md)
* [翻轉](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [隱藏](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [層](r-layer.md)
* [地區設定](r-locale.md)
* [地圖](r-map.md)
* [遮罩](r-mask.md)
* [maskUse](r-maskuse.md)
* [op_blur](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contript](r-op-contrast.md)
* [op_grow](r-op-grow.md)
* [op_growMask](r-op-growmask.md)
* [op_growMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_noise](r-op-noise.md)
* [op_saturation](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [opac](r-opac.md)
* [來源](r-origin.md)
* [pathAttr](r-pathattr.md)
* [pathEmbed](r-pathembed.md)
* [透視](r-perspective.md)
* [pos](r-pos.md)
* [printRes](r-printres.md)
* [pscan](r-pscan.md)
* [qlt](r-is-http-qlt.md)
* [數量](r-is-http-quantize.md)
* [正確](r-rect.md)
* [請求](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [旋轉](r-rotate.md)
* [scale](r-is-http-scale.md)
* [scl](r-scl.md)
* [大小](r-size-reference.md)
* [src](r-src.md)
* [範本](r-template.md)
* [文字](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [textFlowPath](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [textPath](r-textpath.md)
* [textPs](r-textps.md)
* [type](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
