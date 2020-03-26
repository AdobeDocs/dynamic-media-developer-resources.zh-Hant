---
description: 映像轉換實用程式。
seo-description: 映像轉換實用程式。
seo-title: ic
solution: Experience Manager
title: ic
topic: Scene7 Image Serving - Image Rendering API
uuid: 08fabcc9-d0b5-4136-81fc-ac896c341e1d
translation-type: tm+mt
source-git-commit: e0f8153b038446180ddad313e591828223ed31e9

---


# ic {#ic}

映像轉換實用程式。

`ic` 是命令行工具，可將影像檔案轉換為優化的金字塔TIFF格式(PTIFF)。 雖然「影像伺服」可以處理影像而不需轉換，但建議您將所有大於512x512像素的影像轉換為PTIFF。 此轉換可確保最佳的伺服器效能和資源使用，並將回應時間減至最少。

建議包含像片內容的PTIFF檔案採用JPEG編碼(請指 `-jpegcompress`定)。 電腦生成的內容可以受益於無損壓縮( `-deflatecompress` 或 `-lzwcompress`)。 除非需要色彩轉換或像素類型轉換，否則JPEG原始影像資料會在不進行解碼的情況下傳輸至PTIFF，以避免品質降低。 在這種情況下，指定的壓縮選項僅適用於低解析度金字塔級。

如果您不要轉換大型影像，則不需要設定控制使用記憶體量的參數。 但是，如果您是，請使 `ic` 用下面所述的設 `-maxmem` 置來提供更多記憶體。 計算所需記憶體量的一個好經驗法則是將影像寬度乘以影像高度乘以通道數。 例如，若RGB影像是Alpha乘以3，則為4。 此外，如果通道是每個元件16位，而不是最終結果的8倍。

## 使用 {#section-fb5293fa79894442aba831c1e14c5cc9}

`ic -convert` `[`*`options`*`]` *`sourceFiledestFile`*

` ic -convert` `[`*`options`*`]` *`sourceFolderdestFolder`*

` -c -convert` `[`*`options`*`]` *`sourceFiledestFolder`*

<table id="table_E368E220299D449D8311478AB5042987"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> 選 <span class="varname"><i>項</i></span></span> </p> </td> 
   <td colname="col2"> <p>命令選項（請參閱下面）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"> sourceFile <i></i></span></span> </p> </td> 
   <td colname="col2"> <p>單一輸入影像檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> destFile <span class="varname"><i></i></span></span> </p> </td> 
   <td colname="col2"> <p>單一輸出PTIFF檔案（如果與SourceDirectory搭配使用則無效）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> <span class="varname"><i>sourceFolder</i></span></span> </p> </td> 
   <td colname="col2"> <p>包含輸入影像的資料夾。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> destFolder <span class="varname"><i></i></span></span> </p> </td> 
   <td colname="col2"> <p>輸出PTIFF檔案寫入的資料夾。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## Returns {#section-36a2dcfa39824d29b69547c432366219}

0（如果成功）。 如果發生錯誤，則會傳回非零值，並傳送錯誤詳細資訊給 `stderr`。

## 選項 {#section-df311ace43f947b3817b60b667ae04ca}

