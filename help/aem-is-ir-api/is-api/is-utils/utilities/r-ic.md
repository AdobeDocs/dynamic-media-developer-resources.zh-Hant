---
description: 映像轉換實用程式。
solution: Experience Manager
title: 整合電路
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: ab653aae-532b-4f3d-8541-f6296fbf9172
source-git-commit: 790ce3aa4e9aadc019d17e663fc93d7c69772b23
workflow-type: tm+mt
source-wordcount: '1203'
ht-degree: 2%

---

# 整合電路 {#ic}

映像轉換實用程式。

`ic` 是將影像檔案轉換為優化的金字塔TIFF格式(PTIFF)的命令行工具。 雖然「影像服務」可以處理影像而不進行轉換，但建議將所有大於512x512像素的影像轉換為PTIFF。 此轉換可確保最佳伺服器效能和資源利用率，並最大限度地縮短響應時間。

建議將包含照片內容的PTIFF檔案JPEG編碼(指定 `-jpegcompress`)。 電腦生成的內容可以從無損壓縮中獲益(可以是 `-deflatecompress` 或 `-lzwcompress`)。 除非需要顏色轉換或像素類型轉換，否則JPEG源影像資料將不進行解碼而傳輸到PTIFF，以避免質量下降。 在這種情況下，指定的壓縮選項只適用於較低解析度的金字塔級。

如果不轉換大影像，則不必設定控制要使用的記憶體量的參數。 但是，如果是，請 `ic` 使用 `-maxmem` 下面介紹的設定。 計算所需記憶體量的一個很好的經驗法則是將影像的寬度乘以影像的高度乘以通道數。 例如，對於Alpha乘3的RGB影像，為4。 此外，如果通道是每個分量16位，而不是最終結果的8倍。

