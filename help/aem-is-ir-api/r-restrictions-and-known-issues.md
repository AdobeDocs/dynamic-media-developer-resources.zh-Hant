---
description: 使用Dynamic Media影像服務時，應考慮一些限制和已知問題。
solution: Experience Manager
title: 限制和已知問題
feature: Dynamic Media Classic,SDK/API
role: Developer,User
exl-id: fd32456b-9d99-4e82-a61c-2fc4d7030630
source-git-commit: bf31e5226cbb763e2fb82391772b64e5d5c89fae
workflow-type: tm+mt
source-wordcount: '1222'
ht-degree: 0%

---

# 限制和已知問題{#restrictions-and-known-issues}

使用Dynamic Media影像服務時，應考慮一些限制和已知問題。

## 文檔勘誤表 {#section-b1579410b11e41e488c7de9ecc7e8d5c}

* 行數不會超過 `\copyfitmaxlines` 設定和文本輸入中的顯式行數。
* 影像集中需要匹配大括弧和圓括弧。 如果大括弧和括弧不匹配，則它們需要URL編碼。
* 伺服器端全局響應時間警報包括錯誤響應。
* 的 `id=` 當使用 `rect=` 命令。

## 已知差異textPs=與text= {#section-16ede4c13a7648feb0d2fc93341fd4aa}

* 與使用 `text=`。
* 與使用 `text=`。
* `\expnd` 和 `\expndtw` 與高負值一起使用時，會導致字元在使用時相互放在前面 `text=`。

* `\charscaley` 比使用 `text=` 但不影響線高。

* 如果最後一行文本不適合，則刪除整行，而不顯示為截止。
* `\slmult` 和 `\sl` 與MS Word的行為方式不同， `text=`，它們只對當前段和後續段落生效。

* `\sb` 適用於MS Word和 `text=`、Adobe InDesign [!DNL Photoshop] 別這樣。

* `\sa` 適用於MS Word和 `text=`、Adobe InDesign [!DNL Photoshop] 別這樣。

## 向後相容性 {#section-a76842f751944f4fb664af296d064122}

* 轉義下划線字元( `\_`)中的RTF字串不能使用 `textPs=`

* 支援不區分大小寫的宏處理。
* 目錄快取已從60秒減少到10秒。
* 錯誤重定向功能現在僅重定向引用目錄中發佈但在磁碟上找不到的損壞影像、字型、顏色配置檔案和影像的請求。
* `posN=`。 `anchor=`。 `anchorN=`。 `origin=`, `originN=` 現在，如果任何修飾符值大於2147483648，則返回分析錯誤。

* 不支援嵌套請求的編碼。 轉換為新行為，並解除對站點和公司目錄中URL請求中找到的任何嵌套請求值的編碼。
* DefaultImage現在在使用 `req=tmb`。
* 在以前版本中使用 `flip=`，無論錨點是什麼，都不會重新定位影像。

## 適用於第三方庫的限制 {#section-79768b96bf634e44ab672c5b893f343d}

如果已檢測到Digimarc水印，則Digimarc庫拒絕將Digimarc水印應用於影像。 如果對主影像進行了足夠的編輯，Digimarc庫可能仍然能夠識別是否應用了水印。 但是，它可能無法讀取這些資訊。 這會產生一個新影像，在該新影像中無法獲得應用於原始影像的原始Digimarc資訊。 影像服務現在可以應用公司目錄中定義的Digimarc水印。

## 適用於影像服務和影像渲染的限制 {#section-f836cb40ae2d4f32a9cf7ebda4d91bae}

* 當可用的CPU超過4個時，影像服務和影像呈現可能無法充分利用所有CPU。 模擬這些電腦上的流量，瞭解4個以上CPU的優勢。
* 返回重定向（HTTP狀態301、302或303）的遠程URL被拒絕。
* 配置時 `errorRedirect.rootUrl` 此屬性中定義的IP地址需要包含在規則集中 `<addressfilter>` 該伺服器上的標籤值。

   *範例*:

   伺服器A已定義 `errorRedirect.rootUrl=10.10.10.10` 。

   IP地址為10.10.10.10的伺服器B將 `<addressfilter>` 規則集檔案中的標籤值，以包括其IP地址(10.10.10.10)。

* 具有定位的點文本和文本路徑可能顯示剪貼。
* `text=` 僅適用 `\sa` 和 `\sb` 全文塊，而不是按段落。

* 使用在URL中定義的一家公司和為 `src=` 或 `mask=` 修改量，您必須為為 `src=` 或 `mask=` 這種形式的請求。

   *範例*:

   `/is/image/MyCompany?src=/YourCompany/MyImage` .

   而不是： `/is/image/MyCompany?src=YourCompany/MyImage` 。

