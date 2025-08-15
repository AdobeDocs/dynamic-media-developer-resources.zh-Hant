---
description: vntc會產生文字資料，並傳送至stderr或記錄檔。
solution: Experience Manager
title: 輸出
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: 48b15fc2-19c2-4ff8-8059-ba3478a4eec2
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 0%

---

# 輸出{#output}

vntc會產生文字資料，並傳送至stderr或記錄檔。

資料格式為每一筆文字記錄一個`name=value`屬性。 字串值未加上引號。 警告和錯誤訊息一律會傳送至`stderr`，即使已指定`-log`亦然。

某些屬性可能會在同一輸出中出現多次。 以0開始的序號會附加至這些屬性的名稱，並以句點分隔。 此類屬性會在屬性名稱后面加上`. *`n`*`尾碼來識別。

會產生下列屬性：

<table id="simpletable_32AAA1A2DDB04BC6B86885E6223BF609"> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">bgc=<span class="varname"> ival</span>，<span class="varname"> ival</span>，<span class="varname"> ival</span></span> </p> </td> 
  <td class="stentry"> <p>封包樣式的RGB背景色彩。 僅限封包樣式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">defaultFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>預設的輸出檔案版本。 也是這個版本的<span class="filepath"> vntc</span>可以產生的最高檔案版本號碼。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">錯誤。<span class="varname"> n</span>=<span class="varname">字串</span></span> </p></td> 
  <td class="stentry"> <p>錯誤訊息。 錯誤訊息的存在通常表示未建立輸出檔案，或不適合用於影像演算。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">檔案。<span class="varname"> n</span>=<span class="varname">字串</span></span> </p></td> 
  <td class="stentry"> <p>所有輸出檔案（包括暈映、封包樣式檔案、完整解析度影像和縮圖影像）的完整路徑/名稱。 每個產生的檔案（記錄檔除外）都會有一個檔案屬性。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">玻璃=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>如果機櫃包含玻璃門，則<span class="varname"> ival</span>為1，否則為0。 僅限封包樣式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">iccProfile=<span class="varname">字串</span></span> </p></td> 
  <td class="stentry"> <p>內嵌於<span class="varname"> sourceFile</span>中的iccProfile名稱。 </p> <p>如果<span class="varname"> sourceFile</span>不是色彩管理，則為空白。 僅限暈映。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">資訊。<span class="varname"> n</span>=<span class="varname">字串</span></span> </p></td> 
  <td class="stentry"> <p>參考訊息，例如進度資訊。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceIsMaster=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>如果<span class="varname"> sourceFile</span>是主暈映，則<span class="varname"> ival</span>為1；如果先前已使用<span class="filepath"> vnUpdate</span>或<span class="filepath"> vntc</span>處理它，則為0。 僅限暈映。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">master=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>如果<span class="varname"> sourceFile</span>是包含JPEG影像資料的封包樣式（在此情況下也會輸出警告），則<span class="varname"> ival</span>為0，否則為1。 僅封包和視窗涵蓋樣式檔案。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxMem=<span class="varname">字串</span></span> </p></td> 
  <td class="stentry"> <p>套用至執行中<span class="filepath"> vntc</span>處理序的最大記憶體限制。 <span class="varname">字串</span>為<span class="varname"> ival</span>、<span class="varname"> ivalK</span>、<span class="varname"> ivalM</span>、<span class="varname"> ivalG</span>或<span class="codeph"> 0</span> （已停用）。 其中<span class="varname"> K</span>、<span class="varname"> M</span>和<span class="varname"> G</span>代表KB （1024位元組）、MB (1048576位元組)和GB (1073741824位元組)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">maxScl=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>輸出暈映中最低解析度金字塔層級的比例。 只有在指定<span class="codeph"> -pyramid</span>時才會出現。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numMaterials=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname"> sourceFile</span>中儲存的材料數目。 僅限暈映。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numPanels=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>此封包樣式檔案中的面板影像數目。 僅限封包樣式。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">numViews=<span class="codeph"> ival</span></span> </p></td> 
  <td class="stentry"> <p>輸出暈映中的金字塔層級數目。 只有在指定 — pyramid時才會出現。 僅限暈映。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">金字塔=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>如果來源或目的地暈映具有金字塔結構，則為0。 僅限暈映。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">解析度=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>對於封包樣式，<span class="varname"> sourceFile</span>的物件解析度。 對於暈映，這是呈現輸出暈映時為獲得最佳品質演算結果而建議的材質解析度。 畫素/英吋(ppi)。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.min=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>輸出暈映中最小的物件解析度。 僅限暈映。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">resolution.avg=<span class="varname"> val</span></span> </p></td> 
  <td class="stentry"> <p>輸出暈映中的平均物件解析度。 僅限暈映。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFile=<span class="varname">字串</span></span> </p></td> 
  <td class="stentry"> <p>完整<span class="varname"> sourceFile</span>路徑。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p><span class="varname">來源檔案</span>的檔案版本。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">sourceSize=<span class="varname"> ival</span>，<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>輸入暈映的畫素大小、封包樣式檔案中的預設面板影像，或視窗遮蓋樣式檔案的第一個不透明度影像。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">style=<span class="varname">字串</span></span> </p></td> 
  <td class="stentry"> <p>視窗涵蓋範圍型別（僅限視窗涵蓋範圍樣式）： </p> <p> 
    <ul id="ul_51AECE556B8B40109FFAD2B315D0695C"> 
     <li id="li_3D3B9211C7AF4810883AE815BEBD4228">0=水準陰影或百葉窗 </li> 
     <li id="li_DE88052467D64ECDAEB29264FC3904E4">1=垂直百葉窗 </li> 
     <li id="li_6F976CABF7244B20A471391A685ED05F"> 2=全形短窗簾 </li> 
     <li id="li_E8D2B0B9189F4BDBB70E145E9196C1CD">3=左/右短窗簾 </li> 
     <li id="li_026F043A50D34C8AB850D9832F375DB7"> 4=全形全長窗簾 </li> 
     <li id="li_283A2E5BFF75461B8F697FFF0796361F"> 5=左/右全長窗簾 </li> 
     <li id="li_E175BA9EAE1F46B89109F4892FF54656"> 6=咖啡廳窗簾 </li> 
     <li id="li_79D2F7F68C4746F3B6742EFECD01BDD9"> 7=valance </li> 
    </ul> </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">尾碼=<span class="varname">字串</span></span> </p></td> 
  <td class="stentry"> <p>如果<span class="codeph"> sourceFile</span>為暈映，<span class="varname"> vnt</span>；如果<span class="codeph"> sourceFile</span>為封包樣式，<span class="varname"> vnc</span>；或者<span class="codeph"> vnw</span> （如果<span class="varname"> sourceFile</span>為視窗涵蓋樣式）。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetFileVersion=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>以<span class="codeph"> -version</span>指定的值，或未指定<span class="codeph"> -version</span>的值<span class="codeph"> defaultFileVersion</span>。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">targetSizes=<span class="varname"> ival</span>，<span class="varname"> ival</span>*[，<span class="varname"> ival</span>，<span class="varname"> ival</span>]</span> </p></td> 
  <td class="stentry"> <p>以逗號分隔的輸出暈映（金字塔暈映的全解析度檢視）中所有檢視的畫素大小清單、封包樣式檔案中預設面板影像的畫素大小清單，或視窗遮蓋樣式檔案的第一個不透明度影像的畫素大小清單。 </p> </td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">texturable=<span class="varname"> ival</span></span> </p></td> 
  <td class="stentry"> <p>如果封包樣式是可紋理的，則<span class="varname"> ival</span>為1，否則為0。 對於暈映和視窗覆蓋樣式檔案不存在。 </p></td> 
 </tr> 
 <tr class="strow"> 
  <td class="stentry"> <p><span class="codeph">警告。<span class="varname"> n</span>=<span class="varname">字串</span></span> </p></td> 
  <td class="stentry"> <p>警告訊息（例如指定<span class="codeph"> -imagemap</span>時，暈映中找不到對應資料）。 </p></td> 
 </tr> 
</table>
