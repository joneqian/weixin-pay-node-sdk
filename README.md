# weixin-pay-node-sdk

<a name="O8p0G"></a>

# 一、概述

weixin-pay-node-sdk 是微信支付 sdk。

<a name="xlIgq"></a>

# 二、使用方法

## 安装

```shell
npm install weixin-pay-node-sdk --save
```

## 引用依赖库

```js
const wxpay = require('weixin-pay-node-sdk');
```

## 初始化

```js
const config = {
  appid: '公众号APPID',
  mchid: '商户号ID',
  partnerKey: '商户号API密钥',
  pfx: fs.readFileSync('证书文件'),
  notify_url: '支付回调网址',
  spbill_create_ip: '服务器IP',
};
const wxpay = new WXPay(config);
```

## 调用

```js
let res_pay = await wxpay.transfers({
  partner_trade_no: '',
  openid: '',
  re_user_name: '',
  amount: 100,
  desc: '',
});
```

## 微信支付 API 文档
https://pay.weixin.qq.com/wiki/doc/api/index.html
