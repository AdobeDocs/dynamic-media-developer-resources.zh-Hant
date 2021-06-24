---
description: 暈映製作工具(Dynamic Media影像製作套件的一部分)提供控制暈映演算引擎低階層面的機制。
solution: Experience Manager
title: 進階轉譯設定
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
exl-id: 0ad8f4b4-dd9c-43f5-aacc-67a564e34d92
source-git-commit: 1ec8b59f442eb96c6c3f5f1405d57a38a86bd056
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 25%

---

# 進階轉譯設定{#advanced-render-settings}

暈映製作工具(Dynamic Media影像製作套件的一部分)提供控制暈映演算引擎低階層面的機制。

>[!NOTE]
>
>「轉譯設定」是「影像轉譯」和「影像編寫」的進階功能。 請聯絡Adobe技術支援或您的Adobe諮詢代表，以取得使用「演算設定」的訓練、諮詢或兩者。

在「影像製作」中以互動方式控制這些設定。 可以使用`rs=`命令（或使用`catalog::RenderSettings`值）在「影像呈現」中應用相同的設定。 此機制用於為每個材料選擇不同的銳利化選項，並修改照度渲染算法的行為，例如改變亮度的飽和度或陰影中的對比度。

## 高級渲染設定(rs=)值 {#section-d9e7f341ebd44f07a4e90f1f5910726b}

<table id="table_1517FC39C7344EBB9F17BE20415DB057"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>Code </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
   <th colname="col3" class="entry"> <p>最小值 </p> </th> 
   <th colname="col4" class="entry"> <p>最大值 </p> </th> 
   <th colname="col5" class="entry"> <p>附註 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>A </p> </td> 
   <td colname="col2"> <p>「渲染效果/替代著色器」(Render Effects/Alternate Shader)會覆蓋暈映中的設定。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>1 </p> </td> 
   <td colname="col5"> <p>A0=渲染效果 </p> <p>A1=替代著色器 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>U </p> </td> 
   <td colname="col2"> <p>USM（不銳利遮色片）。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>2 </p> </td> 
   <td colname="col5"> <p>要使用USM,U必須大於0 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>W </p> </td> 
   <td colname="col2"> <p>USM金額(%)。 </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>500 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>V </p> </td> 
   <td colname="col2"> <p>USM半徑（像素）。 </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>X </p> </td> 
   <td colname="col2"> <p>USM閾值（級別）。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q </p> </td> 
   <td colname="col2"> <p>調整大小模式。 </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>5 </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_87184BB93E7F46D59BA1AAAFA8455512"> 
      <li id="li_E7711C3678ED4DE09E710F7C430CEF42">最近鄰 </li> 
      <li id="li_CAE975B91C604DA0AA493F700AEBE199">雙線性 </li> 
      <li id="li_24E5A40B8A3F4C808A68686C27647CD5">雙立方式 </li> 
      <li id="li_42ACFCE65B4843ACAFA6A52255364642">超採樣（預設值） </li> 
      <li id="li_34EC85C4D15145DF80F7D3DB7B6244D3">蘭喬斯窗口 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>R </p> </td> 
   <td colname="col2"> <p>重新取樣模式。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>5 </p> </td> 
   <td colname="col5"> <p> 
     <ul id="ul_FD4A9D73C32F47C3BF13776BB4D2818D"> 
      <li id="li_F08AD1D093D74059B60302374B472B52">預設 </li> 
      <li id="li_FD4C859D975B44399475D4D93D6B05AB">最近鄰 </li> 
      <li id="li_CA93566F5D4F4D3CAA1D0816562A3851">雙線性 </li> 
      <li id="li_D334ACF969E749A89A464B21C96CE8A6">超級取樣 </li> 
      <li id="li_FAC72C36FF4A418F8A5B05F3B4E7C5D8">最適化 </li> 
      <li id="li_6E9D81045A0C4804A4D35D9B239F6486">泊松採樣器 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>T </p> </td> 
   <td colname="col2"> <p>超採樣：隨機。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>200 </p> </td> 
   <td colname="col5"> <p>預設為 0。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>S </p> </td> 
   <td colname="col2"> <p>超採樣：隨機率。 </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>20 </p> </td> 
   <td colname="col5"> <p>預設為 5。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>M </p> </td> 
   <td colname="col2"> <p>可調整大小：深度。 </p> </td> 
   <td colname="col3"> <p>4 </p> </td> 
   <td colname="col4"> <p>8 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>N </p> </td> 
   <td colname="col2"> <p>可調整大小：寬度。 </p> </td> 
   <td colname="col3"> <p>2 </p> </td> 
   <td colname="col4"> <p>10 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>P </p> </td> 
   <td colname="col2"> <p>泊松：樣本/像素。 </p> </td> 
   <td colname="col3"> <p>1 </p> </td> 
   <td colname="col4"> <p>4 </p> </td> 
   <td colname="col5"> <p>預設為 1。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Y </p> </td> 
   <td colname="col2"> <p>泊松：使用切換。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>1 </p> </td> 
   <td colname="col5"> <p>預設為 1。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>渲染效果（舊著色器）</b> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>I </p> </td> 
   <td colname="col2"> <p>重點。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>J </p> </td> 
   <td colname="col2"> <p>反白顯示飽和度。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>50 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H </p> </td> 
   <td colname="col2"> <p>光亮材料的陰影。 </p> </td> 
   <td colname="col3"> <p>50 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>K </p> </td> 
   <td colname="col2"> <p>陰影飽和度。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>400 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>L </p> </td> 
   <td colname="col2"> <p>基於光澤的外推強度。 </p> </td> 
   <td colname="col3"> <p>100 </p> </td> 
   <td colname="col4"> <p>600 </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0 </p> </td> 
   <td colname="col2"> <p>亮度補償（核取方塊） </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p>預設為on（空白），且取消選取= F100G0。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"><b>替代著色器</b> </td> 
   <td colname="col2"> </td> 
   <td colname="col3"> </td> 
   <td colname="col4"> </td> 
   <td colname="col5"> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Z </p> </td> 
   <td colname="col2"> <p>基本對比。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p>預設為 50。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>a </p> </td> 
   <td colname="col2"> <p>亮度補償。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>格式不同：a36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>b </p> </td> 
   <td colname="col2"> <p>飽和度調整。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>格式不同：b36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>c </p> </td> 
   <td colname="col2"> <p>陰影調整。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>格式不同：c36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>d </p> </td> 
   <td colname="col2"> <p>突出顯示調整。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>格式不同：d36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>e </p> </td> 
   <td colname="col2"> <p>鏡面光。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>格式不同：e36.207.136.177.xx </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>x </p> </td> 
   <td colname="col2"> <p>形狀. </p> </td> 
   <td colname="col3"> <p>-100 </p> </td> 
   <td colname="col4"> <p>100 </p> </td> 
   <td colname="col5"> <p>請參閱上述值中的「xx」。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>k </p> </td> 
   <td colname="col2"> <p>光照調整。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>格式不同：k64.138.175.60.xx.133.242 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>u&amp;s </p> </td> 
   <td colname="col2"> <p>陰影色調變化。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>格式不同：u8.1.2.3.4.5.6.7.8.s8.1.2.3.4.5.6.7.8。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>v&amp;t </p> </td> 
   <td colname="col2"> <p>反白顯示色相移。 </p> </td> 
   <td colname="col3"> <p>0 </p> </td> 
   <td colname="col4"> <p>255 </p> </td> 
   <td colname="col5"> <p>格式不同：v8.1.2.3.4.5.6.7.8.t8.1.2.3.4.5.6.7.8。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>w </p> </td> 
   <td colname="col2"> <p>飽和度調整。 </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>g </p> </td> 
   <td colname="col2"> <p>低飽和度提升。 </p> </td> 
   <td colname="col3"> <p> </p> </td> 
   <td colname="col4"> <p> </p> </td> 
   <td colname="col5"> <p> </p> </td> 
  </tr> 
 </tbody> 
