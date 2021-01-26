---
description: 本節介紹HTTP協定命令。
seo-description: 本節介紹HTTP協定命令。
seo-title: 命令參考
solution: Experience Manager
title: 命令參考
topic: Dynamic Media Image Serving - Image Rendering API
uuid: 72c4ed61-3436-4df5-b586-77808fb1903a
translation-type: tm+mt
source-git-commit: 97a84e8e7edd3d834ca42069eae7c09c00d57938
workflow-type: tm+mt
source-wordcount: '224'
ht-degree: 10%

---


# 命令參考{#command-reference}

本節介紹HTTP協定命令。

**僅適用於AEM中的動態媒體**:除了使用者介面中提供的基本影像設定外， [!DNL Dynamic Media] 在AEM( [!DNL Adobe Experience Manager])中還支援許多進階的影像修改，您可在 **Image** Modifiersfield中指定。這些參數定義如下。 但是，請注意，AEM中的Dynamic Media不支援下列功能。

* 色彩校正指令：`icc=`和`iccEmbed=`。
* 基本範本和文字轉換指令：`text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=`和`textPs=`。
* 本地化命令：`locale=`和`req=xlate`。
* `req=set` 無法用於一般用途。
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* 非核心動態媒體服務：SVG、影像轉換和網路印刷。

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

另請參閱AEM 6.5檔案中的「動態媒體[影像預設集選項](https://docs.adobe.com/content/help/en/experience-manager-65/assets/dynamic/managing-image-presets.html#image-preset-options)」。

* [對齊](r-align.md)
* [錨記](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [快取](r-is-http-cache.md)
* [clipPath](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [color](r-color-commandref.md)
* [裁切](r-crop.md)
* [cropPathE](r-croppath.md)
* [defaultImage](r-is-http-defaultimage.md)
* [效果](r-effect.md)
* [effectMask](r-effectmask.md)
* [延伸](r-extend.md)
* [符合](r-fit.md)
* [翻轉](r-flip.md)
* [fmt](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [隱藏](r-hide.md)
* [icc](r-icc.md)
* [iccEmbed](r-iccembed.md)
* [id](r-id.md)
* [imageSet](r-imageset.md)
* [jpegSize](r-jpegsize.md)
* [圖層](r-layer.md)
* [地區設定](r-locale.md)
* [地圖](r-map.md)
* [遮罩](r-mask.md)
* [maskUse](r-maskuse.md)
* [op_blur](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrast](r-op-contrast.md)
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
* [量化](r-is-http-quantize.md)
* [rect](r-rect.md)
* [requin](r-req/r-req.md)
* [res](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [rotate](r-rotate.md)
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
* [類型](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
