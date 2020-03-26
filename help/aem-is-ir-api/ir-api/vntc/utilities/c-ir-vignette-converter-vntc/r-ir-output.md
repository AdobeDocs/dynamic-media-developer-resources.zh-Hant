---
description: vntc會產生文字資料，並傳送至stderr或記錄檔。
seo-description: vntc會產生文字資料，並傳送至stderr或記錄檔。
seo-title: 輸出
solution: Experience Manager
title: 輸出
topic: Scene7 Image Serving - Image Rendering API
uuid: f2041600-408f-481c-95fc-3c112def7b8a
translation-type: tm+mt
source-git-commit: 7bc7b3a86fbcdc57cfdc31745fae3afc06e44b15

---


# Output{#output}

vntc會產生文字資料，並傳送至stderr或記錄檔。

每個文本記錄的資料格式 `name=value` 為一個屬性。 字串值不加引號。 警告和錯誤訊息一律會傳送 `stderr`至，即使已 `-log` 指定。

某些屬性可在同一輸出中多次發生。 序號（以0開頭）會附加至這些屬性的名稱，並以句點分隔。 這些屬性在下面以屬性名 `. *`稱后`*` n個尾碼標識。

會產生下列屬性：

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>,<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>機櫃樣式的RGB背景顏色。 僅限機櫃樣式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>預設輸出檔案版本。 此外，此版本的vntc可產生的最高 <span class="filepath"> 檔案</span> 版本號。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">錯誤.<span class="varname"> n</span>=字串<span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>錯誤訊息. 出現錯誤訊息通常表示未建立輸出檔案，或者不適合影像演算使用。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">file.<span class="varname"> n</span>=字串<span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>所有輸出檔案的完全限定路徑／名稱，包括暈映、檔案櫃樣式檔案、完整解析度影像和縮圖影像。 每個生成的檔案（日誌檔案除外）都有一個檔案屬性。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">glass=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 如果機櫃</span> 包含玻璃門，ival為1，否則為0。 僅限機櫃樣式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>嵌入在sourceFile中的iccProfile的 <span class="varname"> 名稱</span>。 </p> <p>如果sourceFile <span class="varname"> 不受色彩管理</span> ，則為空。 僅限暈映。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">info.<span class="varname"> n</span>=字串<span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>資訊性消息，如進度資訊。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 如果sourceFile</span> 是主暈映，ival為1；如果先前已使用 <span class="varname"> vnUpdate</span> 或vntc處理過，ival為0 <span class="filepath"></span><span class="filepath"></span>。 僅限暈映。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 如果sourceFile</span><span class="varname"></span> 是包含JPEG影像資料的檔案櫃樣式（在此例中也會輸出警告），則ival為0，否則為1。 檔案櫃和窗口僅覆蓋樣式檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>運行vntc進程所應用的最大內 <span class="filepath"> 存限</span> 制。 <span class="varname"> 字串</span> 是ival <span class="varname"> 、ivalK、ival</span>、ival <span class="varname"> 、ivalG</span><span class="varname"></span><span class="varname"></span><span class="codeph"></span> 、ivalM_M_J、J（禁用）。 其 <span class="varname"> 中K</span>、 <span class="varname"> M</span>、 <span class="varname"></span> G代表千位元組（1024位元組）、兆位元組（1048576位元組）和千兆位元組（1073741824位元組）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>輸出暈映中最低解析度金字塔級的比例。 僅當指定 <span class="codeph"> -pyramid</span> 時存在。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>sourceFile中保存的材 <span class="varname"> 料數</span>。 僅限暈映。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>此檔案櫃樣式檔案中的面板影像數。 僅限機櫃樣式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>輸出暈映中的金字塔級數。 僅當指定-pyramid時才存在。 僅限暈映。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">金字塔=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>如果源暈映或目標暈映具有金字塔結構，則為0。 僅限暈映。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">解析度=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>對於檔案櫃樣式，為sourceFile的對象解<span class="varname"> 析度</span>。 對於暈映，這是建議的材質解析度，以在轉換輸出暈映時產生最佳品質的演算結果。 像素／英吋(ppi)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>輸出暈映中最小的物件解析度。 僅限暈映。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=val<span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>輸出暈映中的平均物件解析度。 僅限暈映。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>完全限定的 <span class="varname"> sourceFile路徑</span> 。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>sourceFile的檔案 <span class="varname"> 版本</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>,<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>輸入暈映的像素大小、檔案櫃樣式檔案中的預設面板影像，或覆蓋樣式檔案的窗口的第一個不透明度影像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p>視窗覆蓋類型（僅限視窗覆蓋樣式）: </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=水準陰影或窗簾 </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=垂直百葉窗 </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=全寬的窗簾 </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=左／右短窗簾 </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=全寬全長窗簾 </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=左／右全長窗簾 </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6.咖啡廳簾 </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valance </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">suffix=<span class="varname"> string</span></span> </p></td> 
  <td class="stentry"> <p><span class="codeph"> vnt</span> File <span class="varname"> if a vignette, vnc</span> if sourceFile <span class="codeph"> if sourceFile</span> if a cabnit style, if sourceFile <span class="varname"></span><span class="codeph"></span><span class="varname"></span> nw if sourceFile is a window over style in </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>使用 <span class="codeph"> -version</span>指定的值，或預設的<span class="codeph"> FileVersion</span> (如果未指定<span class="codeph"></span> -version)的值。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetIval<span class="varname"> ,ival</span>[,ival<span class="varname"> *,</span>ivalSizes=<span class="varname"> ]</span><span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>輸出暈映（金字塔暈映的全解析度視圖）中所有視圖的像素大小、檔案櫃樣式檔案中預設面板影像或覆蓋樣式檔案的窗口的第一個不透明度影像的逗號分隔清單。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> 如果機櫃樣式可變，ival為1；否則為0。</span> 對暈映和視窗覆蓋樣式檔案不存在。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">警告.<span class="varname"> n</span>=字串<span class="varname"></span></span> </p></td> 
  <td class="stentry"> <p>警告訊息(例如，指定 <span class="codeph"> -imagemap</span> ，但暈映中找不到地圖資料時)。 </p></td> 
 </tr> 
</table>

