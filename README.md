Loon 部分远程JS配置

HOST添加(*待补充*)

`Surge & QX MITM = api.termius.com`

京东去广告、Banner

```
http-response ^https?://api\.m\.jd\.com/client\.action\?functionId=(start|myOrderInfo|orderTrackBusiness) requires-body=1,max-size=-1,script-path=https://raw.githubusercontent.com/iCirno/qxLoon/master/Loon/JDAdRemove.js
```

什么值得买去广告

```
http-response ^https?:\/\/(h(aojia|omepage)|(articl|baik)e|s)-api\.smzdm\.com\/(home|sou) requires-body=1,max-size=-1,script-path=https://raw.githubusercontent.com/iCirno/qxLoon/master/Loon/SMZDM.js
```

B站App去广告整合（N脚本合一）

```
http-response ^https?:\/\/ap(i|p).(live.)?bilibili.com\/x(live)?\/(resource\/show\/tab|v2\/(reply\/main|view\/material|account\/(mine|teenagers\/status)|view|feed\/index|show\/popular\/index|rank)|app-room/v1/index/getInfoByRoom)\?access_key requires-body=1,max-size=-1,script-path=https://raw.githubusercontent.com/iCirno/qxLoon/master/Loon/Bilibili.js
```

知乎去广告整合（N脚本合一）

```
http-response ^https?:\/\/(api|www)\.zhihu\.com\/(moments(\/recommend)?\?(action|feed_type)|topstory\/recommend|.*\/questions|market\/header|people|appview\/(v2|p)\/(answer\/)?\d{1,10}\?no\_image\=false(\&article\_fixed\_bottom\=1)?\&X\-SUGER\=) requires-body=1,max-size=-1,script-path=https://raw.githubusercontent.com/iCirno/qxLoon/master/Loon/Zhihu.js
```

丁香园用药助手解锁订阅

```
http-response ^https?:\/\/newdrugs\.dxy\.cn\/app\/user\/(p(ay\/checkIntroOfferPeriod|ro\/stat)|init)\? requires-body=1,script-path=https://raw.githubusercontent.com/iCirno/qxLoon/master/Loon/DingXiangDrugs.js
```

Lightroom解锁订阅（langkhach）

```
http-response ^https:\/\/photos\.adobe\.io\/v2\/accounts requires-body=1,script-path=https://raw.githubusercontent.com/iCirno/qxLoon/master/Loon/Lightroom.js
```

Photoshop解锁订阅（langkhach）

```
http-response ^https://lcs-mobile-cops.adobe.io/mobile_profile/nul/v1 requires-body=1,script-path=https://raw.githubusercontent.com/iCirno/qxLoon/master/Loon/Photoshop.js
```

淘宝历史价格，二合一修正（yichahucha）

```
http-response ^https?://(amdc|trade-acs)\.m\.taobao\.com/(amdc/mobileDispatch|gw/mtop\.taobao\.detail\.getdetail) requires-
```