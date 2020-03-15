个人用Loon远程脚本配置

崩坏3改服

```
# 自定义服务器列表
http-response ^https:\/\/global(.+?)\.bh3\.com\/query_dispatch\?version=.* requires-body=1,max-size=0,script-path=https://raw.githubusercontent.com/iCirno/myLoon/master/Loon/bh3_region_list.js
# 改写连入服务器的客户端标识
http-request ^http:\/\/(.*)\/query_gameserver\?version=.* requires-body=1,max-size=0,script-path=https://raw.githubusercontent.com/iCirno/myLoon/master/Loon/bh3_vid_rewrite.js
```

人人影视

```
http-response ^https:\/\/api\.rr\.tv(\/user\/privilege\/list|\/ad\/getAll|\/rrtv-video\/v4plus\/season\/detail) script-path=https://raw.githubusercontent.com/iCirno/myLoon/master/Loon/rrtv.js, requires-body=true, timeout=10
```

YTB

```
http-request ^https://[\s\S]*\.googlevideo\.com/.*&(oad|ctier) script-path=https://raw.githubusercontent.com/iCirno/myLoon/master/Loon/YouTube.js, timeout=10
```

京东去广告、Banner

```
http-response ^https?://api\.m\.jd\.com/client\.action\?functionId=(start|myOrderInfo|orderTrackBusiness) requires-body=1,max-size=-1,script-path=https://raw.githubusercontent.com/iCirno/myLoon/master/Loon/JDAdRemove.js
```

什么值得买去广告

```
http-response ^https?:\/\/(h(aojia|omepage)|(articl|baik)e|s)-api\.smzdm\.com\/(home|sou) requires-body=1,max-size=-1,script-path=https://raw.githubusercontent.com/iCirno/myLoon/master/Loon/SMZDM.js
```

B站App去广告整合（N脚本合一）

```
http-response ^https?:\/\/ap(i|p).(live.)?bilibili.com\/x(live)?\/(resource\/show\/tab|v2\/(reply\/main|view\/material|account\/(mine|teenagers\/status)|view|feed\/index|show\/popular\/index|rank)|app-room/v1/index/getInfoByRoom)\?access_key requires-body=1,max-size=-1,script-path=https://raw.githubusercontent.com/iCirno/myLoon/master/Loon/Bilibili.js
```

知乎去广告整合（N脚本合一）

```
http-response ^https?:\/\/(api|www)\.zhihu\.com\/(moments(\/recommend)?\?(action|feed_type)|topstory\/recommend|.*\/questions|market\/header|people|appview\/(v2|p)\/(answer\/)?\d{1,10}\?no\_image\=false(\&article\_fixed\_bottom\=1)?\&X\-SUGER\=) requires-body=1,max-size=-1,script-path=https://raw.githubusercontent.com/iCirno/myLoon/master/Loon/Zhihu.js
```

丁香园用药助手解锁订阅

```
http-response ^https?:\/\/newdrugs\.dxy\.cn\/app\/user\/(p(ay\/checkIntroOfferPeriod|ro\/stat)|init)\? requires-body=1,script-path=https://raw.githubusercontent.com/iCirno/myLoon/master/Loon/DingXiangDrugs.js
```

Lightroom解锁订阅（langkhach）

```
http-response ^https:\/\/photos\.adobe\.io\/v2\/accounts requires-body=1,script-path=https://raw.githubusercontent.com/iCirno/myLoon/master/Loon/Lightroom.js
```

Photoshop解锁订阅（langkhach）

```
http-response ^https://lcs-mobile-cops.adobe.io/mobile_profile/nul/v1 requires-body=1,script-path=https://raw.githubusercontent.com/iCirno/myLoon/master/Loon/Photoshop.js
```

淘宝历史价格，二合一修正（yichahucha）

```
http-response ^https?://(amdc|trade-acs)\.m\.taobao\.com/(amdc/mobileDispatch|gw/mtop\.taobao\.detail\.getdetail) requires-
```

HOST添加

