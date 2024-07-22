---
description: 套用PDF工作選項。 工作選項檔案或PDF預設集是Illustrator在「另存為PDF選項」對話方塊中產生的檔案，或是PDF的InDesign預設集。
solution: Experience Manager
title: 工作選項
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 8e7224e7-d801-4550-b95e-24d15734043a
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '239'
ht-degree: 38%

---

# 工作選項{#joboption}

套用PDF工作選項。 工作選項檔案或PDF預設集是Illustrator在「另存為PDF選項」對話方塊中產生的檔案，或是PDF的InDesign預設集。

` joboption= *`值`*`

<table id="simpletable_BA7B58BE0B0740298D45DDEBE7832D93"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph"> <span class="varname">值</span></span> </p> </td> 
  <td class="stentry"> <p>工作選項檔案的IPSID。 </p></td> 
 </tr> 
</table>

工作選項檔案可由IPS/Dynamic Media Classic上傳和發佈。 產生PDF時會使用工作選項檔案中包含的PDF選項。

目前支援的選項如下：

<table id="simpletable_7E0AE8A06AE54A02AF0107FBEDF73D61"> 
 <tr class="strow"> 
  <td class="stentry"> <p>一般 </p></td> 
  <td class="stentry"> <p> 相容性 </p> <p> 物件等級壓縮 </p> <p> 內嵌縮圖 </p> <p> 最佳化快速網頁檢視 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>影像 </p></td> 
  <td class="stentry"> <p> 縮減取樣、解析度、臨界值和壓縮色彩、灰階和單色 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>字型 </p></td> 
  <td class="stentry"> <p> 嵌入所有字型 </p> <p> 內嵌 OpenType 字型 </p> <p> 子集內嵌的字型，若使用的字元百分比低於: </p> <p> 永遠內嵌清單 </p> <p> 永不內嵌清單 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>色彩 </p></td> 
  <td class="stentry"> <p> 色彩策略（僅標籤影像會被視為標籤所有內容） </p> <p> 文件演算色彩比對方式 </p> <p> 4.2.5僅支援下列工作區。 </p> <p> 
    <ul id="ul_3F3EFDFB6A3340978AE31DEDF0FDA2C8"> 
     <li id="li_17A9FA99D6CA4C5182E383A85F0E3C90"> RGB <p> 
       <ul id="ul_1DD0C264DA1248319E751ADD18140C6D"> 
        <li id="li_B91B4D0C1D80442EB8690933AFA1F093"> e-sRGB </li> 
        <li id="li_D7F8C500DF5E4CBC8FFA4FEFB8E4E036"> scRGB，編碼範圍為 [-4.0, 4.0] </li> 
        <li id="li_942CD69732984E16A71C2F75EC5B5245"> Lab D50 </li> 
        <li id="li_7063B9E98D1E4946AC8F0EF7BC988806"> PCS XYZ </li> 
        <li id="li_5809447576B147B68630C4B7EC2E7870"> 平面 XYZ </li> 
        <li id="li_3B5DA42A04124A6BAA12343AFC19F620">線性 ROMM-RGB </li> 
        <li id="li_DEC3028FA9C34176B761D12B7179B44F">ROMM-RGB </li> 
        <li id="li_3E7E7C4A680C4E3EADE0A26048ECF1F4"> sYCC 8 位元 </li> 
        <li id="li_16A615C9A74D443AB3C63B3FE3AB5443"> e-sYCC 8 位元 </li> 
       </ul> </p> </li> 
     <li id="li_AFA6D4D8C0624AA495E2EB2F0F0C7F7B">灰色 <p> 
       <ul id="ul_945389DD426F44C09EB9C7F23933CB77"> 
        <li id="li_DB0AE3DFFC184480BB91666FF1BB4776">灰階係數 1.8 </li> 
        <li id="li_755C556ED94740D1BD30EBE67018E074">灰階係數 2.2 </li> 
        <li id="li_67437440AFB54B7686333A55233AA87F">網點增大 10% </li> 
        <li id="li_0D6CA6004EC84048B5F2198406F4F343">網點增大 15% </li> 
        <li id="li_1AFD11C23AB147978559D8F00BFB3142">網點增大 20% </li> 
        <li id="li_6CD5ACEF6B0B49E8BACA8264FE0E9C44"> 網點增大 25% </li> 
        <li id="li_AB5F1FA7111041BD82353E02A284A546">網點增大 30% </li> 
        <li id="li_7433278AE8054AD28BD38A0A6E4EF7EF"> sGray </li> 
       </ul> </p> </li> 
    </ul> </p> <p> 保留用於校正 CMYK 色域的 CMYK 值 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>進階 </p></td> 
  <td class="stentry"> <p>「保留OPI註解」一律開啟。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p>標準 </p></td> 
  <td class="stentry"> <p>合規性標準。 </p></td> 
 </tr> 
</table>