<table id="table_02011C7C076745A8BF4378B22C48C8A3"> 
 <tbody> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -未壓縮 </span> </p> </td> 
   <td colname="col2"> <p>不要壓縮輸出影像。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -deflatecompress </span> </p> </td> 
   <td colname="col2"> <p>使用平減(zip)壓縮（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -lzwcompress </span> </p> </td> 
   <td colname="col2"> <p>使用Lempel-Ziv-Welch(LZW)壓縮。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegcompress </span> </p> </td> 
   <td colname="col2"> <p>使用JPEG編碼。 如果sourceFile包 <span class="codeph"> 含alpha <span class="varname"> 資 </span> 料，則 </span> 會忽略此點。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -jpegquality &lt; <span class="varname"> 質量 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>JPEG品質(0-100;預設值為95)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -fullsamplechrominance </span> </p> </td> 
   <td colname="col2"> <p>停用JPEG色度縮減取樣（可改善色彩文字和圖形的品質）。 這對CMYK或灰階的輸出影像沒有影響。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -usm &lt; <span class="varname"> amount </span>&gt; &lt; <span class="varname"> radius </span>&gt; &lt; &lt; <span class="varname"> monochreshold </span><span class="varname"></span>&gt; &lt;單色 </span> </p> </td> 
   <td colname="col2"> <p>將非銳利遮色片套用至子取樣金字塔層級。 如需詳 <a href="../../../is-api/http-ref/image-serving-api-ref/c-http-protocol-reference/c-command-reference/r-op-usm.md#reference-51ac75adadfe4346ab60953192d0a1aa" type="reference" format="dita" scope="local"> 細資訊，請參 </a> 閱op_usm=。 （未套用至完整解析度的影像）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -applyClippath </span> </p> </td> 
   <td colname="col2"> <p>使用來源檔案中的剪輯路徑（如果有的話）來建立相關的Alpha資料。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -dpi &lt; <span class="varname"> dpi </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>目的檔的列印解析 <span class="codeph"> 度( <span class="varname"> dpi) </span></span>;如果未指定，則srcFile的打印解 <span class="codeph"> 析度 </span> 將複製到 <span class="codeph"> 目標 <span class="varname"> 檔案 </span></span>。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -autocrop &lt; <span class="varname"> &gt; &lt; </span>corner mode&gt; &lt; <span class="varname"> tolerance </span>&lt; <span class="varname"> infoFile </span><span class="varname"></span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>計算裁切矩形，將純色背景減到最小。 如果自動裁切演算法會導致整個影像遭到裁切，則不會輸出裁切資訊。 </p> <p>若要計算裁切矩形而不轉換影像，請指定 <span class="codeph"> -autocrop(不 </span> 使用 <span class="codeph"> -convert) </span> 和不使用 <span class="codeph"> dest <span class="varname"> File)。</span> </span></p>

<p><i><b>corner</b></i> - ul| ur| ll| lr </p>
   <p> 指定使用種子點的影像的哪個角。 如果模式為1，則忽略。</p>
   <p><i><b>mode</b></i> - 0| 1</p>
   <p>設為0可根據指定角像素的顏色進行裁切；如果alpha資料與來源影像相關聯，則可處理預先乘積的色彩資料。</p>
   <p>設為1以根據Alpha資料裁切；corner被忽略，0總是種子值；如果源影像沒有與alpha資料關聯，則不應用裁切。</p> 
   <p><i><b>容差</b></i> -匹配容差。 實際值0.0到1.0。指定匹配像素元件值的公差。 設定為0以取得完全相符項目。</p>
   <p><i><b>infoFile</b></i> —— 要向其寫入裁切資訊資料的XML輸出檔案的路徑和名稱。</p>