</table>

## 高級呈現設定示例 {#section-56528569eae44ecd997a289b211ff256}

<table id="table_062DCF66ACCC4A6997E3CA951C0A12B8"> 
 <thead> 
  <tr> 
   <th colname="col1" class="entry"> <p>設定組合物 </p> </th> 
   <th colname="col2" class="entry"> <p>說明 </p> </th> 
  </tr>
 </thead>
 <tbody> 
  <tr> 
   <td colname="col1"> <p>H60I30J10K200L400U1V10W100X0 </p> </td> 
   <td colname="col2"> <p>影像製作中的預設值。 
     <ul id="ul_AA7CF1A3E6984B318265BBE8FFFBB4EE">
      <li> USM1
      <li id="li_8EC075956E2E4D5A91355122DC9BC938">H60 =亮材料的陰影(50-100)。 </li> 
      <li id="li_F760B65E057146A7B56673D6B1A9A304">I30 =重點(0-100)。 </li> 
      <li id="li_376C275FDB3548958C09BD266C77318F">J10 =高亮顯示飽和度(0-50)。 </li> 
      <li id="li_FE26429972F544869CDFE2DD61F39CC5">K200 =陰影飽和度(0-400)。 </li> 
      <li id="li_FB6BAA708427428AA4A3AC2E5D3B9932">L400 =基於光澤的外推強度(100-600)。 </li> 
      <li id="li_6B2EEEE7F0D54E078462AAFC4E4FAB42">U1 = USM（遮色片銳利化）(0-2)。 </li> 
      <li id="li_7CD4E3662A6C48F9B5895D133D28BA2A">V10 = USM半徑（1-100像素）。 </li> 
      <li id="li_949B6DB4959B46A892787CD5B3AD7485">W100 = USM金額(1%-500%)。 </li> 
      <li id="li_F39D3834D4A2478D993E5E9C9B434CFE">X0 = USM閾值（0-255級）。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H50I0J0K0L100U1V1W1 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_C6E6DD90ECAB4D2B9284A25A29923DC6"> 
      <li id="li_7B7A8C43BCEB4CB58C7074974CAB0419">USM1 </li> 
      <li id="li_A003B68023424DCABBF3A2CAF98C39A4">所有最大和亮度補償都已開啟。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0H50I0J0K0L100U1V1W1 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_AAEC098CED1C436E933B1C1B88DFB659"> 
      <li id="li_0CC34CDD796E4DFD802824FF21DB021B">USM1 </li> 
      <li id="li_E36886FB1D00444CBA19D7245E89B292">所有最大和亮度補償都關閉。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>F100G0H100I100J50K400L600U2V100W500X255 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_6BB668C6C055493DAAA38F4D3B9C20A7"> 
      <li id="li_D8BAFB41CF4C4B3FAD6F89AF5D7F223A">USM2 </li> 
      <li id="li_DA685F4DE4BA427BA7BE241A75C96152">所有最大和亮度補償都關閉。 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>H80I70J40L300U1V8W80X5 </p> </td> 
   <td colname="col2"> <p> 
     <ul id="ul_7C374842312E4AD0B62692BBCE6743A8"> 
      <li id="li_CC730580B54741FBBBFF507DE0FE1F15">H80 = USM金額 </li> 
      <li id="li_C2801B2C093444AC9401793BC571EC27">I70 =亮點 </li> 
      <li id="li_518C6A690EC34614B0806A0C6BC535FF">J40 =高光飽和度 </li> 
      <li id="li_F280CF29D1E341D9AC9C0C16C2DEA1E6">L300 =基於光澤的外推強度 </li> 
      <li id="li_3F589F109AC94280911BD535C49E42E4">U1 = USM </li> 
      <li id="li_113FEC9B37D54511BAB3FEAC7C271858">V8 = USM半徑 </li> 
      <li id="li_E1BA7406A76B476EB1A89D6EDD87930C">W80 =亮材料的陰影 </li> 
      <li id="li_AAD479EF6A7F43B98A8C147FCD684ECA">X5 = USM臨界值 </li> 
     </ul> </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p>Q5R3S11T103U1V6W120X5Z80b.188.88.75.37 </p> </td> 
   <td colname="col2"> <p>具有銳利化的替代著色器： </p> <p> 
     <ul id="ul_93AD53BB37EA47F6A3CEE424D3AAE18C"> 
      <li id="li_9EF1DF4167164721882E4842C2E0B20C">USM1 </li> 
      <li id="li_7B5D8B7BB5544E7FA4AD702EE281086B">USM金額(120) </li> 
      <li id="li_B3BE096BB0654A2DBADDD6832E499F2A">USM半徑(0.6) </li> 
      <li id="li_793DAB145CE7469ABC1182BCBD324657">USM閾值(5) </li> 
      <li id="li_B1954FEBE2084726828D64E8165DA4DA">調整大小(Lanczos) </li> 
      <li id="li_E5ED76998C0543D8A3F9AD178CFD3C2C">重新取樣（超級取樣，隨機=半，速率=半） </li> 
      <li id="li_CCEE53544E7D48858398BF3168F1E87D">對比（更強） </li> 
      <li id="li_EB0D25C095FB4D5798AC031AB759849B">飽和度調整（中間的第一頂點、沿邊的第二頂點、第三頂點中點低） </li> 
      <li id="li_5C2304DA4A4D4799AE5DCCCB1E2ECBB3">銳利化（右側為3/4） </li> 
     </ul> </p> </td> 
  </tr> 
 </tbody> 
</table>

<!-- RB: I don't know why this is in here; it was added by someone else: 
Alternate Shader Rendering (default on) checkbox provides a more precise Advanced Shader diffuse rendering pipeline. For a number of effects it also provides an alternate Advanced Shader rendering pipeline. Note that the underlying OpenGL hardware must provide support for the Advanced (Per-Pixel) GLSL Shaders for this option to be vailable; else this checkbox is automatically disabled. -->

<!-- RB: I don't know why this is in here; it was added by someone else:
It should probably also go into the different renders - Render Effects and Alternate Shader - or link to descriptions of each. -->