* 非Pyramided Tiff或Vignette請求會生成類似的錯誤消息，

   *&quot;影像 `C:\Program Files\Scene7\ImageRendering\resources\MyVignette.vnt` 沒有有效的DSF,2.25MPixel的面積超過2MPixel的最大值」* 。

   最佳做法是使用Pyramided Tavis和Vignettes。 如果您需要使用非吡唑並獒或小品，請按照以下說明增加尺寸限制。

   *周圍工作*:

   對於影像渲染非吡唑並字，請在 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 配置檔案。

   對於影像服務非吡唑TIFF，請增加 `MaxNonDsfSize` 的 [!DNL install_root/ImageServing/bin/ImageServerRegistry.xml] 配置檔案。

* Adobe [!DNL Photoshop] 預設情況下，CS3不會將分層PSD檔案保存為複合映像。

   *症狀*:

   Adobe [!DNL Photoshop] CS3分層PSD檔案顯示為黑色，文本上寫著： [!DNL Photoshop] 檔案未用複合影像保存。」 在IPS中。

   *解決辦法*︰

   保存Adobe [!DNL Photoshop] 已開啟具有最大相容性的CS3檔案。

* 將ICC配置檔案分配給CMYK/JPEG回復影像會導致某些瀏覽器中的顏色反轉。*周圍工作*:

   使用 `fmt=`

* 壓縮後HTTP響應影像資料（包括檔案頭）的大小限制為16 MB。
* &quot;。&quot; 不允許在HTTP請求中的任何路徑元素中。
* 卸載可從中刪除用戶建立或修改的檔案 *[!DNL install_root]* 或任何子資料夾。 卸載前，將這些檔案複製到其他位置。

## 僅適用於影像服務的限制 {#section-b08ad535e4454265b8157dec244c4faf}

* RTF中的前景色( `\cf`)命令不支援PhotoFont文本。
* 合成粗體、斜體和粗體/斜體會作為PhotoFont文本的錯誤被拒絕。
* PhotoFont文本不支援垂直文本流。
* PhotoFont文本不支援16bpc PNG影像。
* 使用硬編碼選項對具有嵌入顏色配置檔案的PNG影像進行顏色校正。 呈現意圖是相對比色，並且PhotoFont文本的黑點補償已開啟。
* 在公司中啟用區域設定轉換時不支援基於檔案的查找 [!DNL ini] 的子菜單。
* 映像服務不寫入非關閉 [!DNL Photoshop] 路徑正確。
* 映像服務當前不支援處理使用Adobe Media Encoder4.0.1或更早版本導出的TIFF檔案。 Adobe Media Encoder與Premiere ProCS4、After EffectsCS4和Creative Suite4 Production Premium一起提供。
* 使用 `text=` 自調整圖層不支援使用多個設定進行行對齊的RTF字串。

   *範例*

   RTF字串不能同時使用左行和右行對齊來調整文本層的大小。

* SVG對未嵌入到SVG檔案中的引用字型的字型查找路徑有其自己的屬性。

   *症狀*

   包含字型定義的已呈現SVG影像使用的字型不正確。

   *解決方法*

   設定屬性 `svgProvider.fontRoot=` 在 [!DNL install_root/ImageServing/conf/PlatformServer.conf] 。

* 裁剪當前正在使用 `bgColor=` 而不是 `color=` 填充任何新擴展區域。

* 當 `bgColor=` 與涉及顏色配置檔案的基本顏色空間不匹配。
* 如果圖層沒有蒙版或Alpha資料，則不呈現外層效果。

## 僅適用於影像渲染的限制 {#section-4c6949e797174607a3d1ab4d3d4a725a}

* 牆面和牆面材料無法移除。
* 紋理的大小相對於視頻視圖的大小是有限的。 在極少數情況下，視圖大小的425%的預設限制可能會干擾使用非常大的非可重複紋理的應用程式。 如果無法將應用程式或內容更改為在預定義的限制內工作，則百分比可以增加如下。 使用文本編輯器，開啟 [!DNL install_root/ImageServing/conf/ImageServerRegistry.xml]查找 `IrMaxTextureSizeFactor` 並輸入新的百分比值。 更改將立即生效，而不重新啟動映像伺服器。

* 即使設定了nocache標頭，Netscape和Opera中的JavaScript引擎也會快取響應資料。 這妨礙了有狀態請求的正常運作。

   *解決方法*

   將時間戳或其他唯一標識符附加到請求字串，如 `"&.ts=currentTime`。

## 僅適用於實用程式的限制 {#section-906a6b2378154b3da122b2332983f7a5}

`ImageConvert`有時在與 `control-c`。
