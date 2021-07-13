---
description: 「Adobe Scene7 2016年秋季版的最新發行說明，是Adobe Marketing Cloud中Adobe Experience Manager解決方案的一部分。」
solution: Experience Manager
title: Scene7 2016年秋季版
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 206e4643e3926cb85b4be2189743578f88180be7
workflow-type: tm+mt
source-wordcount: '2235'
ht-degree: 0%

---

# Scene7 2016年秋季版{#scene-fall-release}

Adobe Scene7 2016年秋季的最新發行說明，是Adobe Marketing Cloud中Adobe Experience Manager解決方案的一部分。

## Scene7 2016年秋季版 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

[!DNL Adobe Scene7] 2016年秋季版的最新發行說明，此為[!DNL Adobe Marketing Cloud]中[!DNL Adobe Experience Manager]解決方案的一部分。

* [一般](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [場景 7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [檢視器（影像伺服5.5.3）](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [檢視器（影像伺服5.5.2）](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [檢視器（影像伺服5.5.1）](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5檢視器SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic影像提供6.3.2和影像轉譯6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## 一般 {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe很高興宣佈推出HTTP/2內容傳送，整體效能更佳。

請參閱[HTTP2內容傳送常見問題集](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic)。

## Scene7 Publishing System {#section-24487cb493444d808fb7193f0a00cdd4}

如需完整檔案，請參閱[https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**新功能、增強功能和錯誤修正**

* 從[!DNL Adobe Scene7 Publishing System]使用者介面移除視訊重新整理功能。
* 視需要並可能新增驗證至所有Scene7 servlet。
* 垃圾桶中清單檢視的錯誤修正。
* 基於安全考量，已從「使用者管理」中移除&#x200B;**建立Dynamic Media Classic(Scene7)Admin**&#x200B;使用者功能。
* FTP WebAdmin現在支援OKTA驗證。
* 移除為新Media Portal使用者建立的預設密碼功能。
* 新增使用者時產生的暫時密碼錯誤修正。 密碼未滿足必要的密碼要求。
* 已解決WebAdmin根磁碟已滿的問題。
* 有關停用使用者的錯誤修正不會立即反映在使用者介面中。
* 刪除使用者的錯誤修正，之後您無法重新建立該使用者。
* 傳送給新Scene7使用者的歡迎電子郵件（其中未包含用來控制特定設定的驗證）的錯誤修正。
* 若資料夾名稱中有特殊字元，則無法擷取FTP資料夾清單的錯誤修正。
* 為Scene7環境設定OKTA服務提供者。
* 新增對Viewer AnalyticsMarketing Cloud組織ID的支援。
* 實作Scene7 SAML消費者。

## 檢視器（影像伺服5.5.3） {#section-1d59bcd5825d487b80b59a6d1a08ed30}

如需完整檔案，請參閱[檢視器參考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html)。

**影像提供5.5.3的錯誤修正**

* 與RequireJS和DOJO程式庫相容。

   在檢視器部署期間整合SDK JS快取。

## 檢視器（影像伺服5.5.2） {#section-9932c988cfee45749594af481dfc6476}

如需完整檔案，請參閱[檢視器參考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html)。

**影像提供5.5.2的錯誤修正**

* 在Windows 7上的Internet Explorer 11中播放視頻失敗。
* `initialframe` 未影響HTML5 eCatalog的行動裝置上的縱向模式。

## 檢視器（影像伺服5.5.1） {#section-833ab92c91c941d2bfdc27f233f582ad}

如需完整檔案，請參閱[檢視器參考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/home.html)。

**影像伺服5.5.1的新功能、增強功能和錯誤修正**

* 具有搜尋功能的HTML5 eCatalog檢視器。
* 新增HLS串流視訊播放，作為大多數案頭系統的預設視訊傳送方法。 基於Flash的HDS視頻流仍作為替代播放選項提供。
* 新增對執行Chrome瀏覽器且具有滑鼠和觸控輸入的裝置支援。
* 新增Marketing Cloud組織ID支援至Analytics整合。
* 將AppMeasurement JavaScript程式庫更新至1.6.1版。
* 在eCatalog檢視器中新增對從右到左方向的支援。
* 修正`tip=0,-1,0`導致範圍外錯誤的問題。

**相容性說明**

* Blackberry

   * 與舊的AVS集不相容。 客戶端可能需要重新上傳AVS集以允許播放。

* 一般

   * 當使用者放大至頁面時，瀏覽器端縮放可能會導致UI和影像變得模糊。 根據縮放，UI格式也可能顯示不正確。 這將繼續全螢幕。
   * 由於行動裝置上的大小限制，混合媒體檢視器使用投影片手勢來交換內嵌影像集中的幀，而非點選內嵌色票元件。 元件作為視覺指標存在。
   * 在Internet Explorer瀏覽器和某些觸控式裝置中，全螢幕模式不會佔據整個裝置畫面。 而是會將應用程式調整為瀏覽器視窗的大小。
   * 「關閉」按鈕無法用於iOS 8.0和8.1，但iOS 8.2中已不再出現

* Galaxy SII

   * 使用縮放和eCatalog HTML5檢視器時出現記憶體洩漏。 透過框架重複導覽可能會導致瀏覽器當機。
   * 點選兩下檢視器可能會導致整個頁面縮放，而非只啟用瀏覽器端縮放的檢視器。

* Galaxy S4

   * 在瀏覽器設定中勾選全螢幕時，直向模式下的裝置偵測為平板電腦。

* Galaxy Nexus

   * 點選兩下檢視器可能會導致整個頁面縮放，而非只啟用瀏覽器端縮放的檢視器。

* Galaxy Nexus 10和Galaxy平板電腦

   * 以直向和橫向方向展開的eCatalog會顯示錯誤的頁面。

* HTC行動裝置

   * HTC行動裝置的調查結果顯示，無法停用原生縮放是HTC UI包裝函式(HTC Sense)的「功能」。 在檢視器上使用「夾捏以縮放」手勢時，這可能會導致整個頁面縮放。 建議您改用點選兩下。
   * 如果影像地圖小且靠近，則影像地圖表徵圖可以重疊。

* HTML5影片

   * Internet Explorer 9:自訂海報影像無法顯示。
   * `IntialBitRate` 修改器僅支援軟體HLS和FlashHDS播放。使用原生播放器時，無法運作。
   * 目前不支援OGG和WebM漸進式播放。
   * 瀏覽器縮放可能會導致視訊播放器以錯誤的大小顯示（包括Windows OS控制面板顯示設定）
   * 在Safari上使用HLS串流的視訊搜尋可能不一致。

* Internet Explorer

   * 目前不支援怪異模式。
   * 目前不支援相容模式。
   * 目前不支援行動裝置上的Internet Explorer。

* iOS

   * 大型eCatalog可能會在iPad 2上造成瀏覽器當機。
   * 檢視器會偵測到iPhone 6+手機為平板電腦。

* Safari

   * Safari 6.1或更新版本：網際網路外掛程式設定可能會阻止Flash視訊播放。
   * 在Safari上使用HLS串流的視訊「搜尋」可能不一致。
   * 無法在使用HLS串流的Safari 6上尋找視訊結尾。

**已知問題和限制**

* 來自`iscommands`的「影像伺服」修飾元未依設計新增至`req=set`請求。 只影響影像顯示的修飾符可正常工作。 影響大小的修飾元必須用於複雜資產。 例如，

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [] FlyoutIE9有時會在滑鼠關閉後仍停留在螢幕上。
* 瀏覽器縮放會導致重新調整大小錯誤。
* iPad 2:大型eCatalog資產會在iOS上導致Safari當機。
* 所有檢視器

   * 不支援水印、模糊化和鎖定。
   * 不支援影像預設集。
   * 目前不支援使用`display:none` CSS或從父節點動態分離檢視器，從DOM新增或移除檢視器。

* HTML5所有檢視器

   * 表格中的內嵌檢視器可能會導致非原生全螢幕模式中檢視器的大小或位置不正確。 建議改用DIV。
   * 程式碼中具有明確執行個體名稱的參數需要在URL中包含執行個體名稱且需加以覆寫（例如`zoomView.iconfeffect=0`）。
   * 目前不支援影像伺服命令裁切。
   * 「關閉」按鈕僅在查看器在子窗口中開啟時才有效。
   * `iscommands`修飾元不支援影響影像大小的影像伺服修飾元。

* HTML5 eCatalog

   * 導覽至其他HTML頁面並傳回時，偶爾會導致檢視器重設回第一個頁面。
   * 旋轉iOS裝置後，頁面配置偶爾會顯示不正確。 放大頁面可更正佈局。
   * 多頁跨頁中，內部連結只至最左側的頁面。 影響直向模式中的行動裝置。
   * InitalFrame連結僅至多頁跨頁中最左側的頁面。 影響直向模式中的行動裝置。
   * 由於瀏覽器限制，IE9中無法使用列印功能。

* HTML5 MixedMedia

   * 目前不支援音軌播放。

* HTML5社交

   * 若要在傳出的電子郵件中正確呈現縮圖，`serverurl`修飾元必須具有絕對URL。

* HTML5影片

   * 海報影像可能會遇到「大小上限」錯誤。 公司可能需要提高「影像伺服發佈」的限制設定。
   * 如果從外部伺服器(而非Scene7伺服器)提供托管HTML頁面，則視訊標題需要公司規則集。 請聯絡Adobe支援以取得協助。
   * Analytics追蹤可能會因為緩衝而回報不正確的播放百分比
   * iPad或Android裝置上可能會顯示黑色影格，而非海報影像。
   * 在iPad或Android裝置上載入檢視器期間，螢幕上可能會閃爍黑色影格。
   * 當iPad裝置上的背景設為白色/透明時，VideoPlayer元件的側面會顯示黑色邊框。
   * 使用iOS 7的iPad上，視訊的最後一個影格可能會扭曲。
   * 在Chrome、Firefox和Internet Explorer瀏覽器的HLS串流模式中，視訊搜尋期間可能會偶爾發生宏封鎖。
      * 海報影像可能不是第一次在Microsoft Edge瀏覽器中顯示。
      * 使用漸進式播放時，Internet Explorer 9中的視訊載入後，海報影像可能會隱藏。

## Scene7 HTML5檢視器SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

使用手冊位於用戶端安裝的AdobeHTML5檢視器SDK資料夾中。 若需元件API檔案，請參閱用戶端安裝的檔案子資料夾。

**3.0.2的錯誤修正**

* VideoPlayer — 在Windows 7的Internet Explorer 11中播放視訊失敗
* TableOfContents - `initialframe`不影響HTML5 eCatalog檢視器的行動裝置上的縱向模式。

**3.0.1的新功能、增強功能和錯誤修正**

* 一般

   * 新增HLS串流視訊播放，作為大多數案頭系統的預設視訊傳送方法。 基於Flash的HDS視頻流仍作為替代播放選項提供。
   * 新增SearchManager、SearchPanel、SearchEffect和SearchButton元件，以支援eCatalog檢視器中的新搜尋功能。
   * 新增在Chrome瀏覽器上執行滑鼠和觸控輸入的裝置支援。
   * 重構Android版本偵測以支援未來版本的作業系統
   * 在eCatalog專用的SDK元件中新增對從右到左方向的支援。

* 控制欄

   * 新增ControlBar內容的選用捲動功能，以防其不符合可用寬度。

* FlyoutzoomView

   * 修正`tip=0,-1,0`導致範圍外錯誤的案例。

**相容性說明**

* Android 4.x

   * 若要停用預設值，需要為元件新增下列CSS規則的藍色醒目提示：

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* Blackberry

   * 當在AVS集中更改比特率流時，視頻播放可能停止。

* 鉻黃

   * 由於Chrome的內部快取，任何強制重建元件的API呼叫都可能會遭到忽略。

* Galaxy SII

   * 檢視器有時無法載入全螢幕。
   * Pageview目前在裝置上發生記憶體洩漏。
   * 當瀏覽器端縮放處於作用中狀態時，雙點手勢會縮放檢視器和頁面。

* Galaxy Nexus

   * 某些檢視元件上顯示的成品。
   * 當瀏覽器端縮放處於作用中狀態時，雙點手勢會縮放檢視器和頁面。

* iPad 3

   * iPad 3的原生解析度為2048x1536。 如果公司的IS發佈、影像大小限制設定低於，這可能會造成顯示問題。

* iPhone4

   * 捲動頁面後，「影像」重播圖示取代為「播放」圖示。

* Internet Explorer

   * 在IE 10及舊版全螢幕模式中，不會佔用整個螢幕，而只是將應用程式調整為瀏覽器視窗的大小。
   * 不支援怪異渲染模式。
   * 目前不支援行動裝置上的Internet Explorer。
   * 如果以非同步方式包含，Util.js可能會無法載入。
   * IconEffect表徵圖阻止在回轉視圖和縮放視圖元件上按一下事件。

* 原生裝置視訊播放器

   * 使用VideoPlayer呼叫裝置的原生播放器時，不支援將UI元件分層到VideoPlayer上。
   * Safari 6上原生模式的視訊播放不一致。
   * 捲動頁面後，原生播放會以播放圖示取代重播圖示。

* 觸控裝置

   * 全螢幕模式不會佔用整個裝置螢幕，而只是將應用程式調整為瀏覽器視窗的大小。
   * 自定義游標在觸摸設備上無法工作。
   * 目前不支援觸控裝置上的頁面縮放。 內嵌HTML5檢視器需要具備適當設定的檢視區中繼標籤。

* Xoom

   * 當瀏覽器端縮放處於作用中狀態時，雙點手勢會縮放檢視器和頁面。

**已知問題和限制**

* 所有元件

   * 在2.7.2版及舊版中，使用`insertBefore()` API將某些元件新增至DOM。 因此，無論何時建立元件實例是相對於其他元件，這些元件都會將自身置於堆疊順序的底部。 在2.8.1版中，所有元件現在都使用`appendChild()` API，這表示元件堆疊順序會符合執行個體建立的順序。

   * 不支援使用`iscommand`修飾詞來設定影像Alpha通道格式。 請改用元件`FMT`參數。
   * 目前不支援CSS轉換屬性。

* 觸控裝置

   * 觸控裝置上的夾捏手勢不會產生縮放事件

* 容器

   * 不支援容器上的邊框、邊框間距和邊距。 Adobe建議將樣式元素新增至父DIV。
   * 需要明確設定容器大小，否則元件的大小可能會正確。

* 打印元件

   * 由於瀏覽器限制，在Internet Explorer 9中，打印元件可能無法正確縮放紙張上的內容。

* IconEffect元件

   * 如果`autohide`被禁用（設定為`0`）,IconEffect會在Internet Explorer上生成指令碼錯誤。

* ImageMapEffect元件

   * 在檢視元件上平移影像時，重新定點陣圖示會延遲。

* MediaSet元件

   * 內嵌資產要求與URL上的編碼相同。

* NavigationView元件

   * 目前元件不支援調整大小。

* PageScrubber元件

   * 在iPhone 5中，當PageScrubber泡泡設為text時，會在沿著軌道滑動按鈕時顯示偽影。 在樣式中使用`-webkit-background-clip: content;`可解決問題。

* 回轉視圖元件

   * 在影像旋轉時，SpinView有時會在滑動手勢和旋轉裝置後凍結。

* 色票元件

   * 選取超出界限的色票時，會顯示2個反白顯示。
   * 使用`selectSwatch()`方法自動捲動的操作不正確。

* VideoPlayer

   * 如果搜尋設為100%且後援設定為自動，視訊影格不會更新。
   * 在Chrome、Firefox和Internet Explorer瀏覽器的HLS串流模式中，視訊搜尋期間可能會發生偶爾的巨集封鎖。
   * 海報影像可能不是第一次在Microsoft Edge瀏覽器中顯示。
   * 使用漸進式播放時，Internet Explorer 9中的視訊載入後，海報影像可能會隱藏。

## Dynamic Media影像提供6.3.2和影像轉譯6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* IC實用程式 — 不再支援`downsample2x2`標誌。 此標幟是品質不佳的2x2下拉取樣器，IPS不再使用。
* CORS標題 — 目前，CORS標題是針對`/is/content/`請求而設定。
