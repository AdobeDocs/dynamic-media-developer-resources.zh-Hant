---
description: 使用Dynamic Media影像伺服時，應考慮一些限制和已知問題。
solution: Experience Manager
title: 限制與已知問題
feature: Dynamic Media Classic,SDK/API
role: Developer,Business Practitioner
translation-type: tm+mt
source-git-commit: f6c97606d7a4209427316d7367013ad9585a5cae
workflow-type: tm+mt
source-wordcount: '1238'
ht-degree: 0%

---


# 限制與已知問題{#restrictions-and-known-issues}

使用Dynamic Media影像伺服時，應考慮一些限制和已知問題。

## 文檔勘誤表{#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 行數不會超過文本輸入中`\copyfitmaxlines`設定的最大值和顯式行數。
* 影像集中需要符合大括弧和括弧。 如果大括弧和括弧不符，則需要URL編碼。
* 伺服器端全域回應時間警報包含錯誤回應。
* 當將`rect=`命令與影像或遮色片請求搭配使用時，目前需要`id=`命令。

## 已知差異textPs=與text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 合成斜體的呈現效果比使用`text=`時要小。
* 與使用`text=`時相比，加底線會稍低和更薄。
* `\expnd` 並 `\expndtw` 搭配使用高負值時，會使字元在使用時彼此置於前面 `text=`。

* `\charscaley` 縮放比例與使用時不 `text=` 同，但不會影響線高。

* 如果最後一行文字不符合，則會捨棄整行文字，而非顯示為截止。
* `\slmult` 而且 `\sl` 其行為與MS Word不同 `text=`，而且只會對目前和後續段落生效。

* `\sb` MS Word和Adobe InDesign和Photoshop的第 `text=`一段則不適用。

* `\sa` 適用於MS Word和Adobe InDesign和Photoshop `text=`的最後一段。

## 向後相容性{#section-a76842f751944f4fb664af296d064122}

* 轉義RTF字串中的下划線字元(`\_`)不適用於使用`textPs=`的所有字型

* 支援非區分大小寫的巨集處理。
* 目錄快取已從60秒縮減為10秒。
* 錯誤重新導向功能現在只會重新導向參照已發佈在目錄中、但在磁碟上找不到的損毀影像、字型、色彩描述檔和影像的請求。
* `posN=`、、 `anchor=`、 `anchorN=`、 `origin=` `originN=` 和現在，如果任何修飾詞值大於2147483648，則返回解析錯誤。

* 不支援巢狀請求的編碼。 轉換為新行為，並解除編碼您網站和公司目錄中URL請求中的任何巢狀請求值。
* 現在，使用`req=tmb`時，DefaultImage會套用縮圖屬性。
* 在使用`flip=`的舊版中，無論錨點是什麼，都不會重新定位影像。

## 適用於第三方程式庫{#section-79768b96bf634e44ab672c5b893f343d}的限制

如果已檢測到Digimarc水印，Digimarc庫拒絕將Digimarc水印應用於影像。 如果對主要影像進行了足夠的編輯，Digimarc程式庫仍可識別已套用水印。 但是，它可能無法讀取該資訊。 這會產生新影像，而無法取得套用至原始影像的原始Digimarc資訊。 「影像伺服」現在可以套用公司目錄中定義的Digimarc浮水印。

## 影像伺服和影像轉譯適用的限制{#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* 當有4個以上的CPU可用時，影像伺服和影像演算可能無法充分運用所有CPU。 模擬這些電腦上的流量，以瞭解4個以上CPU的優勢。
* 傳回重新導向的遠端URL（HTTP狀態301、302或303）會遭拒。
* 配置`errorRedirect.rootUrl`時，此屬性中定義的IP地址需要包含在該伺服器上的規則集`<addressfilter>`標籤值中。

   *範例*:

   伺服器A已定義`errorRedirect.rootUrl=10.10.10.10`。

   伺服器B的IP地址為10.10.10.10，將規則集檔案中的`<addressfilter>`標籤值設定為包含其IP地址(10.10.10.10)。

* 具有定位的點文字和文字路徑可能會顯示剪裁。
* `text=` 僅適 `\sa` 用於 `\sb` 和整個文本塊，而不適用於每個段落。

* 當使用URL中定義的一家公司和為`src=`或`mask=`修飾詞定義的另一家公司時，您必須在為`src=`或`mask=`定義的公司加上正斜線，才能使用這種形式的請求。

   *範例*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   而不是：`/is/image/MyCompany?src=YourCompany/MyImage`。

