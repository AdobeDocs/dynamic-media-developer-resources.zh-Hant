---
description: Adobe Scene7 2016年秋季版本的最新發行說明，是Adobe Marketing Cloud中Adobe Experience Manager解決方案的一部分。
seo-description: Adobe Scene7 2016年秋季版本的最新發行說明，是Adobe Marketing Cloud中Adobe Experience Manager解決方案的一部分。
seo-title: Scene7 2016年秋季發行
solution: Experience Manager
title: Scene7 2016年秋季發行
topic: Dynamic media
uuid: 3fddda65-0c6e-48ec-bd60-7e0ca59421a8
translation-type: tm+mt
source-git-commit: 6380d839a794cbf82854a2ecd28c18f16f06d4c7
workflow-type: tm+mt
source-wordcount: '2263'
ht-degree: 0%

---


# Scene7 2016年秋季發行{#scene-fall-release}

Adobe Scene7 2016年秋季版本的最新發行說明，是Adobe Marketing Cloud中Adobe Experience Manager解決方案的一部分。

## Scene7 2016年秋季發行 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

2016年秋季版本的最 [!DNL Adobe Scene7] 新發行說明，是解決方 [!DNL Adobe Experience Manager] 案的一部分 [!DNL Adobe Marketing Cloud]。

* [一般](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [Scene7 Publishing System](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [檢視器(Image Serving 5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [檢視器(Image Serving 5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [檢視器(Image Serving 5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [Scene7 HTML5 Viewer SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Scene7 Image Serving 6.3.2和Image Rendering 6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## 一般 {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe很榮幸宣佈推出HTTP/2內容傳送，並提升效能。

請參 [閱HTTP2內容傳送常見問答](https://docs.adobe.com/content/docs/en/aem/6-2/administer/integration/marketing-cloud/scene7/http2faq.html)。

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

如需完整檔案，請參閱 [https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html](https://docs.adobe.com/content/help/en/dynamic-media-classic/using/home.html)

**新功能、增強功能和錯誤修正**

* 已從使用者介面移除視訊 [!DNL Adobe Scene7 Publishing System] 重新剪輯功能。
* 已視需要和可能新增所有Scene7 Servlet的驗證。
* 關於垃圾桶中清單檢視的錯誤修正。
* 由於安 **全考慮，已從「用戶管理** 」中移除「建立SPSAdmin用戶」功能。
* FTP WebAdmin現在支援OKTA驗證。
* 已移除為新Media Portal使用者建立的預設密碼功能。
* 新增使用者時產生的暫時密碼相關的錯誤修正。 密碼不符合必要的密碼要求。
* 已解決WebAdmin根磁碟已滿的問題。
* 錯誤修正：使用者停用時，不會立即反映在使用者介面中。
* 錯誤修正：刪除未讓您稍後重新建立使用者的使用者。
* 傳送給未包含驗證以控制特定設定的新Scene7使用者的歡迎電子郵件錯誤修正。
* 錯誤修正：如果FTP檔案夾名稱中有特殊字元，則無法擷取FTP檔案夾清單。
* 為Scene7環境設定OKTA服務供應商。
* 新增對檢視器分析的Marketing Cloud組織ID支援。
* 實作Scene7 SAML使用者。

## 檢視器(Image Serving 5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

如需完整檔案，請參 [閱檢視器參考指南](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html)。

**Image Serving 5.5.3的錯誤修正**

* 與RequireJS和DOJO程式庫相容。

   在檢視器部署期間，整合的SDK JS快取。

## 檢視器(Image Serving 5.5.2) {#section-9932c988cfee45749594af481dfc6476}

如需完整檔案，請參 [閱檢視器參考指南](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html)。

**Image Serving 5.5.2的錯誤修正**

* 在Windows 7的Internet Explorer 11中播放視訊失敗。
* `initialframe` 未影響HTML5 eCatalog行動裝置上的縱向模式。

## 檢視器(Image Serving 5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

如需完整檔案，請參 [閱檢視器參考指南](https://docs.adobe.com/content/help/en/dynamic-media-developer-resources/library/home.html)。

**Image Serving 5.5.1的新功能、增強功能和錯誤修正**

* 具有搜尋功能的HTML5 eCatalog檢視器。
* 已新增HLS串流視訊播放，做為大多數案頭系統的預設視訊傳送方法。 以Flash為基礎的HDS視訊串流仍可做為另一種播放選項。
* 新增支援執行Chrome瀏覽器的滑鼠和觸控輸入裝置。
* 新增Marketing Cloud組織ID支援至Analytics整合。
* 將AppMeasurement JavaScript程式庫更新至1.6.1版。
* 新增在eCatalog檢視器中支援從右至左方向。
* 修正造 `tip=0,-1,0` 成範圍外錯誤的問題。

**相容性說明**

* Blackberry

   * 與舊版AVS集不相容。 客戶端可能需要重新上載AVS集以允許播放。

* 一般

   * 當使用者放大至頁面時，瀏覽器端縮放可能會導致UI和影像變得模糊。 UI格式也可能會因縮放而顯示錯誤。 這個將傳至全螢幕。
   * 由於行動裝置的大小限制，Mixed Media Viewer使用投影片手勢來交換內嵌影像集中的影格，而非點選內嵌色票元件。 該元件作為可視指示器存在。
   * 在Internet Explorer瀏覽器和某些觸控裝置中，全螢幕模式不會佔據整個裝置螢幕。 它會根據瀏覽器視窗的大小調整應用程式的大小。
   * 「關閉」按鈕無法運作iOS 8.0和8.1，但iOS 8.2中不再出現

* Galaxy SII

   * 使用縮放和eCatalog HTML5檢視器時會發現記憶體洩漏。 在影格中重複導覽可能會導致瀏覽器當機。
   * 點選兩下檢視器可能會使整個頁面縮放，而不只是啟用瀏覽器端縮放的檢視器。

* Galaxy S4

   * 在縱向模式中偵測為平板電腦的裝置，並在瀏覽器設定中勾選「全螢幕」。

* Galaxy Nexus

   * 點選兩下檢視器可能會使整個頁面縮放，而不只是啟用瀏覽器端縮放的檢視器。

* Galaxy Nexus 10與Galaxy Tablet

   * eCatalog會以縱向和橫向方向顯示不正確的頁面跨頁。

* HTC行動裝置

   * HTC行動裝置的發現顯示，無法停用原生夾捏縮放是HTC UI包裝函式(HTC Sense)的「功能」。 在檢視器上使用「夾捏以縮放」手勢時，這可能會導致整個頁面縮放。 建議改用點選兩下。
   * 如果影像映射小且靠近，則影像映射表徵圖可能重疊。

* HTML5視訊

   * Internet Explorer 9: 自訂海報影像不會顯示。
   * `IntialBitRate` 只有軟體HLS和Flash HDS播放才支援修飾元。 當播放使用原生播放器時，它無法運作。
   * 目前不支援OGG和WebM漸進式播放。
   * 瀏覽器縮放可導致視訊播放器以不正確的大小顯示（包括Windows OS控制面板顯示設定）
   * 在Safari上使用HLS串流的視訊搜尋可能不一致。

* Internet Explorer

   * 目前不支援Quirks模式。
   * 目前不支援相容模式。
   * 目前不支援行動裝置上的Internet Explorer。

* iOS

   * 大型eCatalog可能會導致iPad 2的瀏覽器當機。
   * 檢視器會偵測到iPhone 6+手機為平板電腦。

* Safari

   * Safari 6.1或更新版本： 網際網路外掛程式設定可能會阻止Flash視訊播放。
   * 在Safari上使用HLS串流的視訊「搜尋」可能不一致。
   * 無法在使用HLS串流的Safari 6上尋找視訊結束。

**已知問題與限制**

* 「影像伺服」修飾 `iscommands` 元不會依設計新 `req=set` 增至請求。 僅影響影像顯示的修飾元可正常運作。 影響大小的修飾元必須用於複雜資產。 例如，

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [彈出式] IE9有時會在滑鼠關閉後仍保留在螢幕上。
* 瀏覽器縮放會導致調整大小錯誤。
* iPad 2: 大型eCatalog資產會在iOS上造成Safari當機。
* 所有檢視器

   * 不支援浮水印、模糊化和鎖定。
   * 不支援影像預設集。
   * 目前不支援使用 `display:none` CSS或從父節點動態分離檢視器，從DOM新增或移除檢視器。

* HTML5所有檢視器

   * 表格中的內嵌檢視器可能會導致檢視器在非原生全螢幕模式中的大小或位置不正確。 建議改用DIV。
   * 在程式碼中具有明確例項名稱的參數，需要在URL中覆寫例項名稱(例如 `zoomView.iconfeffect=0`)。
   * 目前不支援影像伺服指令裁切。
   * 「關閉」按鈕只有在檢視器在子視窗中開啟時才會運作。
   * 該修 `iscommands` 飾詞不支援影響影像大小的影像伺服修飾詞。

* HTML5 eCatalog

   * 導覽至其他HTML頁面並返回時，偶爾會導致檢視器重設回第一頁。
   * 旋轉iOS裝置後，頁面配置偶爾會顯示錯誤。 放大頁面可修正版面。
   * 多頁跨頁中最左側頁面的內部連結。 影響縱向模式中的行動裝置。
   * InitalFrame連結僅會連結至多頁跨頁中最左側的頁面。 影響縱向模式中的行動裝置。
   * 由於瀏覽器限制，IE9中無法使用列印功能。

* HTML5 MixedMedia

   * 目前不支援配樂播放。

* HTML5 Social

   * 若要在傳出的電子郵件中正確呈現縮圖， `serverurl` 修飾元必須有絕對的URL。

* HTML5視訊

   * 海報影像可能會遇到「最大大小」錯誤。 公司可能需要提高影像伺服發佈的限制設定。
   * 如果代管HTML頁面是從外部伺服器（而非Scene7伺服器）提供，則視訊標題需要公司規則集。 請聯絡Adobe支援以取得協助。
   * Analytics追蹤可能會因為緩衝而報告不正確的播放百分比
   * iPad或Android裝置上可能會顯示黑色影格，而非海報影像。
   * 在iPad或Android裝置上載入檢視器期間，螢幕上可能會出現黑色影格。
   * 當iPad裝置上的背景設為白色／透明時，VideoPlayer元件側會顯示黑色邊框。
   * 使用iOS 7的iPad上，視訊的最後一個影格可能會扭曲。
   * 在Chrome、Firefox和Internet Explorer瀏覽器的HLS串流模式中，視訊搜尋期間可能會偶爾發生Macrobocking。
   * 海報影像可能無法在首次訪客的Microsoft Edge瀏覽器中顯示。
   * 當使用漸進式播放時，海報影像可能會在Internet Explorer 9中載入視訊後隱藏。

## Scene7 HTML5 Viewer SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

使用指南位於用戶端安裝的Adobe HTML5 Viewer SDK檔案夾中。 元件API檔案位於用戶端安裝的docs子資料夾中。

**3.0.2的錯誤修正**

* VideoPlayer —— 在Windows 7的Internet Explorer 11中播放視訊失敗
* TableOfContents —— 不 `initialframe` 會影響HTML5 eCatalog檢視器行動裝置的縱向模式。

**3.0.1的新功能、增強功能和錯誤修正**

* 一般

   * 已新增HLS串流視訊播放，做為大多數案頭系統的預設視訊傳送方法。 以Flash為基礎的HDS視訊串流仍可做為另一種播放選項。
   * 新增SearchManager、SearchPanel、SearchEffect和SearchButton元件，以支援eCatalog檢視器中的新搜尋功能。
   * 新增支援在Chrome瀏覽器上同時執行滑鼠和觸控輸入的裝置。
   * 重構Android版本偵測以支援未來版本的作業系統
   * 在eCatalog專用的SDK元件中新增對由右至左方向的支援。

* ControlBar

   * 新增ControlBar內容的選用捲動功能，以防其不符合可用寬度。

* FlyoutzoomView

   * 已修正 `tip=0,-1,0` 導致範圍外錯誤的案例。

**相容性說明**

* Android 4.x

   * 若要停用預設值，請以藍色反白標示下列CSS規則，以便為元件新增：

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry

   * 當在AVS集中更改比特率流時，視頻播放可能停止。

* Chrome

   * 由於Chrome的內部快取，任何強制重建元件的API呼叫都可能會被忽略。

* Galaxy SII

   * 檢視器有時無法載入全螢幕。
   * Pageview目前在裝置上發生記憶體洩漏。
   * 當瀏覽器端縮放處於作用中時，點選兩下手勢會縮放檢視器和頁面。

* Galaxy Nexus

   * 某些視圖元件上顯示的對象。
   * 當瀏覽器端縮放處於作用中時，點選兩下手勢會縮放檢視器和頁面。

* iPad 3

   * iPad 3的原生解析度為2048x1536。 如果公司的IS發佈、影像大小限制設定為低於此值，這可能會造成顯示問題。

* iPhone4

   * 在捲動頁面後，圖示效果重播圖示已取代為播放圖示。

* Internet Explorer

   * 在IE 10及舊版全螢幕模式中，並不佔用整個螢幕，而是只將應用程式調整為瀏覽器視窗的大小。
   * 不支援Quirks演算模式。
   * 目前不支援行動裝置上的Internet Explorer。
   * 如果非同步包含，Util.js可能無法載入。
   * IconEffect圖示會封鎖回轉檢視和縮放檢視元件上的點按事件。

* 原生裝置視訊播放器

   * 當使用VideoPlayer呼叫裝置的原生播放器時，不支援將UI元件分層至VideoPlayer。
   * 在Safari 6上，原生模式的視訊播放不一致。
   * 在捲動頁面後，原生播放會以播放圖示取代重播圖示。

* 觸控裝置

   * 全螢幕模式不會佔用整個裝置螢幕，而只會將應用程式調整為瀏覽器視窗的大小。
   * 自訂游標無法在觸控裝置上運作。
   * 目前不支援在觸控裝置上縮放頁面。 內嵌HTML5檢視器需要具備適當設定的檢視埠中繼標籤。

* Xoom

   * 當瀏覽器端縮放處於作用中時，點選兩下手勢會縮放檢視器和頁面。

**已知問題與限制**

* 所有元件

   * 在2.7.2版及舊版中，有些元件是使用 `insertBefore()` API新增至DOM。 因此，無論何時建立元件實例相對於其他元件，這些元件都會將自身置於堆疊順序的底部。 在2.8.1版中，所有元件現在都使用 `appendChild()` API，這表示元件堆疊順序會符合執行個體建立順序。

   * 不支 `iscommand` 援使用修飾元來設定影像alpha色版格式。 請改用 `FMT` 元件參數。
   * 目前不支援CSS轉換屬性。

* 觸控裝置

   * 在觸控裝置上夾捏手勢不會產生縮放事件

* 容器

   * 不支援容器上的邊框、間距和邊界。 Adobe建議將樣式元素新增至父DIV。
   * 需要明確設定容器大小，否則元件的大小可能會正確。

* 列印元件

   * 由於瀏覽器的限制，在Internet Explorer 9中，列印元件可能無法正確縮放紙本內容。

* IconEffect元件

   * IconEffect會在Internet Explorer上產生指令碼錯誤( `autohide` 若停用(設為 `0`)。

* ImageMapEffect元件

   * 在檢視元件上平移影像時，會延遲重新定點陣圖示。

* MediaSet元件

   * 內嵌資產要求與URL上的編碼相同。

* NavigationView元件

   * 目前元件不支援調整大小。

* PageScrubber元件

   * 在iPhone 5中，當PageScrubber泡泡設定為文字時，它會在沿著磁軌滑動按鈕時顯示不自然狀態。 在樣 `-webkit-background-clip: content;` 式中使用可解決問題。

* 回轉視圖元件

   * 在影像旋轉時，回轉檢視有時會在滑動手勢和旋轉裝置後出現凍結狀態。

* 色票元件

   * 選取超出範圍的色票時，會顯示2個反白顯示。
   * 使用方法自動 `selectSwatch()` 捲動的運作不正確。

* VideoPlayer

   * 如果搜尋設為100%且備援設為自動，則視訊影格不會更新。
   * 在Chrome、Firefox和Internet Explorer瀏覽器的HLS串流模式中，視訊搜尋期間可能會偶爾發生巨集封鎖。
   * 海報影像可能無法在首次訪客的Microsoft Edge瀏覽器中顯示。
   * 當使用漸進式播放時，海報影像可能會在Internet Explorer 9中載入視訊後隱藏。

## Scene7 Image Serving 6.3.2 and Image Rendering 6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* IC實用程式- `downsample2x2` 不再支援標籤。 此標幟是品質不佳的2x2下採樣器，IPS不再使用。
* CORS標題——目前，CORS標題已針對請求設 `/is/content/` 定。

