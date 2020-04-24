---
description: 使用Scene7 Image Serving時，應考慮一些限制和已知問題。
seo-description: 使用Scene7 Image Serving時，應考慮一些限制和已知問題。
seo-title: 限制與已知問題
solution: Experience Manager
title: 限制與已知問題
topic: Scene7 Image Serving - Image Rendering API
uuid: 9f9fad41-4828-4fba-8f5f-2c33e7811c71
translation-type: tm+mt
source-git-commit: a47f2b4ef8ebef0c8218dafa4678443aa61241f5

---


# 限制與已知問題{#restrictions-and-known-issues}

使用Scene7 Image Serving時，應考慮一些限制和已知問題。

## 檔案勘誤表 {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 行數不會超過文字輸入中設 `\copyfitmaxlines` 定和明確行數的上限。
* 影像集中需要符合大括弧和括弧。 如果大括弧和括弧不符，則需要URL編碼。
* 伺服器端全域回應時間警報包含錯誤回應。
* 當使 `id=` 用命令搭配影像或遮色片要求 `rect=` 時，目前需要此命令。

## 已知差異文字Ps=與文字= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 合成斜體的呈現效果比使用時要小 `text=`。
* 加底線比使用時要低一點，也要薄一點 `text=`。
* `\expnd` 而 `\expndtw` 且搭配使用高負值時，會使字元在使用時彼此前置 `text=`。

* `\charscaley` 縮放比例與使用時不 `text=` 同，但不會影響行高。

* 如果最後一行文字不符合，則會捨棄整行文字，而非顯示為截止。
* `\slmult` 而且 `\sl` 其行為與MS Word不同 `text=`，而且只會對目前和後續段落生效。

* `\sb` 同時套用至MS Word和Adobe InDesign `text=`和Photoshop的第一段。

* `\sa` 同時套用至MS Word和Adobe InDesign `text=`和Photoshop的最後一段。

## 向後相容性 {#section-a76842f751944f4fb664af296d064122}

* 轉義RTF字串中的底線字 `\_`元()不適用於所有使用 `textPs=`

* 支援非區分大小寫的巨集處理。
* 目錄快取已從60秒縮減為10秒。
* 錯誤重新導向功能現在只會重新導向參照已發佈在目錄中、但在磁碟上找不到的損毀影像、字型、色彩描述檔和影像的請求。
* `posN=`、 `anchor=`、 `anchorN=`、 `origin=``originN=` 和現在，如果任何修飾詞值大於2147483648，則返回解析錯誤。

* 不支援巢狀請求的編碼。 轉換為新行為，並解除編碼您網站和公司目錄中URL請求中的任何巢狀請求值。
* DefaultImage現在使用時會套用縮圖屬 `req=tmb`性。
* 在舊版中，不 `flip=`論錨點是什麼，都不會重新定位影像。

## 適用於協力廠商程式庫的限制 {#section-79768b96bf634e44ab672c5b893f343d}

如果已檢測到Digimarc水印，Digimarc庫拒絕將Digimarc水印應用於影像。 如果對主影像進行了足夠的編輯，Digimarc程式庫仍可識別已套用水印。 但是，它可能無法讀取該資訊。 這會產生新影像，而無法取得套用至原始影像的原始Digimarc資訊。 「影像伺服」現在可以套用公司目錄中定義的Digimarc浮水印。

## 影像伺服和影像演算適用的限制 {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* 當有4個以上的CPU可用時，影像伺服和影像演算可能無法充分運用所有CPU。 模擬這些電腦上的流量，以瞭解4個以上CPU的優勢。
* 傳回重新導向的遠端URL（HTTP狀態301、302或303）會遭拒。
* 配置此 `errorRedirect.rootUrl` 屬性中定義的IP地址時，該伺服器上的規則集標 `<addressfilter>` 記值中必須包含該地址。

   *範例*:

   伺服器A已定義 `errorRedirect.rootUrl=10.10.10.10` 。

   伺服器B的IP地址為10.10.10.10，將規則集檔案中的標籤值設定為包含其IP地址(10.10.10.10)。 `<addressfilter>`

* 具有定位的點文字和文字路徑可能會顯示剪裁。
* `text=` 僅適用於 `\sa` 和 `\sb` 整個文本塊，而不適用於每個段落。

* 當使用URL中定義的公司和為該或修飾詞定義的其他公司時，您必須在為此請求形式定義或為此請求形式定義的 `src=``mask=``src=``mask=` 公司前加上正斜線。

   *範例*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   而不是： `/is/image/MyCompany?src=YourCompany/MyImage` 。