* 非吡唑化Tiff或暈映請求會產生類似的錯誤訊息，

   *「影 `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` 像沒有有效的DSF,2.25MPixel的面積超過2MPixel的最大面積* 。」

   最佳做法是使用吡唑並Tiff和暗角。 如果您需要使用非吡唑並獒犬，請依照下列指示增加大小限制。

   *周旋工作*:

   對於影像渲染非吡唑化暈映，請在[!DNL install_root/ImageServing/bin/ImageServerRegistry.xml]配置檔案中增加IrMaxNonPyrVignetteSize的屬性值。

   對於「影像伺服非吡唑化TIFF」，請增加[!DNL install_root/ImageServing/bin/ImageServerRegistry.xml]組態檔中`MaxNonDsfSize`的屬性值。

* Adobe PhotoshopCS3預設不會儲存圖層PSD檔案的合成影像。

   *症狀*:

   Adobe PhotoshopCS3圖層PSD檔案會顯示為黑色，並加上文字，指出「此圖層Photoshop檔案未與合成影像一起儲存」。 用於「影像伺服」回覆影像或IPS中。

   *解決辦法*︰

   開啟最大化的相容性，以儲存Adobe PhotoshopCS3檔案。

* 將ICC描述檔指派給CMYK/JPEG回覆影像，會導致某些瀏覽器中的色彩反轉。*周旋工作*:

   使用`fmt=`變更回覆影像格式

* 壓縮後的HTTP回應影像資料（包括檔案標題）大小限制為16 MB。
* &quot;。.&quot; 不允許在HTTP請求中的任何路徑元素中。
* 卸載可從&#x200B;*[!DNL install_root]*&#x200B;或任何子資料夾中刪除用戶建立或修改的檔案。 在解除安裝之前，請將這些檔案複製到其他位置。

## 僅適用於影像伺服{#section-b08ad535e4454265b8157dec244c4faf}的限制

* PhotoFont文字不支援RTF(`\cf`)命令中的前景色。
* 合成粗體、斜體和粗體／斜體將作為PhotoFont文本的錯誤被拒絕。
* PhotoFont文字不支援垂直文字排列。
* 16bpc PNG影像不支援PhotoFont文字。
* 使用硬式編碼選項，針對內嵌色彩描述檔的PNG影像進行色彩校正。 演算方式是相對比色，而PhotoFont文字則會開啟黑點補償。
* 在公司[!DNL ini]檔案中啟用地區轉譯時，不支援檔案式查閱。
* 影像伺服無法正確寫入非封閉的Photoshop路徑。
* 「影像伺服」目前不支援處理使用Adobe Media Encoder4.0.1或更舊版本匯出的TIFF檔案。 Adobe Media Encoder隨附於Premiere ProCS4、After EffectsCS4和Creative Suite4 Production Premium。
* 使用具有自調整圖層的`text=`不支援使用多個設定進行行對齊的RTF字串。

   *範例*

   RTF字串不能對自調整大小的文本圖層使用左右行對齊。

* SVG對於未嵌入SVG檔案的引用字型的字型查找路徑具有自己的屬性。

   *症狀*

   轉譯的包含字型定義的SVG影像使用的字型不正確。

   *解決方法*

   在[!DNL install_root/ImageServing/conf/PlatformServer.conf]中設定屬性`svgProvider.fontRoot=`。

* 裁切目前使用`bgColor=`取代`color=`來填滿任何新擴充的區域。

* 當`bgColor=`不符合包含色彩描述檔的基本色彩空間時，色彩轉換可能不正確。
* 如果圖層沒有遮色片或Alpha資料，則不會呈現外層效果。

## 僅適用於影像演算{#section-4c6949e797174607a3d1ab4d3d4a725a}的限制

* 壁板和壁材不可拆卸。
* 紋理的大小相對於暈映檢視的大小有限。 在少數情況下，視圖大小的預設限制為425%可能會干擾使用非常大型非重複紋理的應用程式。 如果無法將應用程式或內容變更為符合預先定義的限制，則可依下列方式增加百分比。 使用文本編輯器開啟[!DNL install_root/ImageServing/conf/ImageServerRegistry.xml] ，找到`IrMaxTextureSizeFactor`並輸入新的百分比值。 此更改將立即生效，而不重新啟動映像伺服器。

* Netscape和Opera中的JavaScript引擎會快取回應資料，即使已設定nocache標題亦然。 這會干擾狀態要求的正常運作。

   *解決方法*

   將時間戳記或其他唯一識別碼附加至請求字串，例如`"&.ts=currentTime`。

## 僅適用於實用程式{#section-906a6b2378154b3da122b2332983f7a5}的限制

`ImageConvert`有時會因區段錯誤而當機，而停止使用 `control-c`時
