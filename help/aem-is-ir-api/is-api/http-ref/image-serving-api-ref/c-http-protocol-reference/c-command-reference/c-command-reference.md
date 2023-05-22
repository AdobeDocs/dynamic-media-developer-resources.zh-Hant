---
title: 命令引用
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

# 命令引用{#command-reference}

本節介紹HTTP協定命令。

>[!TIP]
>
>使用Dynamic Media，嘗試並瞭解Dynamic Media映像修改程式和智慧映像的優勢 [_快照_](https://snapshot.scene7.com/)。
>
> Snapshot是一種直觀的演示工具，旨在展示Dynamic Media在優化和動態影像傳輸方面的威力。 對test影像或Dynamic MediaURL進行實驗，以直觀地觀察各種Dynamic Media影像修飾符的輸出，並對以下各項進行智慧成像優化：
>* 檔案大小（使用WebP和AVIF交付）
>* 網路頻寬
>* DPR（設備像素比）
>
>要瞭解使用快照有多容易，請播放 [快照培訓視頻](https://experienceleague.adobe.com/docs/experience-manager-learn/assets/dynamic-media/images/dynamic-media-snapshot.html?lang=en) （3分17秒）。


**只為Dynamic Media在Adobe Experience Manager**  — 除用戶介面中提供的基本映像設定外， [!DNL Dynamic Media] 中AEM [!DNL Adobe Experience Manager])支援許多可在中指定的高級映像修改 **影像修飾符** 的子菜單。 這些參數在下面定義。 但請注意，Dynamic Media不支援以下功AEM能。

* 顏色校正命令： `icc=` 和 `iccEmbed=`。
* 基本模板和文本渲染命令： `text= textAngle= textAttr= textFlowPath= textFlowXPath= textPath=` 和 `textPs=`。
* 本地化命令： `locale=` 和 `req=xlate`。
* `req=set` 不可用於一般用途。
* `req=mbrset`
* `req=saveToFile`
* `req=targets`
* `template=`
* 非核心Dynamic Media服務：SVG、影像渲染和Web到打印。

<!-- Adobe IS command examples website  http://sj1010010254235.corp.adobe.com/iscommands/ -->

另見Dynamic Media [影像預設選項](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/managing-image-presets.html#dynamic) 在6.AEM5文檔中。

* [對齊](r-align.md)
* [錨記](r-anchor.md)
* [足球](r-bfc.md)
* [BGC](r-bgc.md)
* [bg顏色](r-bgcolor.md)
* [blendMode](r-blendmode.md)
* [快取](r-is-http-cache.md)
* [剪輯路徑](r-clippath.md)
* [剪輯XPath](r-clipxpath.md)
* [色彩](r-color-commandref.md)
* [作物](r-crop.md)
* [裁剪路徑E](r-croppath.md)
* [預設影像](r-is-http-defaultimage.md)
* [影響](r-effect.md)
* [效果掩碼](r-effectmask.md)
* [延伸](r-extend.md)
* [合](r-fit.md)
* [翻轉](r-flip.md)
* [fm](r-is-http-fmt.md)
* [hei](r-is-http-hei.md)
* [隱藏](r-hide.md)
* [icc](r-icc.md)
* [icc嵌入](r-iccembed.md)
* [id](r-id.md)
* [影像集](r-imageset.md)
* [jpeg大小](r-jpegsize.md)
* [層](r-layer.md)
* [地區設定](r-locale.md)
* [地圖](r-map.md)
* [掩模](r-mask.md)
* [掩碼使用](r-maskuse.md)
* [op_blur](r-op-blur.md)
* [op_brightness](r-op-brightness.md)
* [op_colorbalance](r-op-colorbalance.md)
* [op_colorize](r-op-colorize.md)
* [op_contrast](r-op-contrast.md)
* [op_grow](r-op-grow.md)
* [op_grow掩碼](r-op-growmask.md)
* [op_growMaskR](r-op-growmaskr.md)
* [op_hue](r-op-hue.md)
* [op_invert](r-op-invert.md)
* [op_noise](r-op-noise.md)
* [op飽和](r-op-saturation.md)
* [op_sharpen](r-op-sharpen.md)
* [op_usm](r-op-usm.md)
* [op_usmR](r-op-usmr.md)
* [Opac](r-opac.md)
* [來源](r-origin.md)
* [路徑屬性](r-pathattr.md)
* [路徑嵌入](r-pathembed.md)
* [透視](r-perspective.md)
* [pos](r-pos.md)
* [打印資源](r-printres.md)
* [掃描](r-pscan.md)
* [QLT](r-is-http-qlt.md)
* [量化](r-is-http-quantize.md)
* [正](r-rect.md)
* [請求](r-req/r-req.md)
* [雷](r-res.md)
* [resMode](r-is-http-resmode.md)
* [rng](r-rgn.md)
* [旋轉](r-rotate.md)
* [scale](r-is-http-scale.md)
* [scl](r-scl.md)
* [大小](r-size-reference.md)
* [高](r-src.md)
* [範本](r-template.md)
* [文字](r-text.md)
* [文本角度](r-textangle.md)
* [文本屬性](r-textattr.md)
* [文本流路徑](r-textflowpath.md)
* [textFlowXPath](r-textflowxpath.md)
* [文本路徑](r-textpath.md)
* [文本Ps](r-textps.md)
* [type](r-type.md)
* [wid](r-is-http-wid.md)
* [xmp嵌入](r-xmpembed.md)
