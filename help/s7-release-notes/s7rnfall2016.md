---
title: Scene72016年秋季發行
description: 「2016年Adobe Scene7秋季最新發佈說明，是Adobe Experience CloudAdobe Experience Manager解決方案的一部分。」
solution: Experience Manager
feature: Dynamic Media Classic
role: Developer,User
exl-id: 23091ef7-750a-4ec2-9d03-1d713f436991
source-git-commit: 11acb9151d3ea247eecde3cfbbd295a95c10829c
workflow-type: tm+mt
source-wordcount: '2209'
ht-degree: 0%

---

# Scene72016年秋季發行{#scene-fall-release}

2016年Adobe Scene7秋季最新發佈說明，是Adobe Experience CloudAdobe Experience Manager解決方案的一部分。

## Scene72016年秋季發行 {#topic-791cdf80f91e457fbb63bfedf79f5a94}

的最新發行說明 [!DNL Adobe Scene7] 2016年秋季發佈部分 [!DNL Adobe Experience Manager] 解決方案 [!DNL Adobe Experience Cloud]。

* [一般](s7rnfall2016.md#section-52afeb72ecb34c1585ea67a5051825a2)
* [場景 7](s7rnfall2016.md#section-24487cb493444d808fb7193f0a00cdd4)
* [查看器(影像服務5.5.3)](s7rnfall2016.md#section-1d59bcd5825d487b80b59a6d1a08ed30)
* [查看器(影像服務5.5.2)](s7rnfall2016.md#section-9932c988cfee45749594af481dfc6476)
* [查看器(影像服務5.5.1)](s7rnfall2016.md#section-833ab92c91c941d2bfdc27f233f582ad)
* [HTML5查看器SDK 3.0.1](s7rnfall2016.md#section-30e2392859c442d1aab2766d0f1d1580)
* [Dynamic Media Classic圖6.3.2服務與圖6.3.2](s7rnfall2016.md#section-19a3e96f52c74757bcdea0f8a11001f2)

## 一般 {#section-52afeb72ecb34c1585ea67a5051825a2}

Adobe很高興宣佈HTTP/2內容交付的可用性，並獲得效能改善的總體好處。

請參閱 [HTTP2內容傳送常見問題](https://experienceleague.adobe.com/docs/experience-manager-65/assets/dynamic/http2.html#dynamic)。

## Scene7出版系統 {#section-24487cb493444d808fb7193f0a00cdd4}

有關完整文檔，請參見 [https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html](https://experienceleague.adobe.com/docs/dynamic-media-classic/using/home.html)

**新功能、增強功能和錯誤修復**

* 已從中刪除視頻重播功能 [!DNL Adobe Scene7 Publishing System] 用戶介面。
* 在必要和可能時向所有Scene7Servlet添加身份驗證
* 涉及垃圾箱中「清單」視圖的Bug修復。
* 已刪除 **建立Dynamic Media Classic(Scene7)管理員** 出於安全考慮，從「用戶管理」獲得用戶功能。
* FTP WebAdmin現在支援OKTA身份驗證。
* 已刪除為新媒體門戶用戶建立的預設密碼的功能。
* 錯誤修復，涉及添加新用戶時生成的臨時密碼。 密碼未滿足必要的密碼要求。
* 已解決WebAdmin根磁碟已滿的問題。
* Bug修復涉及禁用用戶而不會立即反映在用戶介面中。
* Bug修復，涉及刪除不允許您稍後重新建立用戶的用戶。
* Bug修復，涉及發送到未包括身份驗證以控制某些設定的新Scene7用戶的歡迎電子郵件。
* 錯誤修復：如果FTP資料夾名稱中有特殊字元，則無法檢索該資料夾清單。
* 為Scene7環境配置OKTA服務提供商。
* 添加了對查看器分析的Experience Cloud組織ID的支援。
* 已實施Scene7SAML使用者。

## 查看器(影像服務5.5.3) {#section-1d59bcd5825d487b80b59a6d1a08ed30}

有關完整文檔，請參見 [查看器參考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en)。

**Image Service 5.5.3的錯誤修復**

* 與RequireJS和DOJO庫的相容性。

   在查看器部署期間整合的SDK JS快取。

## 查看器(影像服務5.5.2) {#section-9932c988cfee45749594af481dfc6476}

有關完整文檔，請參見 [查看器參考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en)。

**Image Service 5.5.2的錯誤修復**

* 在Windows 7上的Internet Explorer 11中播放視頻失敗。
* `initialframe` 未影響HTML5 eCatalog的移動設備上的縱向模式。

## 查看器(影像服務5.5.1) {#section-833ab92c91c941d2bfdc27f233f582ad}

有關完整文檔，請參見 [查看器參考指南](https://experienceleague.adobe.com/docs/dynamic-media-developer-resources/library/homeviewers.html?lang=en)。

**Image Service 5.5.1的新功能、增強功能和錯誤修復**

* HTML具有搜索功能的eCatalog查看器。
* 已添加HLS流視頻播放作為大多數案頭系統的預設視頻傳送方法。 基於Flash的HDS視頻流仍可作為替代播放選項。
* 添加了對運行Chrome瀏覽器的滑鼠和觸摸輸入設備的支援。
* 已將Experience Cloud組織ID支援添加到分析整合。
* 將AppMeasurement JavaScript庫更新為1.6.1版。
* 在eCatalog查看器中增加了對從右到左方向的支援。
* 已修復問題，其位置 `tip=0,-1,0` 導致超出範圍的錯誤。

**相容性說明**

* BlackBerry®

   * 與舊AVS集不相容。 客戶端必須重新上載AVS集以允許播放。

* 一般

   * 瀏覽器端縮放可能會導致用戶在縮放到頁面時UI和影像變得模糊。 UI格式也可能根據縮放顯示不正確。 此效果傳到全屏。
   * 由於移動設備的大小限制，混合媒體查看器使用幻燈片手勢來交換嵌入影像集中的幀，而不是點擊嵌入的色板元件。 該元件作為視覺指示器存在。
   * 在Internet Explorer瀏覽器和某些觸摸設備中，全屏模式不佔用整個設備螢幕。 相反，它會根據瀏覽器窗口的大小調整應用程式大小。
   * 「關閉」按鈕不能工作於iOS8.0和8.1，但不再出現於iOS8.2

* 銀河SII

   * Zoom和eCatalogHTML5查看器出現記憶體洩漏。 通過框架重複導航可能導致瀏覽器崩潰。
   * 按兩下查看器可能導致整個頁面縮放，而不是僅僅啟用瀏覽器側縮放的查看器。

* 銀河S4

   * 在瀏覽器設定中選中「Full Screen（全屏）」後，在縱向模式下檢測到設備為平板電腦。

* 銀河系

   * 按兩下查看器可能導致整個頁面縮放，而不是僅僅啟用瀏覽器側縮放的查看器。

* Galaxy Nexus 10和Galaxy平板電腦

   * 顯示具有縱向和橫向方向的不正確頁面跨頁的目錄。

* HTC移動設備

   * HTC移動設備Adobe的發現表明，無法禁用本機收縮縮放是HTC UI包裝(HTC Sense)的「特徵」。 在查看器上使用「收縮縮放」手勢時，此問題可能導致整個頁面縮放。 建議改用按兩下。
   * 如果影像映射小且靠近在一起，則影像映射表徵圖可以重疊。

* HTML5視頻

   * Internet Explorer 9:自定義海報影像不顯示。
   * `IntialBitRate` 只有軟體HLS和FlashHDS回放才支援修改量。 當播放使用本機播放器時，它不工作。
   * 當前不支援OGG和WebM漸進式回放。
   * 瀏覽器縮放可導致視頻播放器以不正確的大小顯示（包括Windows OS控制面板的「顯示」設定）。
   * 在Safari上使用HLS流視頻查找可能不一致。

* Internet Explorer

   * 當前不支援Quirks模式。
   * 當前不支援相容模式。
   * 當前不支援移動上的Internet Explorer。

* iOS

   * 大型eCatalogs可能導致iPad2上的瀏覽器崩潰。
   * iPhone6+手機被觀眾檢測為平板電腦。

* Safari

   * Safari 6.1或更高版本：Internet插件設定可能會阻止Flash視頻播放。
   * 使用Safari上的HLS流的視頻「查找」可能不一致。
   * 無法使用HLS流在Safari 6上查找視頻結束。

**已知問題和限制**

* 來自的Image Service修飾符 `iscommands` 未添加到 `req=set` 按設計要求。 僅影響影像顯示的修飾符工作正常。 影響大小的修改量必須用於複雜資產。 例如，

   `https://s7d9.scene7.com/s7viewers/html5/BasicZoomViewer.html?asset= {Scene7SharedAssets/Backpack_B?extendn=0.5%252C0.5%252C0.5%252C0.5}`

* [飛出] 滑鼠關閉後，IE9有時仍保持在螢幕上。
* 瀏覽器縮放會導致調整大小錯誤。
* iPad2:大型eCatalog資產在iOS的Safari崩潰。
* 所有檢視器

   * 不支援水印、混淆和鎖定。
   * 不支援影像預設。
   * 使用 `display:none` 當前不支援CSS或通過從父節點動態分離它。

* HTML5所有查看者

   * 將查看器嵌入表中可能導致在非本機全屏模式下調整查看器大小或放置查看器不正確。 建議改用DIV。
   * 代碼中具有顯式實例名稱的參數要求URL中的實例名稱也必須被覆蓋(例如， `zoomView.iconfeffect=0`)。
   * 當前不支援Image Serving命令裁剪。
   * 僅當查看器在子窗口中開啟時，「關閉」按鈕才起作用。
   * 的 `iscommands` 修飾符不支援影響影像大小的Image Serving修飾符。

* HTML5電子目錄

   * 導航到其他HTML頁並偶爾返回將導致查看器重置到第一頁。
   * 旋轉iOS設備後，頁面佈局偶爾顯示不正確。 縮放頁面可更正佈局。
   * 僅到多頁跨頁中最左側頁面的內部連結。 影響縱向模式下的移動設備。
   * InitalFrame僅連結到多頁跨頁中最左側的頁。 影響縱向模式下的移動設備。
   * 由於瀏覽器限制，IE9中不提供打印功能。

* HTML5混合媒體

   * 不支援配樂播放。

* HTML5

   * 要在傳出電子郵件中正確呈現縮略圖， `serverurl` 修飾符必須具有絕對URL。

* HTML5視頻

   * 海報影像可能遇到「最大大小」錯誤。 公司必須增加「影像服務發佈」的限制設定。
   * 如果從外部伺服器(而不是Scene7伺服器)提供托管HTML頁，則視頻標題需要公司規則集。 聯繫Adobe支援以獲得幫助。
   * 分析跟蹤可能報告由於緩衝而導致的播放百分比不正確
   * 黑框可能在iPad或Android™設備上顯示，而不是海報影像。
   * 在iPad或Android™設備上載入查看器時，黑幀可能會在螢幕上閃爍。
   * 當背景設定為iPad設備上的白色/透明時，VideoPlayer元件的側面顯示黑色邊框。
   * 在iPad使用iOS7時，最後一幀視頻可能會失真。
   * 在Chrome、Firefox和Internet Explorer瀏覽器的HLS流模式下，視頻查找期間可能偶爾出現宏阻塞。
      * 首次訪問者的海報影像可能不會在Microsoft®邊緣瀏覽器中顯示。
      * 使用漸進式回放時，Internet Explorer 9中的視頻載入後，海報影像可能會隱藏。

## Scene7HTML5查看器SDK 3.0.2 {#section-30e2392859c442d1aab2766d0f1d1580}

《使用手冊》位於客戶端安裝的AdobeHTML5 Viewer SDK資料夾中。 元件API文檔位於客戶端安裝的docs子資料夾中。

**3.0.2的錯誤修復**

* VideoPlayer — 在Windows 7上的Internet Explorer 11中播放視頻失敗。
* 目錄 —   `initialframe` 未影響HTML5 eCatalog查看器的移動設備上的縱向模式。

**3.0.1的新功能、增強功能和錯誤修復**

* 一般

   * 已添加HLS流視頻播放作為大多數案頭系統的預設視頻傳送方法。 基於Flash的HDS視頻流仍可作為替代播放選項。
   * 已添加SearchManager、SearchPanel、SearchEffect和SearchButton元件，以支援電子目錄查看器中的新搜索功能。
   * 增加了對在Chrome瀏覽器上同時運行滑鼠和觸摸輸入的設備的支援。
   * 重新構建Android™版本檢測，以支援未來版本的作業系統。
   * 添加對特定於eCatalog的SDK元件中從右到左方向的支援。

* 控制欄

   * 已為ControlBar內容添加可選滾動，以防其不適合可用寬度。

* 浮動縮放視圖

   * 固定案例 `tip=0,-1,0` 導致超出範圍的錯誤。

**相容性說明**

* Android™ 4.x

   * 要禁用預設值，必須為元件添加以下CSS規則：

      `-webkit-tap-highlight-color: rgba(0,0,0,0);`

* BlackBerry®

   * 當在AVS集中改變比特率流時，視頻播放可以停止。

* 鉻

   * 由於Chrome的內部快取，強制重建元件的任何API調用都可能被忽略。

* 銀河SII

   * 查看器有時無法載入到全屏。
   * Pageview當前在設備上出現記憶體洩漏。
   * 當瀏覽器側縮放處於活動狀態時，按兩下手勢會縮放查看器和頁面。

* 銀河系

   * 某些視圖元件上顯示的對象。
   * 當瀏覽器側縮放處於活動狀態時，按兩下手勢會縮放查看器和頁面。

* iPad3

   * iPad3的本地解析度為2048x1536。 如果公司的IS發佈、影像大小限制設定得較低，則此解析可能會導致顯示問題。

* iPhone4

   * 滾動頁面後，影像效果重播表徵圖被播放表徵圖替換。

* Internet Explorer

   * 在IE 10及更舊的全屏模式中，不會佔用整個螢幕，而只是根據瀏覽器窗口的大小調整應用程式大小。
   * 不支援Quirks呈現模式。
   * 當前不支援移動上的Internet Explorer。
   * 如果非同步包含，則Util.js可能無法載入。
   * IconEffect表徵圖阻止在SpinView和ZoomView元件上按一下事件。

* 本機設備視頻播放器

   * 當VideoPlayer用於調用設備的本機播放器時，不支援將UI元件分層到VideoPlayer上。
   * 在Safari 6上，以本機模式播放視頻不一致。
   * 滾動頁面後，本機播放將用播放表徵圖替換重放表徵圖。

* 觸摸設備

   * 全屏模式不會佔用整個設備螢幕，而只是根據瀏覽器窗口的大小調整應用程式大小。
   * 自定義游標在觸摸設備上不工作。
   * 當前不支援在觸摸設備上進行頁面縮放。 嵌入HTML5查看器需要具有適當設定的視區元標籤。

* 索姆

   * 當瀏覽器側縮放處於活動狀態時，按兩下手勢會縮放查看器和頁面。

**已知問題和限制**

* 所有元件

   * 在2.7.2版和更早版本中，某些元件已使用 `insertBefore()` API。 因此，無論何時建立元件實例相對於其它元件，這些元件都會將自身置於堆疊順序的底部。 在2.8.1版中，所有元件都使用 `appendChild()` API，這意味著元件堆疊順序將與實例建立順序匹配。

   * 使用 `iscommand` 不支援設定影像Alpha通道格式的修飾符。 使用元件 `FMT` 的形式。
   * 當前不支援CSS轉換屬性。

* 觸摸設備

   * 觸摸設備上的夾緊手勢不會生成縮放事件

* 容器

   * 不支援容器上的邊框、填充和邊距。 Adobe建議將樣式元素添加到父DIV。
   * 必須顯式設定容器大小，否則元件的大小可能正確。

* 打印元件

   * 由於瀏覽器限制，在Internet Explorer 9中，打印元件可能無法正確縮放紙張上的內容。

* IconEffect元件

   * IconEffect在Internet Explorer上生成指令碼錯誤(如果 `autohide` 已禁用(設定為 `0`)。

* ImageMapEffect元件

   * 在視圖元件上平移影像時延遲重定位表徵圖。

* MediaSet元件

   * 內聯資產請求與URL上的編碼相同。

* NavigationView元件

   * 當前元件不支援調整大小。

* PageScrubger元件

   * 在iPhone5上，當PageScrubber氣泡設定為文本時，它會在沿著軌道滑動按鈕時顯示偽像。 使用 `-webkit-background-clip: content;` 在風格上是圍繞問題展開的。

* SpinView元件

   * 在影像旋轉時，SpinView有時在刷動手勢並旋轉設備後似乎會凍結。

* 色板元件

   * 選取超出界限的色板時，將顯示兩個加亮。
   * 自動滾動 `selectSwatch()` 方法工作不正確。

* 視頻播放器

   * 如果查找設定為100%且回退設定為自動，則不更新視頻幀。
   * 在Chrome、Firefox和Internet Explorer瀏覽器的HLS流模式下，視頻查找期間可能偶爾出現宏阻塞。
   * 首次訪問者的海報影像可能不會在Microsoft®邊緣瀏覽器中顯示。
   * 使用漸進式回放時，Internet Explorer 9中的視頻載入後，海報影像可能會隱藏。

## Dynamic Media圖6.3.2服務與圖6.3.2 {#section-19a3e96f52c74757bcdea0f8a11001f2}

* IC實用程式 —  `downsample2x2` 不再支援標誌。 此標誌是IPS不再使用的質量較差的2x2下採樣器。
* CORS標頭 — 當前，CORS標頭已配置為 `/is/content/` 請求。
