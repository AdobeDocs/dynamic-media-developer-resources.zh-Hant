---
description: 使用Dynamic Media影像伺服時，應考量一些限制和已知問題。
solution: Experience Manager
title: 限制與已知問題
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '1235'
ht-degree: 0%

---

# 限制與已知問題{#restrictions-and-known-issues}

使用Dynamic Media影像伺服時，應考量一些限制和已知問題。

## 文檔勘誤表 {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 行數不會超過文本輸入中`\copyfitmaxlines`設定的最大值和顯式行數。
* 影像集中需要匹配大括弧和括弧。 如果大括弧和括弧不相符，則需進行URL編碼。
* 伺服器端全域回應時間警報包含錯誤回應。
* 將`rect=`命令與影像或遮罩請求一起使用時，當前需要`id=`命令。

## 已知差異textPs=與text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 合成斜體呈現的斜度比使用`text=`時要小。
* 與使用`text=`時相比，加底線要低一些，也要薄一些。
* `\expnd` 和 `\expndtw` 搭配高負值使用時，會在使用時讓字元彼此前 `text=`置。

* `\charscaley` 縮放比例與使用時 `text=` 不同，但不會影響線高。

* 如果最後一行文本不合格，則刪除整行，而不顯示為截止。
* `\slmult` 而且 `\sl` 行為與MS Word和不同 `text=`，它們只對當前段落和後續段落生效。

* `\sb` 適用於MS Word和的第一段， `text=`Adobe InDesign和Photoshop則不適用。

* `\sa` 適用於MS Word和、Adobe InDesign和 `text=`Photoshop的最後一段，則不會這麼做。

## 回溯相容性 {#section-a76842f751944f4fb664af296d064122}

* 對RTF字串中的下划線字元(`\_`)進行逸出時，無法使用`textPs=`的所有字型

* 支援不區分大小寫的宏處理。
* 目錄快取已從60秒縮短為10秒。
* 錯誤重新導向功能現在只會重新導向參考已發佈在目錄中但在磁碟上找不到的損壞影像、字型、顏色描述檔和影像的請求。
* `posN=`、  `anchor=`、  `anchorN=`、  `origin=`和現在會 `originN=` 在任何修飾詞值大於2147483648時傳回剖析錯誤。

* 不支援對巢狀請求進行編碼。 轉換為新行為，並取消編碼您網站和公司目錄中URL請求中找到的任何巢狀請求值。
* 現在使用`req=tmb`時，DefaultImage會套用縮圖屬性。
* 在使用`flip=`的舊版中，無論錨點是什麼，影像都不會重新定位。

## 適用於協力廠商程式庫的限制 {#section-79768b96bf634e44ab672c5b893f343d}

如果已檢測到影像，Digimarc庫拒絕將Digimarc水印應用到影像。 如果對主影像進行了足夠的編輯，則Digimarc庫仍可識別已應用水印。 但是，它可能無法讀取該資訊。 這會產生一個新影像，在該新影像中，無法獲取應用於原始影像的原始Digimarc資訊。 「影像伺服」現在可以套用公司目錄中定義的Digimarc浮水印。

## 影像提供和影像轉譯適用的限制 {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* 當有超過4個CPU可用時，影像提供和影像呈現可能無法充分利用所有CPU。 模擬這些電腦上的流量，以了解4個以上CPU的優勢。
* 傳回重新導向的遠端URL（HTTP狀態301、302或303）會遭拒。
* 配置`errorRedirect.rootUrl`時，此屬性中定義的IP地址需要包含在該伺服器上的規則集`<addressfilter>`標籤值中。

   *範例*:

   伺服器A已定義`errorRedirect.rootUrl=10.10.10.10` 。

   伺服器B的IP地址為10.10.10.10，在規則集檔案中設定`<addressfilter>`標籤值以包含其IP地址(10.10.10.10)。

* 具有定位的點文本和文本路徑可以顯示剪切。
* `text=` 僅適 `\sa` 用於 `\sb` 整個文字區塊，而非依照段落。

* 使用URL中定義的公司和為`src=`或`mask=`修飾詞定義的其他公司時，您必須為為`src=`或`mask=`定義的公司加上正斜線，才能使這種形式的請求生效。

   *範例*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   而非：`/is/image/MyCompany?src=YourCompany/MyImage` 。

