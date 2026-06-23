# 视频分段加速代理服务器，go语言版本,for TVbox spider

## 原理：多线程、协程等分段请求视频数据然后返回给播放器，以起到加速的作用

## api

1. 默认端口12345 ，若被占用就+1。
2. http://127.0.0.1:12345//buildUrl ，post请求，请求体为json {"url":"","headers":{},"key":""},key为md5（url）
3. http://127.0.0.1:12345/proxy?key=&threads=  ,key为md5（url）,threads为并发数
4. http://127.0.0.1:12345/ ,返回`ser200`，说明服务器正常
