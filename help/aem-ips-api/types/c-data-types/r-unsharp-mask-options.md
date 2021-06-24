---
description: 有助於改進優化金字塔TIF檔案的影像清晰度的設定。
solution: Experience Manager
title: 不銳利化遮色片選項
feature: Dynamic Media Classic,SDK/API，資產管理
role: Developer,Administrator
exl-id: 7150b4a8-a44d-4858-96f2-6004d5f48e77
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 12%

---

# 不銳利化遮色片選項{#unsharpmaskoptions}

有助於改進優化金字塔TIF檔案的影像清晰度的設定。

`unsharpMaskOptions=[ *`數量、半徑、臨界值、單色`*]`

## 參數 {#section-c3f0d03136ba4422819cb463bd393885}

為`minOccurs=" *`n`*".`的`unsharpMaskOptions`選項指定值

<table id="table_D1392963C5694969A9D546F82DB6F45C">
 <thead>
  <tr>
   <th colname="col1" class="entry"> 名稱 </th>
   <th colname="col2" class="entry"> 類型 </th>
   <th colname="col3" class="entry"> 說明 </th>
  </tr>
 </thead>
 <tbody>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 量</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>控制套用至邊緣像素的對比度。 
     <ul id="ul_7AA17E354EE64BC4A5BEAE853FF17191">
      <li id="li_42FB21C7ED884E1DB03274130B8DCB10">範圍：0.0 - 5.0 </li>
      <li id="li_E980CAA1A9C54D60A121F21C964820FF">預設值：0 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 半徑</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:double</span></td>
   <td colname="col3"><p>通過設定影像邊緣周圍的像素數來控制銳度。 正確的值取決於影像大小。 
     <ul id="ul_D4391CD407DE4B48AF4523EBD85D0D40">
      <li id="li_8AEF11A489484EFD91416F8A03C4DB25">範圍：0.0 - 250.0 </li>
      <li id="li_9F1D1B52AFBA46B8BDCDF99A21140002">低值僅銳化邊緣像素。 </li>
      <li id="li_7D9FD8AA4899404283D7AB596364A4AF">高值會銳利化較寬的像素帶。 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 臨界值</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>決定不同像素在被視為邊緣像素且可銳化之前必須與周圍區域的差異。 
     <ul id="ul_117E556E3ECF42CC878DD80D338D19CA">
      <li id="li_CFEE76DB78BF437E8463C9089486F8A6">範圍：0 - 255（僅限整數）。 </li>
      <li id="li_77113DC2698A4D48B11288718766E6A2">預設值：6 </li>
     </ul></p></td>
  </tr>
  <tr>
   <td colname="col1"><span class="codeph"><span class="varname"> 單色</span></span></td>
   <td colname="col2"><span class="codeph"> xsd:int</span></td>
   <td colname="col3"><p>值僅包含<span class="codeph"> 0</span>或<span class="codeph"> 1</span>。 </p><p>設為<span class="codeph"> 0</span>以分別應用於每個顏色分量，或設為<span class="codeph"> 1</span>以僅應用於影像亮度（強度）。 圖層遮色片或複合遮色片也會銳化。 </p><p><span class="codeph"><span class="varname"> </span></span> 灰階影像會忽略單色。 </p></td>
  </tr>
 </tbody>
</table>

## 範例 {#section-38adca96c7714cfea35331d20403f59e}

```
<element name="unsharpMaskOptions" type="types:UnsharpMaskOptions" minOccurs="0"/>
    <complexType name="UnsharpMaskOptions">
        <sequence>
            <element name="amount" type="xsd:double" minOccurs="0"/>
            <element name="radius" type="xsd:double" minOccurs="0"/>
            <element name="threshold" type="xsd:int" minOccurs="0"/>
            <element name="monochrome" type="xsd:int" minOccurs="0"/>        
        </sequence>
    </complexType>
```

## 使用者 {#section-db8124a5468b498694a780f8a56a4560}

`unsharpMaskOptions`類型由：

* [ReprocessAssetsJob](../../types/c-data-types/r-reprocess-assets-job.md#reference-a303f7832ae44fdab1dca7cc8bef3fa3)
* [UploadDirectoryJob](../../types/c-data-types/r-upload-directory-job.md#reference-e707ebf53b074c49ad983d1886e0bbb6)
* [UploadPostJob](../../types/c-data-types/r-upload-post-job.md#reference-bca2339b593f4637a687c33937215ef4)
* [UploadUrlsJob](../../types/c-data-types/r-upload-urls-job.md#reference-8e9bc895268c4321b233dbeadc990398)

>[!MORELIKETHIS]
>
>* [影像提供API參考：op_usm](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/image-serving-api/image-serving-api/http-protocol-reference/command-reference/r-op-usm.html)

