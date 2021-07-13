---
description: 這些命令可用於定義圖層效果，如陰影或發光效果。 效果層忽略所有其它命令。
solution: Experience Manager
title: 圖層效果命令
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 483b1f24-9cd2-45e0-9d18-0dc0fbe8abcf
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '124'
ht-degree: 1%

---

# 圖層效果命令{#layer-effect-commands}

這些命令可用於定義圖層效果，如陰影或發光效果。 效果層忽略所有其它命令。

<table id="simpletable_3094B9783772437FAACF9B382F7A32EE"> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-blendmode.md#reference-8be10dde1d584429966cb61ac8e7d172" type="reference" format="dita" scope="local"> blendMode</a> </p></td> 
  <td class="stentry"> <p>指定圖層混合模式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="/help/aem-is-ir-api/is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-data-types/r-is-http-color.md" type="reference" format="dita" scope="local"> color</a> </p></td> 
  <td class="stentry"> <p>指定主效顏色和不透明度。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-effect.md#reference-b1296c4afed047fb921bbc1e33752135" type="reference" format="dita" scope="local"> 效果</a> </p></td> 
  <td class="stentry"> <p>啟動效果層段並指定z順序。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-maskuse.md#reference-9bb1fb5eee4a4bd38f33dadc1a752464" type="reference" format="dita" scope="local"> maskUse</a> </p></td> 
  <td class="stentry"> <p>指定如何使用父級的圖層蒙版（Alpha通道）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-blur.md#reference-00638f29e59b49c99f6bba27daf24668" type="reference" format="dita" scope="local"> op_blur</a> </p></td> 
  <td class="stentry"> <p>讓效果更加豐富。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-grow.md#reference-f95f3291c78c42b9a34b1b7e177e739a" type="reference" format="dita" scope="local"> op_grow</a> </p></td> 
  <td class="stentry"> <p>生長或收縮層效應。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-noise.md#reference-763c4a890fe24bb6bb5ae9dad4e2da94" type="reference" format="dita" scope="local"> op_noise</a> </p></td> 
  <td class="stentry"> <p>增加噪音。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-opac.md#reference-d2269b51aca34599a08d0a46ee5c27e5" type="reference" format="dita" scope="local"> opac</a> </p></td> 
  <td class="stentry"> <p>減少圖層不透明度。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p> <a href="../../../../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-pos.md#reference-65de948f4b404f1182b22119ca332143" type="reference" format="dita" scope="local"> pos</a> </p></td> 
  <td class="stentry"> <p>將效果層相對於其父層定位。 </p></td> 
 </tr> 
</table>
