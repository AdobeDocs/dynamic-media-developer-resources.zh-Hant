---
title: 命令參考
description: 本節說明HTTP通訊協定命令。
solution: Experience Manager
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 959cb193-d0b7-4aa9-a747-fa17484f80c7
source-git-commit: 347aa2f52bc6433043ba65fc75fe9f7f221e6aa3
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 4%

---

# 命令參考{#command-reference}

本節說明HTTP通訊協定命令。

>[!TIP]
>
>嘗試使用Dynamic Media [_快照_](https://snapshot.scene7.com/)，探索Dynamic Media影像修飾元和智慧型影像的優點。
>
> Snapshot是視覺化展示工具，旨在說明Dynamic Media在最佳化及動態影像傳送方面的強大功能。 實驗測試影像或Dynamic Media URL，以視覺化方式觀察各種Dynamic Media影像修飾元的輸出，以及針對下列專案的智慧型影像最佳化：
>* 檔案大小（含WebP和AVIF傳送）
>* 網路頻寬
>* DPR （裝置畫素比率）
>
>若要瞭解使用快照的簡易程度，請播放[快照訓練影片](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=zh-Hant) （3分17秒）。


**僅適用於Adobe Experience Manager中的Dynamic Media** — 除了使用者介面中可用的基本影像設定之外，AEM ( [!DNL Dynamic Media])中的[!DNL Adobe Experience Manager]還支援您可以在&#x200B;**影像修飾元**&#x200B;欄位中指定的許多進階影像修改。 這些引數定義如下。 但是請注意，AEM的Dynamic Media不支援下列功能。

* 色彩校正命令： `icc=`和`iccEmbed=`。
* 基本範本化和文字演算命令： `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=`和`textPs=`。
* 本地化命令： `locale=`和`req=xlate`。
* `req=set`無法供一般使用。
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* 非核心Dynamic Media服務：SVG、影像演算和Web對列印。

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

另請參閱AEM 6.5檔案中的動態媒體[影像預設集選項](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html?lang=zh-Hant#dynamic)。

* [對齊](r-align.md)
* [錨記](r-anchor.md)
* [bfc](r-bfc.md)
* [bgc](r-bgc.md)
* [bgColor](r-bgcolor.md)
* [混合模式](r-blendmode.md)
* [快取](r-is-http-cache.md)
* [剪裁路徑](r-clippath.md)
* [clipXPath](r-clipxpath.md)
* [色彩](r-color-commandref.md)
* [裁切](r-crop.md)
* [cropPathE](r-croppath.md)
* [預設影像](r-is-http-defaultimage.md)
* [dpr](r-dpr.md)
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
* [遮色片](r-mask.md)
* [遮色片使用](r-maskuse.md)
* [網路](r-network.md)
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
* [矩形](r-rect.md)
* [需要](r-req/r-req.md)
* [res](r-res.md)
* [解析模式](r-is-http-resmode.md)
* [rgn](r-rgn.md)
* [旋轉](r-rotate.md)
* [縮放](r-is-http-scale.md)
* [scl](r-scl.md)
* [大小](r-size-reference.md)
* [src](r-src.md)
* [範本](r-template.md)
* [文字](r-text.md)
* [textAngle](r-textangle.md)
* [textAttr](r-textattr.md)
* [文字流程路徑](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [文字路徑](r-textpath.md)
* [textPs](r-textps.md)
* [type](r-type.md)
* [wid](r-is-http-wid.md)
* [xmpEmbed](r-xmpembed.md)