<p>  
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedXmpData </span> </p> </td> 
   <td colname="col2"> <p>將XMP中繼資料（如果有）從sourceFile複製 <span class="codeph"> 至目的檔案， <span class="varname"> 不需 </span> 進行任何 </span><span class="codeph"><span class="varname"></span></span> 修改。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -embedColorProfile </span> </p> </td> 
   <td colname="col2"> <p> 將ICC色彩描述檔內嵌 <span class="codeph"> 在目 <span class="varname"> 的 </span></span>檔案中（如果可用）（預設未內嵌描述檔）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -imageprofile &lt; <span class="varname"> 檔案 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC配置檔案的路徑和名稱。 定義sourceFile的色域 <span class="codeph"> , <span class="varname"> 且 </span></span> 必須符合其像素類型。 只有在源檔案中未嵌入配置式時才應 <span class="codeph"> 指 <span class="varname"> 定 </span></span>，因為這會覆蓋嵌入的配置檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -viewprofile &lt; <span class="varname"> 檔案 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>ICC配置檔案的路徑和名稱。 定義目標檔案的像素類 <span class="codeph"> 型和 <span class="varname"> 色域 </span></span>。 如果sourceFile具有嵌入的配 <span class="codeph"> 置檔案，或 <span class="varname"> 者也指定了 </span> -imageprofile,IC將 </span><span class="codeph"></span> 轉換為此配置檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentEncertable </span> </p> </td> 
   <td colname="col2"> <p>色彩空間轉換的感性演算方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentRelBoryic </span> </p> </td> 
   <td colname="col2"> <p> 色彩空間轉換的相對比色演算方式（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentAbsBoryticle </span> </p> </td> 
   <td colname="col2"> <p>色彩空間轉換的絕對比色演算方式。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -intentSaturation </span> </p> </td> 
   <td colname="col2"> <p>飽和度演算色彩空間轉換的「方式」。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoBlackPointCompensation </span> </p> </td> 
   <td colname="col2"> <p>停用特定色彩轉換的黑點補償 </p> <p>預設情況下被啟用. </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -cmsNoDither8 </span> </p> </td> 
   <td colname="col2"> <p>在色彩轉換時停用混色（錯誤擴散）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maintainpixeltype </span> </p> </td> 
   <td colname="col2"> <p> 停用從CMYK到RGB的自動轉換。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> - forceJPEGDecompress </span> </p> </td> 
   <td colname="col2"> <p>強制解碼JPEG輸入影像並重新編碼。 </p> <p> <b>注意：</b> 套用此選項可能會降低影像品質。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample2x2 </span> </p> </td> 
   <td colname="col2"> <p>使用標準品質（雙線性）重新取樣濾鏡。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8 </span> </p> </td> 
   <td colname="col2"> <p>使用較高品質（Lanczos視窗）重新取樣濾鏡（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8FlashPix </span> </p> </td> 
   <td colname="col2"> <p>使用更高品質(FlashPix)重新取樣濾鏡。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -downsample8x8BicubicSharp </span> </p> </td> 
   <td colname="col2"> <p>使用Photoshop樣式8x8雙立方體銳利濾鏡縮減取樣。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -年齡 </span> </p> </td> 
   <td colname="col2"> <p> 當指定為第一個選項時，在遇到無效選項時隱藏使用資訊的輸出。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -覆寫 </span> </p> </td> 
   <td colname="col2"> <p>允許覆寫現有的目 <span class="codeph"> 標 <span class="varname"> 檔案 </span></span>。 預設情況下，檔案名中會附加一個數字尾碼以防止覆寫。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -skiphiddend </span> </p> </td> 
   <td colname="col2"> <p>忽略隱藏的源檔案。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -continueonerror </span> </p> </td> 
   <td colname="col2"> <p>發生錯誤時，請勿停止處理。 只有在處理多個檔案時才有效。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logfile &lt;文 <span class="varname"> 件&gt; </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>日誌檔案的路徑和名稱(預設為 <span class="codeph"> stdout </span>)。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -loglevel &lt; <span class="varname"> 級別 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>記錄層級。 </p> 
   <p>&lt; 0 —— 禁用記錄。</p>
   <p>0 —— 列出要處理的檔案。</p>
   <p>1 —— 新增不需要的檔案的報表。</p>
   <p>2 —— 添加進度報告。</p>
   <p>3 —— 新增遇到的每個檔案的報表。</p>
   <p>4 —— 在檔案級別添加進度報告。</p>
   <p> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logappend </span> </p> </td> 
   <td colname="col2"> <p>附加至記錄檔（預設）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -nologappend </span> </p> </td> 
   <td colname="col2"> <p>覆寫記錄檔。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -logprogressmsec &lt; <span class="varname"> msec </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>日誌級別2和更高版本（預設為3000）的日誌間隔（毫秒）。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmem &lt; <span class="varname"> 位元組 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>記憶體使用量限制。 必須至少為10 MB。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -maxmempercent &lt; <span class="varname"> 百分比 </span>&gt; </span> </p> </td> 
   <td colname="col2"> <p>記憶體使用量限制。 預設為物理記憶體的25%。 如果未明 <span class="codeph"> 確設 </span> 置 <span class="codeph"> maxmem和 </span> maxmempercent ，則使用maxmempercent預設值。 </p> </td> 
  </tr> 
  <tr> 
   <td colname="col1"> <p> <span class="codeph"> -版本 </span> </p> </td> 
   <td colname="col2"> <p> 返回此實用程式的版本資訊。 不使用其他選項指定。 </p> </td> 
  </tr> 
 </tbody> 
</table>

## 支援的輸入影像格式 {#section-ab13d941d6724e65b9f84b62d949d31c}