* 非吡唑化Tiff或暈映請求會產生類似的錯誤訊息，如下

   *「影 `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` 像沒有有效的DSF，且2.25MPixel的面積超過最大2MPixel」* 。

   最佳作法是使用漸變Tiff和暈映。 如果您需要使用非縮圖或暈圖，請依照下列指示增加大小限制。

   *解決*:

   對於影像呈現非吡唑並字暈，請增加[!DNL install_root/ImageServing/bin/ImageServerRegistry.xml]配置檔案中IrMaxNonPyrVignetteSize的屬性值。

   對於「影像伺服」未隱藏的TIFF，請增加[!DNL install_root/ImageServing/bin/ImageServerRegistry.xml]配置檔案中`MaxNonDsfSize`的屬性值。

* Adobe Photoshop CS3預設不會儲存複合影像的分層PSD檔案。

   *症狀*:

   Adobe Photoshop CS3分層PSD檔案顯示為黑色，並顯示「此分層Photoshop檔案未與複合影像一起儲存」文字。 用於「影像服務」回復影像或IPS中。

   *解決辦法*︰

   儲存Adobe Photoshop CS3檔案，並開啟最大程度的相容性。

* 將ICC配置檔案分配給CMYK/JPEG回復影像會導致某些瀏覽器中的顏色反轉。*解決*:

   使用`fmt=`變更回覆影像格式

* 壓縮後HTTP回應影像資料（包括檔案標題）的大小上限為16 MB。
* &quot;。.&quot; 在HTTP要求中的任何路徑元素中皆不允許。
* 卸載可從&#x200B;*[!DNL install_root]*&#x200B;或任何子資料夾中刪除用戶建立或修改的檔案。 在卸載前將此類檔案複製到其他位置。

## 僅適用於影像伺服的限制 {#section-b08ad535e4454265b8157dec244c4faf}

* PhotoFont文本不支援RTF(`\cf`)命令中的前景顏色。
* 合成粗體、斜體和粗體/斜體將作為PhotoFont文本的錯誤而被拒絕。
* PhotoFont文字不支援垂直文字流。
* 16bpc PNG影像不支援PhotoFont文字。
* 使用硬式編碼選項對具有內嵌顏色描述檔的PNG影像進行色彩校正。 渲染目的是相對比色，並且為PhotoFont文本開啟黑點補償。
* 在公司[!DNL ini]檔案中啟用地區轉換時，不支援基於檔案的查找。
* 影像伺服無法正確寫入非封閉的Photoshop路徑。
* 影像伺服目前不支援處理使用Adobe Media Encoder 4.0.1或更舊版本匯出的TIFF檔案。 Adobe Media Encoder隨附於Premiere ProCS4、After Effects CS4和Creative Suite4 Production Premium。
* 使用`text=`和自調整層時不支援使用多個設定進行行對齊的RTF字串。

   *範例*

   RTF字串不能同時使用左行和右行對齊來自行調整文本層。

* SVG對於未嵌入到SVG檔案中的引用字型的字型查找路徑具有其自己的屬性。

   *症狀*

   包含字型定義的已呈現SVG影像正在使用不正確的字型。

   *因應措施*

   在[!DNL install_root/ImageServing/conf/PlatformServer.conf]中設定屬性`svgProvider.fontRoot=` 。

* 裁切目前使用`bgColor=`（而非`color=`）來填滿任何新擴展的區域。

* 當`bgColor=`與涉及顏色輪廓的基本顏色空間不匹配時，顏色轉換可能不正確。
* 如果圖層沒有蒙版或Alpha資料，則不呈現外層效果。

## 僅適用於影像呈現的限制 {#section-4c6949e797174607a3d1ab4d3d4a725a}

* 壁板和壁材不可移除。
* 紋理的大小相對於暈映視圖的大小是有限的。 在少數情況下，425%的預設檢視大小限制可能會干擾使用非常大且不可重複的紋理的應用程式。 如果無法將應用程式或內容變更為在預先定義的限制內運作，百分比可增加如下。 使用文本編輯器，開啟[!DNL install_root/ImageServing/conf/ImageServerRegistry.xml]，找到`IrMaxTextureSizeFactor`並輸入新的百分比值。 更改將立即生效，而不重新啟動映像伺服器。

* 即使已設定nocache標頭，Netscape和Opera快取回應資料中的JavaScript引擎也會。 這會干擾有狀態要求的正常運作。

   *因應措施*

   將時間戳記或其他唯一識別碼附加至請求字串，例如`"&.ts=currentTime`。

## 僅適用於實用程式的限制 {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`有時當機時會發生分段錯誤，當停止時會出現 `control-c`。