`Surge & QX MITM = *.360buyimg.com,*.cnbetacdn.com,*.doubanio.com,*.iydsj.com,*.pstatp.com,*.ydstatic.com,*.youtube.com,*.zymk.cn,101.201.62.22,113.105.222.132,113.96.109.*,118.178.214.118,121.14.89.216,121.9.212.178,14.21.76.30,183.232.237.194,183.232.246.225,183.60.159.227,59.37.96.220,789.kakamobi.cn,a.applovin.com,aarkissltrial.secure2.footprint.net,acs.m.taobao.com,activity2.api.ofo.com,adm.10jqka.com.cn,adproxy.autohome.com.cn,afd.baidu.com,api.app.vhall.com,api.chelaile.net.cn,api.douban.com,api.feng.com,api.fengshows.com,api.gotokeep.com,api.huomao.com,api.jr.mi.com,api.k.sohu.com,api.kkmh.com,api.laifeng.com,api.m.jd.com,api.m.mi.com,api.mddcloud.com.cn,api.psy-1.com,api.smzdm.com,api.tv.sohu.com,api.weibo.cn,api.xiachufang.com,api.zhihu.com,api.zhuishushenqi.com,api5.futunn.com,api-mifit.huami.com,api-mifit-cn.huami.com,api-release.wuta-cam.com,app.10086.cn,app.m.zj.chinamobile.com,app.mixcapp.com,app.wy.guahao.com,app2.autoimg.cn,appsdk.soku.com,atrace.chelaile.net.cn,b.zhuishushenqi.com,c.m.163.com,capi.douyucdn.cn,capi.mwee.cn,cdn.kuaidi100.com,cdn.moji.com,classbox2.kechenggezi.com,client.mail.163.com,connect.facebook.net,consumer.fcbox.com,creatives.ftimg.net,d.1qianbao.com,daoyu.sdo.com,dapis.mting.info,dl.app.gtja.com,dongfeng.alicdn.com,dsp-impr2.youdao.com,e.dangdang.com,erebor.douban.com,fm.fenqile.com,frodo.douban.com,fuss10.elemecdn.com,g1.163.com,gorgon.youdao.com,hm.xiaomi.com,hui.sohu.com,huichuan.sm.cn,i1.hoopchina.com.cn,iface.iqiyi.com,iface2.iqiyi.com,img.jiemian.com,img.zuoyebang.cc,img01.10101111cdn.com,img1.126.net,img1.doubanio.com,img3.doubanio.com,impservice.dictapp.youdao.com,impservice.youdao.com,interface.music.163.com,ios.wps.cn,kano.guahao.cn,lives.l.qq.com,m.aty.sohu.com,m.client.10010.com,m.ibuscloud.com,m.yap.yahoo.com,m5.amap.com,ma.ofo.com,mage.if.qidian.com,mapi.appvipshop.com,mbl.56.com,mimg.127.net,mmg.aty.sohu.com,mmgr.gtimg.com,mp.weixin.qq.com,ms.jr.jd.com,nex.163.com,oimagea4.ydstatic.com,oimagec2.ydstatic.com,p.kuaidi100.com,p1.music.126.net,pic.k.sohu.com,pic1.chelaile.net.cn,pic1cdn.cmbchina.com,pic2.zhimg.com,r.inews.qq.com,resource.cmbchina.com,res-release.wuta-cam.com,ress.dxpmedia.com,rm.aarki.net,rtbapi.douyucdn.cn,service.4gtv.tv,slapi.oray.net,smkmp.96225.com,snailsleep.net,ssl.kohsocialapp.qq.com,sso.ifanr.com,static.api.m.panda.tv,static1.keepcdn.com,staticlive.douyucdn.cn,storage.wax.weibo.com,supportda.ofo.com,ups.youku.com,wapwenku.baidu.com,wenku.baidu.com,www.facebook.com,www.ft.com,www.oschina.net,www.zhihu.com,youtubei.googleapis.com,*.bh3.com,trade-acs.m.taobao.com,api.rr.tv,oauth.secure.pixiv.net,app-api.pixiv.net,education.github.com,*.googlevideo.com,getuserinfo-globalapi.zymk.cn`