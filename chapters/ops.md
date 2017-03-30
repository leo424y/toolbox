Ops
======

Nginx Pagespeed
---

> ngx_pagespeed 是 Nginx 的一個擴充套件模組，主要的功能是針對前端頁面而進行伺服器端的優化，對前端設計人員來說，可以省去優化css、js以及圖片的過程。ngx_pagespeed對nginx自身負載能力的提升基本是看不到的，甚至會因為進行伺服器端的優化而使系統增加負載；但從減少客戶請求數的角度去看，犧牲部分伺服器效能還是值得的

主要功能如下：

 - 影象優化：剝離後設資料、動態調整，重新壓縮
 - CSS和JavaScript壓縮、合併、級聯、內聯
 - 小資源內聯
 - 推遲影象和JavaScript載入
 - 對HTML重寫、壓縮空格、去除註釋等
 - 提升快取週期
 - 以及其他config_filters

Boom
---

Boom是一個用Go語言實現的壓力測試工具，就是和Apache Bench類似的工具。它提供了一個很有意思的UI，這就是我為什麼推薦他的原因了：

```
1000 / 1000 Boooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooooo! 100.00 %

Summary:
  Total:    1.9052 secs.
  Slowest:  0.2054 secs.
  Fastest:  0.0111 secs.
  Average:  0.1817 secs.
  Requests/sec: 524.8813
  Total Data Received:  5459000 bytes.
  Response Size per Request:    5459 bytes.

Status code distribution:
  [200] 1000 responses

Response time histogram:
  0.011 [1] |
  0.031 [10]    |
  0.050 [10]    |
  0.069 [11]    |
  0.089 [11]    |
  0.108 [10]    |
  0.128 [11]    |
  0.147 [11]    |
  0.167 [11]    |
  0.186 [295]   |∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎
  0.205 [619]   |∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎∎

Latency distribution:
  10% in 0.1764 secs.
  25% in 0.1841 secs.
  50% in 0.1892 secs.
  75% in 0.1942 secs.
  90% in 0.2011 secs.
  95% in 0.2024 secs.
  99% in 0.2038 secs.
```

GoAccess
---

> GoAccess是一款開源、實時，執行在命令列終端下的web日誌分析工具。該工具提供快速、多樣的HTTP狀態統計，可以令管理員不再糾結於統計各類資料，和繁雜的指令以及一大堆管道/正規表示式說byebye。

這生成的風格是這樣的：

![GoAccess](http://toolbox.phodal.com/images/ops/goaccess-dashboard.png)


它可以輕鬆統計出訪問概況、動態頁面請求、靜態頁面請求（如圖片、樣式表、指令碼等）、訪客排名，訪客使用的作業系統，訪客使用的瀏覽器，來路域名，404 錯誤，搜尋爬蟲，搜尋關鍵詞等等。

而，我們所要做的只需要執行：

```shell
goaccess -f access.log
```

Fabric
---

因為我的部落格是基於Django框架而開發的，我偏向於使用Python作為開發語言，所以我需要選擇了Fabric作為運維工具。


> Fabric 是一個 Python (2.5-2.7) 庫和命令列工具，用來流水線化執行 SSH以部署應用或系統管理任務。

更具體地說，Fabric 是：

 - 一個讓你通過 命令列 執行 任意 Python 函數 的工具；
 - 一個讓通過 SSH 執行 Shell 命令更加 容易 和 蟒樣 的子程式庫（建立於一個更低層次的庫）。

Docker
---

> Docker是一個開源的引擎，可以輕鬆的為任何應用建立一個輕量級的、可移植的、自給自足的容器。

Jenkins
---

> Jenkins是一個用Java編寫的開源的持續整合工具。Jenkins提供了軟體開發的持續整合服務。它執行在Servlet容器中（例如Apache Tomcat）。它支援軟體配置管理（SCM）工具，可以執行基於Apache Ant和Apache Maven的項目，以及任意的Shell指令碼和Windows批處理命令。

除了將Jenkins有於持續整合環境外，我們還可以使用Jenkins來完成一些自動化的部署工作。
