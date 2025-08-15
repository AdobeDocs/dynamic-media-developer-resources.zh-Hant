---
description: 使用Dynamic Media影像伺服時，有一些限制和已知問題需要考量。
solution: Experience Manager
title: 限制和已知問題
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: 4f81f755789613222a66bed2961117604ae19e62
workflow-type: tm+mt
source-wordcount: '1233'
ht-degree: 0%

---

# 限制和已知問題{#restrictions-and-known-issues}

使用Dynamic Media影像伺服時，有一些限制和已知問題需要考量。

## 檔案勘誤表 {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 行數未超過`\copyfitmaxlines`設定的上限以及文字輸入中的明確行數。
* 影像集中必須搭配大括弧和括弧。 如果大括弧和括弧不相符，則必須將URL編碼。
* 伺服器端全域回應時間警示包含錯誤回應。
* 將`id=`命令與影像或遮罩要求搭配使用時，目前需要`rect=`命令。

## 已知差異textPs=與text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 綜合斜體呈現的斜體比使用`text=`時少。
* 底線比使用`text=`時稍微低一點且更薄。
* `\expnd`和`\expndtw`搭配高負值使用時，導致字元在使用`text=`時彼此排在前。

* `\charscaley`的縮放比例與使用`text=`時不同，但不會影響行高。

* 如果文字的最後一行不符合，則會捨棄整行，而不會顯示為截斷。
* `\slmult`和`\sl`的行為與MS Word和`text=`不同，它們只會對目前和後續段落生效。

* `\sb`套用至MS Word和`text=`的第一段落，Adobe InDesign和[!DNL Photoshop]不執行此動作。

* `\sa`套用至MS Word和`text=`的最後一個段落，Adobe InDesign和[!DNL Photoshop]不執行此動作。

## 回溯相容性 {#section-a76842f751944f4fb664af296d064122}

* 在RTF字串中逸出底線字元( `\_`)不適用於使用`textPs=`的所有字型

* 支援不區分大小寫的巨集處理。
* 目錄快取已從60秒減少到10秒。
* 錯誤重新導向功能現在只會重新導向參考已發佈在目錄中但在磁碟上找不到之損毀影像、字型、色彩設定檔和影像的請求。
* 如果任何修飾元值大於2147483648，`posN=`、`anchor=`、`anchorN=`、`origin=`和`originN=`現在會傳回剖析錯誤。

* 不支援巢狀要求的編碼。 轉換至新行為，並對在網站上和公司目錄的URL請求中找到的所有巢狀請求值進行取消編碼。
* 使用`req=tmb`時，DefaultImage現在會套用縮圖屬性。
* 在先前使用`flip=`的版本中，無論錨點是什麼，都不會重新定位影像。

## 適用於協力廠商程式庫的限制 {#section-79768b96bf634e44ab672c5b893f343d}

Digimarc程式庫拒絕將Digimarc浮水印套用至已偵測到的影像。 如果對主要影像進行了足夠的編輯，Digimarc資料庫仍可能能夠識別已套用浮水印。 但是，它可能無法讀取該資訊。 這會導致無法取得套用至原始影像的原始Digimarc資訊的新影像。 「影像伺服」現在可以套用公司目錄中定義的Digimarc浮水印。

## 適用於影像提供與影像轉譯的限制 {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* 超過4個CPU可供使用時，「影像伺服」和「影像演算」可能無法充分利用所有CPU。 在這些電腦上模擬您的流量，瞭解它在4顆CPU以上時的優勢。
* 傳回重新導向（HTTP狀態301、302或303）的遠端URL會遭到拒絕。
* 設定`errorRedirect.rootUrl`時，此屬性中定義的IP位址必須包含在該伺服器上的規則集`<addressfilter>`標籤值中。

  *範例*：

  伺服器A已定義`errorRedirect.rootUrl=10.10.10.10` 。

  伺服器B的IP位址為10.10.10.10，將規則集檔案中的`<addressfilter>`標籤值設定為包含其IP位址(10.10.10.10)。

* 具有定位的點文字和文字路徑可能會顯示剪裁。
* `text=`只將`\sa`和`\sb`套用至整個文字區塊，而非每個段落。

* 使用在URL中定義的一個公司，以及為`src=`或`mask=`修飾元定義的另一個公司時，您必須將正斜線加到為`src=`或`mask=`定義的公司，此表單的請求才能運作。

  *範例*：

  `/is/image/MyCompany?src=/YourCompany/MyImage` 。

  而非： `/is/image/MyCompany?src=YourCompany/MyImage` 。