## 使用 {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]`*`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]`*`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]`*`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>選項</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>命令選項（請參閱下文）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> <i>源檔案</i> </span> </span> </p> </td> 
   <td colname="col2"> <p>單個輸入影像檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>目標檔案</i></span> </span> </p> </td> 
   <td colname="col2"> <p>單個輸出PTIFF檔案（如果與SourceDirectory一起使用，則無效）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>源資料夾</i></span> </span> </p> </td> 
   <td colname="col2"> <p>包含輸入影像的資料夾。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>目標資料夾</i></span> </span> </p> </td> 
   <td colname="col2"> <p>輸出PTIFF檔案寫入到的資料夾。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 返回 {#section-36a2dcfa39824d29b69547c432366219}

0（如果成功）。 如果發生錯誤，則返回非零值，並將錯誤詳細資訊發送到 `stderr`。

## 選項 {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -未壓縮 </span> </p> </td> 
   <td colname="col2"> <p>不壓縮輸出影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflate壓縮 </span> </p> </td> 
   <td colname="col2"> <p>使用壓縮(zip)壓縮（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>使用Lempel-Ziv-Welch(LZW)壓縮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpecmpress </span> </p> </td> 
   <td colname="col2"> <p>使用JPEG編碼。 如果忽略 <span class="codeph"> <span class="varname"> 源檔案 </span> </span> 包括Alpha資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> 質量 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>JPEG質量(0-100;預設值為95)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">  — 滿載 </span> </p> </td> 
   <td colname="col2"> <p>禁用JPEG降色採樣（可改善彩色文本和圖形的質量）。 這對CMYK或灰度的輸出影像沒有影響。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> 金額 </span>&gt; &lt; <span class="varname"> 半徑 </span>&gt; &lt; <span class="varname"> 閾值 </span>&gt; &lt; <span class="varname"> 單色 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>對子採樣金字塔級應用反銳化掩碼。 請參閱 <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> op_usm= </a> 的雙曲餘切值。 （未應用於全解析度影像。） </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>使用源檔案中的剪輯路徑（如果有）建立關聯的Alpha資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dip </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>打印解析度(dpi) <span class="codeph"> <span class="varname"> 目標檔案 </span> </span>;如果未指定，則打印解析度 <span class="codeph"> src檔案 </span> 複製到 <span class="codeph"> <span class="varname"> 目標檔案 </span> </span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">  — 自動裁剪&lt; <span class="varname"> 角 </span>&gt; &lt; <span class="varname"> 模式 </span>&gt; &lt; <span class="varname"> 容差 </span>&gt; &lt; <span class="varname"> 資訊檔案 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>計算裁剪矩形以最小化實色背景。 如果自動裁剪算法會導致整個影像被裁剪，則不會輸出裁剪資訊。 </p> <p>要計算裁剪矩形而不轉換影像，請指定 <span class="codeph">  — 自動裁剪 </span> 無 <span class="codeph">  — 轉換 </span> 沒有 <span class="codeph"> <span class="varname"> destFile。</span> </span></p>

<p><i><b>角</b></i> - ul |ur | | lr </p>
   <p> 指定要使用種子點的影像的哪個角。 如果模式為1，則忽略。</p>
   <p><i><b>模式</b></i> - 0 | 1</p>
   <p>設定為0以根據指定角點像素的顏色裁剪；如果Alpha資料與源影像相關聯，則對預乘顏色資料進行操作。</p>
   <p>設定為1以基於Alpha資料裁剪；角被忽略，0總是種子值；如果沒有與源影像關聯的alpha資料，則不應用裁剪。</p> 
   <p><i><b>容差</b></i>  — 匹配容差。 實值0.0到1.0。指定匹配像素元件值的容差。 為完全匹配設定0。</p>
   <p><i><b>資訊檔案</b></i>  — 將裁剪資訊資料寫入到的XML輸出檔案的路徑和名稱。</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>複製XMP元資料（如果可用） <span class="codeph"> <span class="varname"> 源檔案 </span> </span> 至 <span class="codeph"> <span class="varname"> 目標檔案 </span> </span> 不修改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> 將ICC顏色配置檔案嵌入 <span class="codeph"> <span class="varname"> 目標檔案 </span> </span>，如果可用（預設情況下未嵌入任何配置檔案）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> 檔案 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC配置檔案的路徑和名稱。 定義顏色空間 <span class="codeph"> <span class="varname"> 源檔案 </span> </span> 必須匹配其像素類型。 僅當未嵌入配置檔案時才應指定 <span class="codeph"> <span class="varname"> 源檔案 </span> </span>，因為這將覆蓋嵌入的配置檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> 檔案 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC配置檔案的路徑和名稱。 定義的像素類型和顏色空間 <span class="codeph"> <span class="varname"> 目標檔案 </span> </span>。 IC在 <span class="codeph"> <span class="varname"> 源檔案 </span> </span> 具有嵌入的配置檔案，或 <span class="codeph"> -imageprofile </span> 。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentCenterval </span> </p> </td> 
   <td colname="col2"> <p>顏色空間轉換的感知渲染意圖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRel比色 </span> </p> </td> 
   <td colname="col2"> <p> 顏色空間轉換的相對比色渲染方法（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbs比色 </span> </p> </td> 
   <td colname="col2"> <p>用於顏色空間轉換的絕對比色呈現意圖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>色彩空間轉換的飽和度渲染意圖。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>禁用某些顏色轉換的黑點補償 </p> <p>預設情況下被啟用. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>顏色轉換時禁用抖動（誤差擴散）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> 禁用從CMYK到RGB的自動轉換。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>對JPEG輸入影像進行強制解碼和重新編碼。 </p> <p> <b>注意：</b> 應用此選項可能會降低影像質量。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">  — 下採樣2x2 </span> </p> </td> 
   <td colname="col2"> <p>使用標準質量（雙線性）重採樣濾波器。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">  — 下採樣8x8 </span> </p> </td> 
   <td colname="col2"> <p>使用更高質量（Lanczos窗口）重新取樣過濾器（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>使用更高質量(FlashPix)重新取樣過濾器。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8雙斜面銳 </span> </p> </td> 
   <td colname="col2"> <p>使用Photoshop式8x8雙立方銳濾波器進行降採樣。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nousage </span> </p> </td> 
   <td colname="col2"> <p> 如果指定為第一個選項，則在遇到無效選項時取消使用資訊的輸出。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -覆寫 </span> </p> </td> 
   <td colname="col2"> <p>允許覆蓋現有 <span class="codeph"> <span class="varname"> 目標檔案 </span> </span>。 預設情況下，在檔案名後附加一個數字尾碼以防止覆蓋。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 斯基夫登 </span> </p> </td> 
   <td colname="col2"> <p>忽略隱藏的源檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">  — 連續錯誤 </span> </p> </td> 
   <td colname="col2"> <p>發生錯誤時不停止處理。 僅在處理多個檔案時有效。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph">  — 日誌檔案&lt; <span class="varname"> 檔案 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>日誌檔案的路徑和名稱(預設為 <span class="codeph"> 施圖 </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> 級別 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>日誌級別。 </p> 
   <p>&lt; 0 — 記錄已禁用。</p>
   <p>0 — 列出要處理的檔案。</p>
   <p>1 — 添加不需要的檔案的報告。</p>
   <p>2 — 添加進度報告。</p>
   <p>3 — 添加遇到的每個檔案的報告。</p>
   <p>4 — 添加檔案級進度報告。</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>追加到日誌檔案（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>覆蓋日誌檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressssec &lt; <span class="varname"> 毫秒 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>日誌級別2及更高級別（預設為3000）的日誌記錄間隔（毫秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> 位元組 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>記憶體使用限制。 必須至少為10 MB。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> 百分比 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>記憶體使用限制。 預設為物理記憶體的25%。 如果兩者都不 <span class="codeph"> 最大記憶 </span> 無 <span class="codeph"> 最大門 </span> 顯式設定使用maxmempercent預設值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -版本 </span> </p> </td> 
   <td colname="col2"> <p> 返回此實用程式的版本資訊。 不使用其他選項指定。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 支援的輸入影像格式 {#section-ab13d941d6724e65b9f84b62d949d31c}

下表列出了IC支援的影像檔案格式和格式選項。

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> 格式</b> </p> </th> 
   <th class="entry"> <p> <b> 像素類型</b> <b> 比特/陳</b> </p> </th> 
   <th class="entry"> <p> <b> 比特/陳</b> </p> </th> 
   <th class="entry"> <p> <b> 壓縮</b> </p> </th> 
   <th class="entry"> <p> <b> 附註</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> （Windows點陣圖） </p> </td> 
   <td> <p> RGB |已索引 </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> 未壓縮 | RLE </p> </td> 
   <td> <p> 5/6位/通道表示支援16位RGB（5-5-5和5-6-5位/通道）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> （封裝後指令碼） </p> </td> 
   <td> <p> CMYK |RGB |灰色 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII碼 | ASCII85 |二進位 |JPEG </p> </td> 
   <td> <p> 僅支援由Photoshop生成的EPS檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
   <td> </td> 
  </tr> 
  <tr> 
   <td> <p> CompuServe </p> <b>GIF</b> </td> 
   <td> <p> 索引 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> LZW </p> </td> 
   <td> <p> 如果存在，則調色板中的透明度值將轉換為Alpha。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK |RGB |灰色 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK | CMYKA |RGB | RGBA |灰色 | grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 未壓縮 |壓縮 </p> </td> 
   <td> <p> 僅合併影像；將忽略圖層和額外通道。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>皮克</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> 勒 </p> </td> 
   <td> <p> 僅點陣圖資料；將忽略向量資料。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB | RGBA |灰色 | grayA |已索引 </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> 已壓縮 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK | CMYKA |RGB | RGBA |灰色 | grayA |已索引 </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 未壓縮 | ZIP | LZW |JPEG | CCITT RLE | CCITT G3 | CCITT G4 |包位 </p> </td> 
   <td> <p> 除第一個關聯的Alpha通道外，忽略額外的通道。 </p> </td> 
  </tr> 
 </tbody> 
</table>

嵌入式ICC配置檔案在EPS、JPG、PSD、PNG和TIFF檔案中可識別。

嵌入的路徑XMP和元資料在EPS、JPG、PSD和TIFF檔案中可識別。

## 範例 {#section-3c1986b30315431989bd76b1ee5bef6d}

以最佳質量轉換單個影像，並將其保留在同一資料夾中：

`ic -convert src/myFile.png src/myFile.tif`

轉換中的所有影像 *`srcFolder`* 到JPEG編碼的金字塔TIFF和 *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

轉換中的所有影像 *`srcFolder`*。 JPG檔案的編碼影像資料用於這些影像金字塔的其餘部分以及所有非JPG輸入檔案的整個輸出影像的全解析度級無損LZW壓縮。 像素類型、嵌入的顏色配置XMP檔案、元資料等。 保留。

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