* 非吡唑化Tiff或暈映請求會產生類似的錯誤訊息，

   *「影`C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt`像沒有有效的DSF,2.25MPixel的面積超過2MPixel的最大面積* 。」

   最佳做法是使用吡唑並Tiff和暗角。 如果您需要使用非吡唑並獒犬，請依照下列指示增加大小限制。

   *周旋工作*:

   對於影像渲染非吡唑化暈映，請在[!DNL *[!DNL install_root]*/ImageServing/bin/ ImageServerRegistry.xml]配置檔案中增加IrMaxNonPyrVignetteSize的屬性值。

   對於「影像伺服」非吡唑化TIFF，請增 `MaxNonDsfSize` 加[!DNL *[!DNL install_root]* /ImageServing/bin/ ImageServerRegistry.xml]組態檔中的屬性值。

* Adobe Photoshop CS3預設不會儲存圖層PSD檔案為複合影像。

   *症狀*:

   Adobe Photoshop CS3圖層PSD檔案會以黑色顯示，並加上「此圖層Photoshop檔案未與合成影像一起儲存」的文字。 用於「影像伺服」回覆影像或IPS中。

   *解決辦法*︰

   在開啟最大化相容性的情況下儲存Adobe Photoshop CS3檔案。

* 將ICC描述檔指派給CMYK/JPEG回覆影像，會導致某些瀏覽器中的色彩反轉。*周旋工作*:

   使用 `fmt=`

* 壓縮後的HTTP回應影像資料（包括檔案標題）大小限制為16 MB。
* &quot; ..&quot; 不允許在HTTP請求中的任何路徑元素中。
* 卸載可從或任何子資料夾中刪除用戶建立或 *[!DNL install_root]* 修改的檔案。 在解除安裝之前，請將這些檔案複製到其他位置。

## 僅適用於影像伺服的限制 {#section-b08ad535e4454265b8157dec244c4faf}

* PhotoFont文字不支援RTF( `\cf`)命令中的前景色。
* 合成粗體、斜體和粗體／斜體將作為PhotoFont文本的錯誤被拒絕。
* PhotoFont文字不支援垂直文字排列。
* 16bpc PNG影像不支援PhotoFont文字。
* 使用硬式編碼選項，針對內嵌色彩描述檔的PNG影像進行色彩校正。 演算方式是相對比色，而PhotoFont文字則會開啟黑點補償。
* 公司檔案中啟用地區轉譯時，不支援檔案式查 [!DNL ini] 閱。
* 「影像伺服」無法正確寫入非封閉的Photoshop路徑。
* 影像伺服目前不支援處理使用Adobe Media Encoder 4.0.1或更舊版本匯出的TIFF檔案。 Adobe Media Encoder隨附於Premiere Pro CS4、After Effects CS4和Creative Suite 4 Production Premium。
* 使 `text=` 用自調整圖層時不支援使用多個設定進行行對齊的RTF字串。

   *範例*

   RTF字串不能對自調整大小的文本圖層使用左右行對齊。

* SVG對於未嵌入SVG檔案的引用字型的字型查找路徑具有自己的屬性。

   *症狀*

   轉譯的包含字型定義的SVG影像使用的字型不正確。

   *解決方法*

   在[!DNL `svgProvider.fontRoot=` /ImageServing/conf/PlatformServer.conf]中設定 *[!DNL install_root]* 屬性。

* 裁切目前正在使 `bgColor=` 用，而 `color=` 非填滿任何新延伸區域。

* 當與涉及色彩描述檔的基 `bgColor=` 色空間不符時，色彩轉換可能不正確。
* 如果圖層沒有遮色片或Alpha資料，則不會呈現外層效果。

## 僅適用於影像演算的限制 {#section-4c6949e797174607a3d1ab4d3d4a725a}

* 壁板和壁材不可拆卸。
* 紋理的大小相對於暈映檢視的大小有限。 在少數情況下，視圖大小的預設限制為425%可能會干擾使用非常大型非重複紋理的應用程式。 如果無法將應用程式或內容變更為符合預先定義的限制，則可依下列方式增加百分比。 使用文本編輯器開啟[!DNL *[!DNL install_root]*/ImageServing/conf/ImageServerRegistry.xml]，找到並 `IrMaxTextureSizeFactor` 輸入新的百分比值。 此更改將立即生效，而不重新啟動映像伺服器。

* Netscape和Opera中的JavaScript引擎會快取回應資料，即使已設定nocache標題亦然。 這會干擾狀態要求的正常運作。

   *解決方法*

   將時間戳記或其他唯一識別碼附加至請求字串，例如 `"&.ts=currentTime`。

## 僅適用於實用程式的限制 {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`有時會因區段錯誤而當機，而停止使用 `control-c`時
