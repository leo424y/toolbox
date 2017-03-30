Chrome外掛篇
===

Chrome DevTools
---

在我所用過的這些前端工具裡，最常用、實用的就屬Chrome自帶的DevTools。通常情況下，我們只需要使用這個工具就可以完成大部分的工作了。

![Chrome DevTools](http://toolbox.phodal.com/images/fe-plugins/dev-tool.jpg)

每個前端工程師，都應該好好學習如何去使用Chrome DevTools。當然，這並不是一篇詳細的關於Chrome DevTools的介紹——相關的內容足夠寫一本書了。除了正常的Debug功能，它可以模擬移動裝置，模擬網路、模板解析度、模擬，並在HTTP請求中帶上相應的User Agent方便我們偵錯。

Open SEO Stats
---

顧名思義這是一個SEO狀態查詢工具，它可以讓我們檢視網站的SEO相關資訊。也是一個非常棒的反詐騙軟體，因為一個好的網站的Alexa Traffic Rank、PR以及Pages indexed（索引數）等等都會相對較高。

![Open SEO Stats](http://toolbox.phodal.com/images/fe-plugins/seo-stats.jpg)

除了基本的SEO狀態顯示，它還提供了一些有效的工具，來幫助我們優化頁面的SEO。如在Page Info裡，會羅列出頁面的相關標籤是否完整。在Links Stats裡，會幫我們檢查頁面的外鏈情況等等。

PageSpeed Insights
---

這是Google的PageSpeed Insights的外掛版（網頁版見： [https://developers.google.com/speed/pagespeed/insights/](https://developers.google.com/speed/pagespeed/insights/)），一個非常棒的網頁優化工具，有了它就可以讓我們輕鬆對網頁進行優化。我們所需要做的事情就是點選“分析”按鈕，然後就坐等他分析完成。

如下就是我部落格的一個分析結果：

![PageSpeed Insights](http://toolbox.phodal.com/images/fe-plugins/pagespeed.jpg)

總體分數98分，看來我針對這個所說的東西進行優化的效果還不錯。左邊顯示了我部落格存在的一些問題，如：

 - 沒有壓縮CSS
 - 可以使用瀏覽器快取
 - 需要指定快取驗證工具
 - 暫緩JavaScript解析
 - 將查詢字元從靜態資源中刪除

等等的幾個問題——這些已經都是小問題了。所以他們的重要等級是“低”，一般來說如果有一個等級是“高”整個評分就會特別低。

除此，我們還可以使用命令列工具來對你的網頁進行測試。

[https://github.com/addyosmani/psi](https://github.com/addyosmani/psi)

安裝：

``` shell
$ npm install --global psi
```

只需要執行下面的命令即可：

``` shell
psi http://www.example.com/
```

如我的部落格的結果:

``` shell
--------------------------------------------------------

URL:       phodal.com
Strategy:  mobile
Speed:     90
Usability: 96

CSS size                                   | 30.04 kB
HTML size                                  | 11.8 kB
Image size                                 | 41.08 kB
JavaScript size                            | 28.07 kB
CSS resources                              | 1
Hosts                                      | 2
JS resources                               | 1
Resources                                  | 5
Static resources                           | 3
Total size of request bytes sent           | 695 B

Leverage browser caching                   | 1.5
Main resource server response time         | %
```

再依據不同的結果對網頁進化優化，不過它有一個前提是它並不適合SPA（單頁面）應用。

Postman
---

我相信這個軟體，搞過Web開發的人都聽過。

![Chrome Postman](http://toolbox.phodal.com/images/fe-plugins/postman.jpg)

它是一款功能強大的網頁偵錯與傳送網頁HTTP請求的Chrome外掛。總之，就是我們可以在瀏覽器上執行GET、POST等等的測試。在偵錯遠端API的時候很有用，一般在偵錯本地API的時候，我都是用jQuery的。

同樣的，你仍然可以使用命令列工具來測試它，即[Newman](https://github.com/postmanlabs/newman)。由於其沒有UI，它可以執行在CI上，並編寫相應的UI測試。

XPath Helper
---

這是我在寫UI自動化測試的時候使用的工具，由於那是一個遺留項目，所以我們都對整體UI的佈局都不是特別熟悉。並且由於業務推進的關係，我們並沒有足夠的時候去解決這個問題，於是就開始使用這個工具來完成工作了。

在編寫的時候我們會在Console用jQuery去選定元素，然後再將其轉換為XPath。接著在這個工具上嘗試，如下圖顯示：

![XPath Helper](http://toolbox.phodal.com/images/fe-plugins/xpath.jpg)

最後，我們將會寫到程式碼中。

ObservePoint Tag Debugger
---

這是一個可以用於偵錯各種Web分析工具的外掛，它可以用於分析SiteCat、Google Analytics、WebTrend等發出的事件請求，並解析其資料。

![ObservePoint Tag Debugger](http://toolbox.phodal.com/images/fe-plugins/observerPoint.jpg)

Capture Webpage Screenshot Entirely
---

這是一個截圖工具，可以用於擷取頁面長圖。
