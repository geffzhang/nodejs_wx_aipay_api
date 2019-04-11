# 个人支付免签系统 Api 版本

  技术栈 eggJs + mysql + Vue

  项目说明： 解决个人网站微信支付宝收款；
  
   ### demo演示是基于普通版 https://github.com/yioMe/node_wx_alipay_personalPay 项目，支付宝必须上传二维码，不支持h5唤醒！API版无需上传支 付宝二维码，支持h5唤醒支付 https://github.com/yioMe/nodejs_wx_aipay_api api版没有演示地址，请自行搭建或观看视频教程！

  支付Demo地址: http://pay.yio.me/#/goods/DwnNGCW4VLk1CjemIiUqf

  客户端地址： http://pay.yio.me/#/goods/74ct1zBzZBW8YGFBKe-Yf

  注:安卓客户端不提供源代码，仅提供App安装文件;
  
## 最后一次更新 2019年04月07日11:35:36

  1. 最新版支付宝(10.1.60)已经支持h5唤醒支付，将支付宝二维码地址使用a标签href属性即可，具体用法可参考视频教程，之前的版本请按照 app/controller/order.js 第127行修改，注：目前可以唤醒的不用理会本次更新;
  
  2. 唤醒演示 https://pan.baidu.com/s/1kQMkfCyTCqb-pQoURE8aSg 
  
  ### 2019年03月03日08:04:26 更新

  1. 解决支付宝二维码生成限制，无需上传支付宝二维码;

  2. 增加视频教程;
  
## 视频教程
    
   https://pan.baidu.com/s/1czuBjaTIT2hwC215yQ-FlQ

## 文本教程

  1. 安装 node.js mysql 环境，并将此项目所有文件下载到服务器任意目录上面；

  2. 进入项目根目录,找到 config/config.default.js 文件按照提示修改所需配置， 进入database/config.js 文件修改 development 数据库配置信息；

  3. 在根目录中打开命令行， 执行 npm install 安装依赖文件；

  4. 在根目录中打开命令行， 执行 npx sequelize db:migrate  创建数据表结构； 注： 是npx 不是 npm；

  5. 在根目录中打开命令行， 执行 npm start 启动应用,默认端口7001； 注： npm stop 停止应用;

  6. 访问 http://你的服务器地址:端口号/index.html 注：必须带index.html


## Api文档

  下载本项目后，进入DocApi目录，使用浏览器打开index.html文件即可;

  你只需要关注 ↓

  order - 创建支付订单

  无需关注↓

  android - 接收推送客户端信息

  android - 验证客户端
  
 ## 客户端配置

  api 地址填写： http(s)://你的服务器地址/addons/pay/ 注意：必须以反斜杠结尾

  签名密匙填写： config/config.default.js 里的 secretkey 值

  点击保存提示配置成功即可，没有其他设置!
  
 ## 开启微信/支付宝收款通知
 
  微信->钱包->二维码收款->开启收款到账语音提醒  

  注：（如果微信在PC登录了，请在手机微信中关闭手机静音，或退出PC微信）

  支付宝->收钱->开启收款到账语音提醒
  
 ## 注意
 
  1.收款二维码是定额的二维码不是你的微信二维码，二维码收款->设置金额->保存收款二维码（不能修改任何文字信息，否则会无法识别报404）;
  
  2.服务器一定要是外网，否则支付宝付款时无法找到正确的二维码地址;

 ## 疑问

  问：资金多久到账？

  答： 实时到账，直接到账微信/支付宝余额，不经过任何第三方；

  问：会掉单吗？

  答： 保持客户端和服务端网络畅通99.99%不会掉单!

  问：这个服务端是什么意思，客户端是什么意思?

  答: 服务端源码是用来接收客户端推送收款信息，客户端是监听支付宝和微信的收款信息并实时推送到服务器;

  问: 微信公众号可以使用吗?

  答： 可以使用微信，长按二维码即可直接支付；
  
  问：如何联系到你
  
  答： 邮件 a@yio.me 
  
  ## 特别注意
    提供支付搭建技术支持。不提供、不参与对接具体的业务；

