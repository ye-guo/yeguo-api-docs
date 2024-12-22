---
order: 0
group:
  title: 签名认证
  path: /singature
  order: 2
---

## 签名串
```js
POST
/xxx/xxx/xxx/xxx
X-Access-Key:xxxxxxxxxx
X-Timestamp:1734665583575
X-Nonce:3ym1x68426q3p256s126e244f2414p

```

## 签名算法
HMAC-SHA256


### 请求头
- X-Access-Key: your-access-key
- X-Timestamp:1734665583575
- X-Nonce:3ym1x68426q3p256s126e244f2414p
- X-Signature:6cfd2a5961c027073511ca7fed1daf2cab4538f79814def0d09eae2586b91545


## 🐞 提供 bug 反馈或建议

- [YG-API-SDK GitHub Issue](https://github.com/ye-guo/yeguo-api-sdk/issues/new/choose)
- [YG-API-Docs GitHub Issue](https://github.com/ye-guo/yeguo-api-docs/issues/new/choose)
