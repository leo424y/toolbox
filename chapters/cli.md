CLI
===

tree
---

> tree命令可以以樹形結構顯示檔案目錄結構，它非常適合於我們給別人介紹我們的檔案目錄的組成框架，同時該命令使用適當的參數也可以將命令結果輸出到文字檔案中。

這個命令非常適用於我們寫作的時候用的，如下就是toolbox下的chapters目錄：

```shell
chapters
├── api.md
├── backend.md
├── chrome-plugins.md
├── cli.md
├── devices.md
├── documents.md
├── graphics.md
├── hardware.md
└── ops.md

0 directories, 9 files
```

sl
---

這是一個神奇的命令列工具，由於兩個手的手速不致，我經常將ls敲成sl。而在Ubuntu上則會提示你，你是不是要安裝sl，於是我就安裝了。然後：

![SL](http://toolbox.phodal.com/images/cli/sl-tool.jpg)

每次我敲錯命令的時候，都會有這個神奇的火車頭出現，火車頭動的期間就只能等它完成。每次這個時候，就說明我們需要休息。

cURL
---

cURL利用URL語法在命令列方式下工作的開原始檔傳輸工具。它是一個很常用的命令，也可以支援檔案上傳和下載。

``` shell
curl -I -s -A 'Googlebot' www.phodal.com
HTTP/1.1 200 OK
Server: mokcy/0.17.9
Content-Type: text/html; charset=utf-8
Connection: keep-alive
Vary: Accept-Encoding
Vary: Accept-Language, Cookie
Content-Language: en
X-UA-Compatible: IE=Edge,chrome=1
Date: Thu, 09 Apr 2015 14:39:11 GMT
X-Page-Speed: Powered By Phodal
Cache-Control: max-age=0, no-cache
```

``` shell
curl --data "_method=PUT&led1=1&sensors1=22&sensors2=12&temperature=14" http://b.phodal.com/athome/1
```