* 非金字塔Tiff或暈映請求會產生類似的錯誤訊息，以便

  *「影像`C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt`沒有有效的DSF，且2.25MPixel的區域超過最大值2MPixel」*。

  最佳實務建議使用金字塔Tiff和暈映。 如果您需要使用非金字塔形浮雕或暈映，請依照下列指示增加大小限制。

  *因應措施*：

  針對影像演算非金字塔暈映，請增加[!DNL install_root/ImageServing/bin/ImageServerRegistry.xml]組態檔中IrMaxNonPyrVignetteSize的屬性值。

  對於影像伺服非金字塔TIFF，請在`MaxNonDsfSize`設定檔中增加[!DNL install_root/ImageServing/bin/ImageServerRegistry.xml]的屬性值。

* Adobe [!DNL Photoshop] CS3預設不會儲存圖層式PSD檔案為複合影像。

  *症狀*：

  Adobe [!DNL Photoshop] CS3分層PSD檔案顯示為黑色，並含有文字指出：「此分層[!DNL Photoshop]檔案並未儲存為複合影像。」 用於「影像伺服」回覆影像或IPS。

  *解決辦法*︰

  儲存開啟最大相容性的Adobe [!DNL Photoshop] CS3檔案。

* 將ICC設定檔指派給CMYK/JPEG回覆影像，會導致某些瀏覽器中的顏色反轉。*因應措施*：

  使用`fmt=`變更回覆影像格式

* HTTP回應影像資料在壓縮後（包括檔案標頭）的大小上限為16 MB。
* 「 ..」 不允許在HTTP要求的任何路徑元素中使用。
* 解除安裝可能會從&#x200B;*[!DNL install_root]*&#x200B;或任何子資料夾中移除使用者建立或修改的檔案。 在解除安裝之前，將此類檔案複製到其他位置。

## 僅適用於影像伺服的限制 {#section-b08ad535e4454265b8157dec244c4faf}

* PhotoFont文字不支援RTF ( `\cf`)命令中的前景色彩。
* 合成粗體、斜體和粗體/斜體會因為PhotoFont文字的錯誤而被拒絕。
* PhotoFont文字不支援垂直文字排列。
* photofont文字不支援16bpc PNG影像。
* 內嵌色彩設定檔的PNG影像色彩校正使用硬式編碼選項。 「演算色彩比對方式」為相對比色，且PhotoFont文字的「黑點」補償已開啟。
* 在公司[!DNL ini]檔案中啟用地區設定轉譯時，不支援檔案型查詢。
* 「影像伺服」無法正確寫入非封閉[!DNL Photoshop]路徑。
* 「影像伺服」目前不支援處理使用Adobe Media Encoder 4.0.1或更舊版本匯出的TIFF檔案。 Adobe Media Encoder包含在Premiere Pro CS4、After Effects CS4和Creative Suite 4 Production Premium。
* 搭配自動調整圖層使用`text=`不支援使用多個設定進行行對齊的RTF字串。

  *範例*

  RTF字串無法同時使用左右行對齊來調整文字圖層大小。

* 對於未內嵌在SVG檔案中的參照字型，SVG有其專屬的字型查閱路徑屬性。

  *症狀*

  包含字型定義的演算SVG影像使用的字型不正確。

  *因應措施*

  在`svgProvider.fontRoot=`中設定屬性[!DNL install_root/ImageServing/conf/PlatformServer.conf]。

* 裁切目前使用`bgColor=`而非`color=`來填滿任何新的延伸區域。

* 當`bgColor=`不符合涉及色彩設定檔的基本色域時，色彩轉換可能不正確。
* 如果圖層沒有遮色片或Alpha資料，則不會呈現外部圖層效果。

## 僅適用於影像演算的限制 {#section-4c6949e797174607a3d1ab4d3d4a725a}

* 貼花和牆面材料無法移除。
* 紋理大小會相對於暈映檢視的大小而受限。 在極少數情況下，預設的檢視大小425%限制可能會干擾使用非常大的不可重複紋理的應用程式。 如果無法將應用程式或內容變更為在預先定義的限制內運作，則百分比可以依照以下方式增加。 使用文字編輯器，開啟[!DNL install_root/ImageServing/conf/ImageServerRegistry.xml]，找到`IrMaxTextureSizeFactor`並輸入新的百分比值。 此變更會立即生效，無需重新啟動影像伺服器。

* Netscape和Opera快取回應資料中的JavaScript引擎，即使已設定nocache標頭亦然。 這會干擾有狀態要求的正常運作。

  *因應措施*

  將時間戳記或其他唯一識別碼附加至要求字串，例如`"&.ts=currentTime`。

## 僅適用於公用程式的限制 {#section-906a6b2378154b3da122b2332983f7a5}

透過`ImageConvert`停止時，`control-c`有時會因分段錯誤而當機。