下表列出IC支援的影像檔案格式和格式選項。

<table id="table_1EB2B60993D34B1887275EA4E3491401"> 
 <thead> 
  <tr> 
   <th class="entry"> <p> <b> 格式</b> </p> </th> 
   <th class="entry"> <p> <b> 像素類型</b><b> Bits/Chan</b> </p> </th> 
   <th class="entry"> <p> <b> 比特／陳</b> </p> </th> 
   <th class="entry"> <p> <b> 壓縮</b> </p> </th> 
   <th class="entry"> <p> <b> 附註</b> </p> </th> 
  </tr> 
 </thead>
 <tbody> 
  <tr> 
   <td> <b> BMP</b> <p> （Windows點陣圖） </p> </td> 
   <td> <p> RGB|索引 </p> </td> 
   <td> <p> 1 | 5/6 | 8 </p> </td> 
   <td> <p> 解壓縮| RLE </p> </td> 
   <td> <p> 5/6位／通道表示支援16位RGB（5-5-5和5-6-5位／通道）。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> EPS</b> <p> （封裝的Postscript） </p> </td> 
   <td> <p> CMYK| RGB|灰色 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> ASCII| ASCII85|二進位| JPEG </p> </td> 
   <td> <p> 僅支援Photoshop產生的EPS檔案。 </p> </td> 
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
   <td> <p> 如果存在，則調色板中的透明度值將轉換為alpha。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> JPG</b> <p> (JFIF/JPEG) </p> </td> 
   <td> <p> CMYK| RGB|灰色 </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> JPEG </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Photoshop </p> <b>PSD</b> </td> 
   <td> <p> CMYK| CMYKA| RGB| RGBA|灰色| grayA </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 解壓縮|壓縮 </p> </td> 
   <td> <p> 僅合併影像；圖層和額外的色版會被忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <p> Macintosh </p> <b>PICT</b> </td> 
   <td> <p> RGB </p> </td> 
   <td> <p> 8 </p> </td> 
   <td> <p> RLE </p> </td> 
   <td> <p> 僅點陣圖資料；向量資料會被忽略。 </p> </td> 
  </tr> 
  <tr> 
   <td> <b> PNG</b> </td> 
   <td> <p> RGB| RGBA|灰色| grayA|索引 </p> </td> 
   <td> <p> 1 | 2 | 4 | 8 | 16 </p> </td> 
   <td> <p> 已壓縮 </p> </td> 
   <td> <p> </p> </td> 
  </tr> 
  <tr> 
   <td> <b> TIFF</b> </td> 
   <td> <p> CMYK| CMYKA| RGB| RGBA|灰色| grayA|索引 </p> </td> 
   <td> <p> 1 | 8 | 16 </p> </td> 
   <td> <p> 解壓縮| ZIP| LZW| JPEG| CCITT RLE| CCITT G3| CCITT G4|包位 </p> </td> 
   <td> <p> 除了第一個相關的alpha頻道外，會忽略額外的頻道。 </p> </td> 
  </tr> 
 </tbody> 
</table>

內嵌的ICC描述檔可在EPS、JPG、PSD、PNG和TIFF檔案中辨識。

內嵌路徑和XMP中繼資料可在EPS、JPG、PSD和TIFF檔案中辨識。

## 範例 {#section-3c1986b30315431989bd76b1ee5bef6d}

以最佳品質轉換單一影像，並將它保留在相同的檔案夾中：

`ic -convert src/myFile.png src/myFile.tif`

將所有影像轉 *`srcFolder`* 換為JPEG編碼的金字塔TIFF，並置入 *`destFolder`*:

`ic -convert -jpegcompress -jpegquality 90 -overwrite -continueOnError srcFolder destFolder`

轉換所有影像 *`srcFolder`*。 JPG檔案的編碼影像資料用於這些影像金字塔的其餘影像以及所有非JPG輸入檔案的整個輸出影像的全解析度、無損的LZW壓縮。 像素類型、內嵌的色彩描述檔、XMP中繼資料等。 中。

`ic -convert -lzwcompress -embedXmpData -embedColorProfile -maintainpixeltype -overwrite -continueOnError srcFolder destFolder`
