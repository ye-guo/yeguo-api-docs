---
order: 4
group:
  title: API服务
  path: /qrcode-encode
---

# 二维码生成

## ℹ️ 接口信息

- **接口状态：** <div style="display: inline-block; background-color: #bad80a; color: #fff; padding: 2px; border-radius: 5px; width: 40px; height: 20px; text-align: center; line-height: 20px;">正常</div>
- **接口描述：** 生成指定内容的二维码
- **请求方式：** `GET`
- **返回格式：** `JSON`
- **接口地址：** `https://gw.yeguo.icu/api/qrcode/encode`
- **请求示例：** `https://gw.yeguo.icu/api/qrcode/encode?accessKey=***&signature=***&text=https://api.yeguo.icu`

## 🔢 请求参数

| 参数名 | 必填 | 类型   | 说明                       |
| ------ | ---- | ------ | -------------------------- |
| text   | 是   | string | 文本内容                   |
| m      | 否   | number | 边距，可选值{0,10}，默认 2 |

## 💬 响应参数

| 参数名称 | 类型   | 说明                             |
| -------- | ------ | -------------------------------- |
|          | string | 返回 svg，在线调用会格式化为图片 |

## 📜 代码示例

:::info{title=提示}
没有开发者调用凭证无法调用接口， <a href="https://api.yeguo.icu/person" target="_blank" rel="noopener noreferrer">前往获取开发者凭证</a>
:::

- **方式一: 自动注入， 推荐**

**application.yml 配置凭证**

```yml
yeguo:
  api:
    access-key: your-accessKey
    secret-key: your-secretKey
```

**调用接口**

```js
@Autowired
private YGApiClient ygApiClient;

try {
      String result = ygApiClient.getQrcodeEncode("https://api.yeguo.icu");
      System.out.println(result);
    } catch (YGApiException e) {
        log.error("调用API接口异常", e);
      }

```

- **方式二：主动实例化**

```js
try {
      String accessKey = "your-accessKey";
      String secretKey = "your-secretKey";
      ygApiClient = new YGApiClient(accessKey,secretKey);
      String result = ygApiClient.getQrcodeEncode("https://api.yeguo.icu");
      System.out.println(result);
    } catch (YGApiException e) {
        log.error("调用API接口异常", e);
      }
```

## 📝 响应示例

```json
<svg xmlns="http://www.w3.org/2000/svg" class="qr-svg qrcode" viewBox="0 0 29 29" preserveAspectRatio="xMidYMid">
<path class="qr-data light qrcode" fill="#fff" d="M11 2 h1 v1 h-1Z M12 2 h1 v1 h-1Z M15 2 h1 v1 h-1Z M17 2 h1 v1 h-1Z M13 3 h1 v1 h-1Z M14 3 h1 v1 h-1Z M17 3 h1 v1 h-1Z M11 4 h1 v1 h-1Z M12 4 h1 v1 h-1Z M13 4 h1 v1 h-1Z M15 4 h1 v1 h-1Z M16 4 h1 v1 h-1Z M17 4 h1 v1 h-1Z M11 5 h1 v1 h-1Z M12 5 h1 v1 h-1Z M13 5 h1 v1 h-1Z M16 5 h1 v1 h-1Z M12 6 h1 v1 h-1Z M13 6 h1 v1 h-1Z M14 6 h1 v1 h-1Z M16 6 h1 v1 h-1Z M17 6 h1 v1 h-1Z M11 7 h1 v1 h-1Z M12 7 h1 v1 h-1Z M15 7 h1 v1 h-1Z M16 7 h1 v1 h-1Z M17 7 h1 v1 h-1Z M11 9 h1 v1 h-1Z M14 9 h1 v1 h-1Z M15 9 h1 v1 h-1Z M17 9 h1 v1 h-1Z M12 10 h1 v1 h-1Z M14 10 h1 v1 h-1Z M2 11 h1 v1 h-1Z M3 11 h1 v1 h-1Z M4 11 h1 v1 h-1Z M5 11 h1 v1 h-1Z M10 11 h1 v1 h-1Z M12 11 h1 v1 h-1Z M13 11 h1 v1 h-1Z M15 11 h1 v1 h-1Z M18 11 h1 v1 h-1Z M20 11 h1 v1 h-1Z M26 11 h1 v1 h-1Z M2 12 h1 v1 h-1Z M3 12 h1 v1 h-1Z M9 12 h1 v1 h-1Z M10 12 h1 v1 h-1Z M11 12 h1 v1 h-1Z M13 12 h1 v1 h-1Z M14 12 h1 v1 h-1Z M16 12 h1 v1 h-1Z M19 12 h1 v1 h-1Z M22 12 h1 v1 h-1Z M24 12 h1 v1 h-1Z M3 13 h1 v1 h-1Z M4 13 h1 v1 h-1Z M5 13 h1 v1 h-1Z M9 13 h1 v1 h-1Z M10 13 h1 v1 h-1Z M12 13 h1 v1 h-1Z M13 13 h1 v1 h-1Z M15 13 h1 v1 h-1Z M19 13 h1 v1 h-1Z M21 13 h1 v1 h-1Z M22 13 h1 v1 h-1Z M24 13 h1 v1 h-1Z M25 13 h1 v1 h-1Z M5 14 h1 v1 h-1Z M10 14 h1 v1 h-1Z M12 14 h1 v1 h-1Z M15 14 h1 v1 h-1Z M16 14 h1 v1 h-1Z M19 14 h1 v1 h-1Z M22 14 h1 v1 h-1Z M23 14 h1 v1 h-1Z M24 14 h1 v1 h-1Z M25 14 h1 v1 h-1Z M3 15 h1 v1 h-1Z M4 15 h1 v1 h-1Z M6 15 h1 v1 h-1Z M10 15 h1 v1 h-1Z M11 15 h1 v1 h-1Z M12 15 h1 v1 h-1Z M13 15 h1 v1 h-1Z M14 15 h1 v1 h-1Z M15 15 h1 v1 h-1Z M19 15 h1 v1 h-1Z M20 15 h1 v1 h-1Z M22 15 h1 v1 h-1Z M23 15 h1 v1 h-1Z M24 15 h1 v1 h-1Z M26 15 h1 v1 h-1Z M3 16 h1 v1 h-1Z M4 16 h1 v1 h-1Z M5 16 h1 v1 h-1Z M9 16 h1 v1 h-1Z M10 16 h1 v1 h-1Z M15 16 h1 v1 h-1Z M19 16 h1 v1 h-1Z
M20 16 h1 v1 h-1Z M24 16 h1 v1 h-1Z M3 17 h1 v1 h-1Z M4 17 h1 v1 h-1Z M14 17 h1 v1 h-1Z M15 17 h1 v1 h-1Z M16 17 h1 v1 h-1Z M17 17 h1 v1 h-1Z M18 17 h1 v1 h-1Z M22 17 h1 v1 h-1Z M25 17 h1 v1 h-1Z M3 18 h1 v1 h-1Z M6 18 h1 v1 h-1Z M7 18 h1 v1 h-1Z M10 18 h1 v1 h-1Z M12 18 h1 v1 h-1Z M14 18 h1 v1 h-1Z M15 18 h1 v1 h-1Z M16 18 h1 v1 h-1Z M23 18 h1 v1 h-1Z M25 18 h1 v1 h-1Z M26 18 h1 v1 h-1Z M11 19 h1 v1 h-1Z M12 19 h1 v1 h-1Z M13 19 h1 v1 h-1Z M16 19 h1 v1 h-1Z M17 19 h1 v1 h-1Z M23 19 h1 v1 h-1Z M24 19 h1 v1 h-1Z M25 19 h1 v1 h-1Z M26 19 h1 v1 h-1Z M14 20 h1 v1 h-1Z M15 20 h1 v1 h-1Z M16 20 h1 v1 h-1Z M17 20 h1 v1 h-1Z M23 20 h1 v1 h-1Z M24 20 h1 v1 h-1Z M25 20 h1 v1 h-1Z M12 21 h1 v1 h-1Z M13 21 h1 v1 h-1Z M16 21 h1 v1 h-1Z M23 21 h1 v1 h-1Z M24 21 h1 v1 h-1Z M13 22 h1 v1 h-1Z M15 22 h1 v1 h-1Z M23 22 h1 v1 h-1Z M12 23 h1 v1 h-1Z M13 23 h1 v1 h-1Z M14 23 h1 v1 h-1Z M15 23 h1 v1 h-1Z M19 23 h1 v1 h-1Z M21 23 h1 v1 h-1Z M22 23 h1 v1 h-1Z M23 23 h1 v1 h-1Z M24 23 h1 v1 h-1Z M15 24 h1 v1 h-1Z M16 24 h1 v1 h-1Z M19 24 h1 v1 h-1Z M20 24 h1 v1 h-1Z M21 24 h1 v1 h-1Z M22 24 h1 v1 h-1Z M25 24 h1 v1 h-1Z M11 25 h1 v1 h-1Z M12 25 h1 v1 h-1Z M14 25 h1 v1 h-1Z M15 25 h1 v1 h-1Z M20 25 h1 v1 h-1Z M23 25 h1 v1 h-1Z M24 25 h1 v1 h-1Z M25 25 h1 v1 h-1Z M12 26 h1 v1 h-1Z M13 26 h1 v1 h-1Z M14 26 h1 v1 h-1Z M17 26 h1 v1 h-1Z M20 26 h1 v1 h-1Z M21 26 h1 v1 h-1Z M22 26 h1 v1 h-1Z M24 26 h1 v1 h-1Z M25 26 h1 v1 h-1Z"/>
<path class="qr-finder light qrcode" fill="#fff" d="M3 3 h1 v1 h-1Z M4 3 h1 v1 h-1Z M5 3 h1 v1 h-1Z M6 3 h1 v1 h-1Z M7 3 h1 v1 h-1Z M21 3 h1 v1 h-1Z M22 3 h1 v1 h-1Z M23 3 h1 v1 h-1Z M24 3 h1 v1 h-1Z M25 3 h1 v1 h-1Z M3 4 h1 v1 h-1Z M7 4 h1 v1 h-1Z M21 4 h1 v1 h-1Z M25 4 h1 v1 h-1Z M3 5 h1 v1 h-1Z M7 5 h1 v1 h-1Z M21 5 h1 v1 h-1Z M25 5 h1 v1 h-1Z M3 6 h1 v1 h-1Z M7 6 h1 v1 h-1Z M21 6 h1 v1 h-1Z M25 6 h1 v1 h-1Z M3 7 h1 v1 h-1Z M4 7 h1 v1 h-1Z M5 7 h1 v1 h-1Z M6 7 h1 v1 h-1Z M7 7 h1 v1 h-1Z M21 7 h1 v1 h-1Z M22 7 h1 v1 h-1Z M23 7 h1 v1 h-1Z M24 7 h1 v1 h-1Z M25 7 h1 v1 h-1Z M3 21 h1 v1 h-1Z M4 21 h1 v1 h-1Z M5 21 h1 v1 h-1Z M6 21 h1 v1 h-1Z M7 21 h1 v1 h-1Z M3 22 h1 v1 h-1Z M7 22 h1 v1 h-1Z M3 23 h1 v1 h-1Z M7 23 h1 v1 h-1Z M3 24 h1 v1 h-1Z M7 24 h1 v1 h-1Z M3 25 h1 v1 h-1Z M4 25 h1 v1 h-1Z M5 25 h1 v1 h-1Z M6 25 h1 v1 h-1Z M7 25 h1 v1 h-1Z"/>
<path class="qr-separator light qrcode" fill="#fff" d="M9 2 h1 v1 h-1Z M19 2 h1 v1 h-1Z M9 3 h1 v1 h-1Z M19 3 h1 v1 h-1Z M9 4 h1 v1 h-1Z M19 4 h1 v1 h-1Z M9 5 h1 v1 h-1Z M19 5 h1 v1 h-1Z M9 6 h1 v1 h-1Z M19 6 h1 v1 h-1Z M9 7 h1 v1 h-1Z M19 7 h1 v1 h-1Z M9 8 h1 v1 h-1Z M19 8 h1 v1 h-1Z M2 9 h1 v1 h-1Z M3 9 h1 v1 h-1Z M4 9 h1 v1 h-1Z M5 9 h1 v1 h-1Z M6 9 h1 v1 h-1Z M7 9 h1 v1 h-1Z M8 9 h1 v1 h-1Z M9 9 h1 v1 h-1Z M19 9 h1 v1 h-1Z M20 9 h1 v1 h-1Z M21 9 h1 v1 h-1Z M22 9 h1 v1 h-1Z M23 9 h1 v1 h-1Z M24 9 h1 v1 h-1Z M25 9 h1 v1 h-1Z M26 9 h1 v1 h-1Z M2 19 h1 v1 h-1Z M3 19 h1 v1 h-1Z M4 19 h1 v1 h-1Z M5 19 h1 v1 h-1Z M6 19 h1 v1 h-1Z M7 19 h1 v1 h-1Z M8 19 h1 v1 h-1Z M9 19 h1 v1 h-1Z M9 20 h1 v1 h-1Z M9 21 h1 v1 h-1Z M9 22 h1 v1 h-1Z M9 23 h1 v1 h-1Z M9 24 h1 v1 h-1Z M9 25 h1 v1 h-1Z M9 26 h1 v1 h-1Z"/>
<path class="qr-alignment light qrcode" fill="#fff" d="M19 19 h1 v1 h-1Z M20 19 h1 v1 h-1Z M21 19 h1 v1 h-1Z M19 20 h1 v1 h-1Z M21 20 h1 v1 h-1Z M19 21 h1 v1 h-1Z M20 21 h1 v1 h-1Z M21 21 h1 v1 h-1Z"/>
<path class="qr-timing light qrcode" fill="#fff" d="M11 8 h1 v1 h-1Z M13 8 h1 v1 h-1Z M15 8 h1 v1 h-1Z M17 8 h1 v1 h-1Z M8 11 h1 v1 h-1Z M8 13 h1 v1 h-1Z M8 15 h1 v1 h-1Z M8 17 h1 v1 h-1Z"/>
<path class="qr-format light qrcode" fill="#fff" d="M10 2 h1 v1 h-1Z M10 3 h1 v1 h-1Z M10 4 h1 v1 h-1Z M10 7 h1 v1 h-1Z M10 9 h1 v1 h-1Z M4 10 h1 v1 h-1Z M5 10 h1 v1 h-1Z M6 10 h1 v1 h-1Z M10 10 h1 v1 h-1Z M19 10 h1 v1 h-1Z M20 10 h1 v1 h-1Z M21 10 h1 v1 h-1Z M24 10 h1 v1 h-1Z M25 10 h1 v1 h-1Z M26 10 h1 v1 h-1Z M10 22 h1 v1 h-1Z M10 23 h1 v1 h-1Z M10 24 h1 v1 h-1Z"/>
<path class="qr-quietzone light qrcode" fill="#fff" d="M0 0 h1 v1 h-1Z M1 0 h1 v1 h-1Z M2 0 h1 v1 h-1Z M3 0 h1 v1 h-1Z M4 0 h1 v1 h-1Z M5 0 h1 v1 h-1Z M6 0 h1 v1 h-1Z M7 0 h1 v1 h-1Z M8 0 h1 v1 h-1Z M9 0 h1 v1 h-1Z M10 0 h1 v1 h-1Z M11 0 h1 v1 h-1Z M12 0 h1 v1 h-1Z M13 0 h1 v1 h-1Z M14 0 h1 v1 h-1Z M15 0 h1 v1 h-1Z M16 0 h1 v1 h-1Z M17 0 h1 v1 h-1Z M18 0 h1 v1 h-1Z M19 0 h1 v1 h-1Z M20 0 h1 v1 h-1Z M21 0 h1 v1 h-1Z M22 0 h1 v1 h-1Z M23 0 h1 v1 h-1Z M24 0 h1 v1 h-1Z M25 0 h1 v1 h-1Z M26 0 h1 v1 h-1Z M27 0 h1 v1 h-1Z M28 0 h1 v1 h-1Z M0 1 h1 v1 h-1Z M1 1 h1 v1 h-1Z M2 1 h1 v1 h-1Z M3 1 h1 v1 h-1Z M4 1 h1 v1 h-1Z M5 1 h1 v1 h-1Z M6 1 h1 v1 h-1Z M7 1 h1 v1 h-1Z M8 1 h1 v1 h-1Z M9 1 h1 v1 h-1Z M10 1 h1 v1 h-1Z M11 1 h1 v1 h-1Z M12 1 h1 v1 h-1Z M13 1 h1 v1 h-1Z M14 1 h1 v1 h-1Z M15 1 h1 v1 h-1Z M16 1 h1 v1 h-1Z M17 1 h1 v1 h-1Z M18 1 h1 v1 h-1Z M19 1 h1 v1 h-1Z M20 1 h1 v1 h-1Z M21 1 h1 v1 h-1Z M22 1 h1 v1 h-1Z M23 1 h1 v1 h-1Z M24 1 h1 v1 h-1Z M25 1 h1 v1 h-1Z M26 1 h1 v1 h-1Z M27 1 h1 v1 h-1Z M28 1 h1 v1 h-1Z M0 2 h1 v1 h-1Z M1 2 h1 v1 h-1Z M27 2 h1 v1 h-1Z M28 2 h1 v1 h-1Z M0 3 h1 v1 h-1Z M1 3 h1 v1 h-1Z M27 3 h1 v1 h-1Z M28 3 h1 v1 h-1Z M0 4 h1 v1 h-1Z M1 4 h1 v1 h-1Z M27 4 h1 v1 h-1Z M28 4 h1 v1 h-1Z M0 5 h1 v1 h-1Z M1 5 h1 v1 h-1Z M27 5 h1 v1 h-1Z M28 5 h1 v1 h-1Z M0 6 h1 v1 h-1Z M1 6 h1 v1 h-1Z M27 6 h1 v1 h-1Z M28 6 h1 v1 h-1Z M0 7 h1 v1 h-1Z M1 7 h1 v1 h-1Z M27 7 h1 v1 h-1Z M28 7 h1 v1 h-1Z M0 8 h1 v1 h-1Z M1 8 h1 v1 h-1Z M27 8 h1 v1 h-1Z M28 8 h1 v1 h-1Z M0 9 h1 v1 h-1Z M1 9 h1 v1 h-1Z M27 9 h1 v1 h-1Z M28 9 h1 v1 h-1Z M0 10 h1 v1 h-1Z M1 10 h1 v1 h-1Z M27 10 h1 v1 h-1Z M28 10 h1 v1 h-1Z M0 11 h1 v1 h-1Z M1 11 h1 v1 h-1Z M27 11 h1 v1 h-1Z M28 11 h1 v1 h-1Z M0 12 h1 v1 h-1Z M1 12 h1 v1 h-1Z
M27 12 h1 v1 h-1Z M28 12 h1 v1 h-1Z M0 13 h1 v1 h-1Z M1 13 h1 v1 h-1Z M27 13 h1 v1 h-1Z M28 13 h1 v1 h-1Z M0 14 h1 v1 h-1Z M1 14 h1 v1 h-1Z M27 14 h1 v1 h-1Z M28 14 h1 v1 h-1Z M0 15 h1 v1 h-1Z M1 15 h1 v1 h-1Z M27 15 h1 v1 h-1Z M28 15 h1 v1 h-1Z M0 16 h1 v1 h-1Z M1 16 h1 v1 h-1Z M27 16 h1 v1 h-1Z M28 16 h1 v1 h-1Z M0 17 h1 v1 h-1Z M1 17 h1 v1 h-1Z M27 17 h1 v1 h-1Z M28 17 h1 v1 h-1Z M0 18 h1 v1 h-1Z M1 18 h1 v1 h-1Z M27 18 h1 v1 h-1Z M28 18 h1 v1 h-1Z M0 19 h1 v1 h-1Z M1 19 h1 v1 h-1Z M27 19 h1 v1 h-1Z M28 19 h1 v1 h-1Z M0 20 h1 v1 h-1Z M1 20 h1 v1 h-1Z M27 20 h1 v1 h-1Z M28 20 h1 v1 h-1Z M0 21 h1 v1 h-1Z M1 21 h1 v1 h-1Z M27 21 h1 v1 h-1Z M28 21 h1 v1 h-1Z M0 22 h1 v1 h-1Z M1 22 h1 v1 h-1Z M27 22 h1 v1 h-1Z M28 22 h1 v1 h-1Z M0 23 h1 v1 h-1Z M1 23 h1 v1 h-1Z M27 23 h1 v1 h-1Z M28 23 h1 v1 h-1Z M0 24 h1 v1 h-1Z M1 24 h1 v1 h-1Z M27 24 h1 v1 h-1Z M28 24 h1 v1 h-1Z M0 25 h1 v1 h-1Z M1 25 h1 v1 h-1Z M27 25 h1 v1 h-1Z M28 25 h1 v1 h-1Z M0 26 h1 v1 h-1Z M1 26 h1 v1 h-1Z M27 26 h1 v1 h-1Z M28 26 h1 v1 h-1Z M0 27 h1 v1 h-1Z M1 27 h1 v1 h-1Z M2 27 h1 v1 h-1Z M3 27 h1 v1 h-1Z M4 27 h1 v1 h-1Z M5 27 h1 v1 h-1Z M6 27 h1 v1 h-1Z M7 27 h1 v1 h-1Z M8 27 h1 v1 h-1Z M9 27 h1 v1 h-1Z M10 27 h1 v1 h-1Z M11 27 h1 v1 h-1Z M12 27 h1 v1 h-1Z M13 27 h1 v1 h-1Z M14 27 h1 v1 h-1Z M15 27 h1 v1 h-1Z M16 27 h1 v1 h-1Z M17 27 h1 v1 h-1Z M18 27 h1 v1 h-1Z M19 27 h1 v1 h-1Z M20 27 h1 v1 h-1Z M21 27 h1 v1 h-1Z M22 27 h1 v1 h-1Z M23 27 h1 v1 h-1Z M24 27 h1 v1 h-1Z M25 27 h1 v1 h-1Z M26 27 h1 v1 h-1Z M27 27 h1 v1 h-1Z M28 27 h1 v1 h-1Z M0 28 h1 v1 h-1Z M1 28 h1 v1 h-1Z M2 28 h1 v1 h-1Z M3 28 h1 v1 h-1Z M4 28 h1 v1 h-1Z M5 28 h1 v1 h-1Z M6 28 h1 v1 h-1Z M7 28 h1 v1 h-1Z M8 28 h1 v1 h-1Z M9 28 h1 v1 h-1Z M10 28 h1 v1 h-1Z M11 28 h1 v1 h-1Z M12 28 h1 v1 h-1Z
M13 28 h1 v1 h-1Z M14 28 h1 v1 h-1Z M15 28 h1 v1 h-1Z M16 28 h1 v1 h-1Z M17 28 h1 v1 h-1Z M18 28 h1 v1 h-1Z M19 28 h1 v1 h-1Z M20 28 h1 v1 h-1Z M21 28 h1 v1 h-1Z M22 28 h1 v1 h-1Z M23 28 h1 v1 h-1Z M24 28 h1 v1 h-1Z M25 28 h1 v1 h-1Z M26 28 h1 v1 h-1Z M27 28 h1 v1 h-1Z M28 28 h1 v1 h-1Z"/>
<path class="qr-darkmodule dark qrcode" fill="#000" d="M10 19 h1 v1 h-1Z"/>
<path class="qr-data-dark dark qrcode" fill="#000" d="M13 2 h1 v1 h-1Z M14 2 h1 v1 h-1Z M16 2 h1 v1 h-1Z M18 2 h1 v1 h-1Z M11 3 h1 v1 h-1Z M12 3 h1 v1 h-1Z M15 3 h1 v1 h-1Z M16 3 h1 v1 h-1Z M18 3 h1 v1 h-1Z M14 4 h1 v1 h-1Z M18 4 h1 v1 h-1Z M14 5 h1 v1 h-1Z M15 5 h1 v1 h-1Z M17 5 h1 v1 h-1Z M18 5 h1 v1 h-1Z M11 6 h1 v1 h-1Z M15 6 h1 v1 h-1Z M18 6 h1 v1 h-1Z M13 7 h1 v1 h-1Z M14 7 h1 v1 h-1Z M18 7 h1 v1 h-1Z M12 9 h1 v1 h-1Z M13 9 h1 v1 h-1Z M16 9 h1 v1 h-1Z M18 9 h1 v1 h-1Z M11 10 h1 v1 h-1Z M13 10 h1 v1 h-1Z M15 10 h1 v1 h-1Z M16 10 h1 v1 h-1Z M17 10 h1 v1 h-1Z M18 10 h1 v1 h-1Z M6 11 h1 v1 h-1Z M7 11 h1 v1 h-1Z M9 11 h1 v1 h-1Z M11 11 h1 v1 h-1Z M14 11 h1 v1 h-1Z M16 11 h1 v1 h-1Z M17 11 h1 v1 h-1Z M19 11 h1 v1 h-1Z M21 11 h1 v1 h-1Z M22 11 h1 v1 h-1Z M23 11 h1 v1 h-1Z M24 11 h1 v1 h-1Z M25 11 h1 v1 h-1Z M4 12 h1 v1 h-1Z M5 12 h1 v1 h-1Z M6 12 h1 v1 h-1Z M7 12 h1 v1 h-1Z M12 12 h1 v1 h-1Z M15 12 h1 v1 h-1Z M17 12 h1 v1 h-1Z M18 12 h1 v1 h-1Z M20 12 h1 v1 h-1Z M21 12 h1 v1 h-1Z M23 12 h1 v1 h-1Z M25 12 h1 v1 h-1Z M26 12 h1 v1 h-1Z M2 13 h1 v1 h-1Z M6 13 h1 v1 h-1Z M7 13 h1 v1 h-1Z M11 13 h1 v1 h-1Z M14 13 h1 v1 h-1Z M16 13 h1 v1 h-1Z M17 13 h1 v1 h-1Z M18 13 h1 v1 h-1Z M20 13 h1 v1 h-1Z M23 13 h1 v1 h-1Z M26 13 h1 v1 h-1Z M2 14 h1 v1 h-1Z M3 14 h1 v1 h-1Z M4 14 h1 v1 h-1Z M6 14 h1 v1 h-1Z M7 14 h1 v1 h-1Z M9 14 h1 v1 h-1Z M11 14 h1 v1 h-1Z M13 14 h1 v1 h-1Z M14 14 h1 v1 h-1Z M17 14 h1 v1 h-1Z M18 14 h1 v1 h-1Z M20 14 h1 v1 h-1Z M21 14 h1 v1 h-1Z M26 14 h1 v1 h-1Z M2 15 h1 v1 h-1Z M5 15 h1 v1 h-1Z M7 15 h1 v1 h-1Z M9 15 h1 v1 h-1Z M16 15 h1 v1 h-1Z M17 15 h1 v1 h-1Z M18 15 h1 v1 h-1Z M21 15 h1 v1 h-1Z M25 15 h1 v1 h-1Z M2 16 h1 v1 h-1Z M6 16 h1 v1 h-1Z M7 16 h1 v1 h-1Z M11 16 h1 v1 h-1Z M12 16 h1 v1 h-1Z M13 16 h1 v1 h-1Z M14 16 h1 v1 h-1Z M16 16 h1 v1 h-1Z M17 16 h1 v1 h-1Z
M18 16 h1 v1 h-1Z M21 16 h1 v1 h-1Z M22 16 h1 v1 h-1Z M23 16 h1 v1 h-1Z M25 16 h1 v1 h-1Z M26 16 h1 v1 h-1Z M2 17 h1 v1 h-1Z M5 17 h1 v1 h-1Z M6 17 h1 v1 h-1Z M7 17 h1 v1 h-1Z M9 17 h1 v1 h-1Z M10 17 h1 v1 h-1Z M11 17 h1 v1 h-1Z M12 17 h1 v1 h-1Z M13 17 h1 v1 h-1Z M19 17 h1 v1 h-1Z M20 17 h1 v1 h-1Z M21 17 h1 v1 h-1Z M23 17 h1 v1 h-1Z M24 17 h1 v1 h-1Z M26 17 h1 v1 h-1Z M2 18 h1 v1 h-1Z M4 18 h1 v1 h-1Z M5 18 h1 v1 h-1Z M9 18 h1 v1 h-1Z M11 18 h1 v1 h-1Z M13 18 h1 v1 h-1Z M17 18 h1 v1 h-1Z M24 18 h1 v1 h-1Z M14 19 h1 v1 h-1Z M15 19 h1 v1 h-1Z M11 20 h1 v1 h-1Z M12 20 h1 v1 h-1Z M13 20 h1 v1 h-1Z M26 20 h1 v1 h-1Z M11 21 h1 v1 h-1Z M14 21 h1 v1 h-1Z M15 21 h1 v1 h-1Z M17 21 h1 v1 h-1Z M25 21 h1 v1 h-1Z M26 21 h1 v1 h-1Z M11 22 h1 v1 h-1Z M12 22 h1 v1 h-1Z M14 22 h1 v1 h-1Z M16 22 h1 v1 h-1Z M17 22 h1 v1 h-1Z M24 22 h1 v1 h-1Z M25 22 h1 v1 h-1Z M26 22 h1 v1 h-1Z M11 23 h1 v1 h-1Z M16 23 h1 v1 h-1Z M17 23 h1 v1 h-1Z M18 23 h1 v1 h-1Z M20 23 h1 v1 h-1Z M25 23 h1 v1 h-1Z M26 23 h1 v1 h-1Z M11 24 h1 v1 h-1Z M12 24 h1 v1 h-1Z M13 24 h1 v1 h-1Z M14 24 h1 v1 h-1Z M17 24 h1 v1 h-1Z M18 24 h1 v1 h-1Z M23 24 h1 v1 h-1Z M24 24 h1 v1 h-1Z M26 24 h1 v1 h-1Z M13 25 h1 v1 h-1Z M16 25 h1 v1 h-1Z M17 25 h1 v1 h-1Z M18 25 h1 v1 h-1Z M19 25 h1 v1 h-1Z M21 25 h1 v1 h-1Z M22 25 h1 v1 h-1Z M26 25 h1 v1 h-1Z M11 26 h1 v1 h-1Z M15 26 h1 v1 h-1Z M16 26 h1 v1 h-1Z M18 26 h1 v1 h-1Z M19 26 h1 v1 h-1Z M23 26 h1 v1 h-1Z M26 26 h1 v1 h-1Z"/>
<path class="qr-finder-dark dark qrcode" fill="#000" d="M2 2 h1 v1 h-1Z M3 2 h1 v1 h-1Z M4 2 h1 v1 h-1Z M5 2 h1 v1 h-1Z M6 2 h1 v1 h-1Z M7 2 h1 v1 h-1Z M8 2 h1 v1 h-1Z M20 2 h1 v1 h-1Z M21 2 h1 v1 h-1Z M22 2 h1 v1 h-1Z M23 2 h1 v1 h-1Z M24 2 h1 v1 h-1Z M25 2 h1 v1 h-1Z M26 2 h1 v1 h-1Z M2 3 h1 v1 h-1Z M8 3 h1 v1 h-1Z M20 3 h1 v1 h-1Z M26 3 h1 v1 h-1Z M2 4 h1 v1 h-1Z M8 4 h1 v1 h-1Z M20 4 h1 v1 h-1Z M26 4 h1 v1 h-1Z M2 5 h1 v1 h-1Z M8 5 h1 v1 h-1Z M20 5 h1 v1 h-1Z M26 5 h1 v1 h-1Z M2 6 h1 v1 h-1Z M8 6 h1 v1 h-1Z M20 6 h1 v1 h-1Z M26 6 h1 v1 h-1Z M2 7 h1 v1 h-1Z M8 7 h1 v1 h-1Z M20 7 h1 v1 h-1Z M26 7 h1 v1 h-1Z M2 8 h1 v1 h-1Z M3 8 h1 v1 h-1Z M4 8 h1 v1 h-1Z M5 8 h1 v1 h-1Z M6 8 h1 v1 h-1Z M7 8 h1 v1 h-1Z M8 8 h1 v1 h-1Z M20 8 h1 v1 h-1Z M21 8 h1 v1 h-1Z M22 8 h1 v1 h-1Z M23 8 h1 v1 h-1Z M24 8 h1 v1 h-1Z M25 8 h1 v1 h-1Z M26 8 h1 v1 h-1Z M2 20 h1 v1 h-1Z M3 20 h1 v1 h-1Z M4 20 h1 v1 h-1Z M5 20 h1 v1 h-1Z M6 20 h1 v1 h-1Z M7 20 h1 v1 h-1Z M8 20 h1 v1 h-1Z M2 21 h1 v1 h-1Z M8 21 h1 v1 h-1Z M2 22 h1 v1 h-1Z M8 22 h1 v1 h-1Z M2 23 h1 v1 h-1Z M8 23 h1 v1 h-1Z M2 24 h1 v1 h-1Z M8 24 h1 v1 h-1Z M2 25 h1 v1 h-1Z M8 25 h1 v1 h-1Z M2 26 h1 v1 h-1Z M3 26 h1 v1 h-1Z M4 26 h1 v1 h-1Z M5 26 h1 v1 h-1Z M6 26 h1 v1 h-1Z M7 26 h1 v1 h-1Z M8 26 h1 v1 h-1Z"/>
<path class="qr-alignment-dark dark qrcode" fill="#000" d="M18 18 h1 v1 h-1Z M19 18 h1 v1 h-1Z M20 18 h1 v1 h-1Z M21 18 h1 v1 h-1Z M22 18 h1 v1 h-1Z M18 19 h1 v1 h-1Z M22 19 h1 v1 h-1Z M18 20 h1 v1 h-1Z M20 20 h1 v1 h-1Z M22 20 h1 v1 h-1Z M18 21 h1 v1 h-1Z M22 21 h1 v1 h-1Z M18 22 h1 v1 h-1Z M19 22 h1 v1 h-1Z M20 22 h1 v1 h-1Z M21 22 h1 v1 h-1Z M22 22 h1 v1 h-1Z"/>
<path class="qr-timing-dark dark qrcode" fill="#000" d="M10 8 h1 v1 h-1Z M12 8 h1 v1 h-1Z M14 8 h1 v1 h-1Z M16 8 h1 v1 h-1Z M18 8 h1 v1 h-1Z M8 10 h1 v1 h-1Z M8 12 h1 v1 h-1Z M8 14 h1 v1 h-1Z M8 16 h1 v1 h-1Z M8 18 h1 v1 h-1Z"/>
<path class="qr-format-dark dark qrcode" fill="#000" d="M10 5 h1 v1 h-1Z M10 6 h1 v1 h-1Z M2 10 h1 v1 h-1Z M3 10 h1 v1 h-1Z M7 10 h1 v1 h-1Z M9 10 h1 v1 h-1Z M22 10 h1 v1 h-1Z M23 10 h1 v1 h-1Z M10 20 h1 v1 h-1Z M10 21 h1 v1 h-1Z M10 25 h1 v1 h-1Z M10 26 h1 v1 h-1Z"/>
<path class="qr-finder-dot dark qrcode" fill="#000" d="M4 4 h1 v1 h-1Z M5 4 h1 v1 h-1Z M6 4 h1 v1 h-1Z M22 4 h1 v1 h-1Z M23 4 h1 v1 h-1Z M24 4 h1 v1 h-1Z M4 5 h1 v1 h-1Z M5 5 h1 v1 h-1Z M6 5 h1 v1 h-1Z M22 5 h1 v1 h-1Z M23 5 h1 v1 h-1Z M24 5 h1 v1 h-1Z M4 6 h1 v1 h-1Z M5 6 h1 v1 h-1Z M6 6 h1 v1 h-1Z M22 6 h1 v1 h-1Z M23 6 h1 v1 h-1Z M24 6 h1 v1 h-1Z M4 22 h1 v1 h-1Z M5 22 h1 v1 h-1Z M6 22 h1 v1 h-1Z M4 23 h1 v1 h-1Z M5 23 h1 v1 h-1Z M6 23 h1 v1 h-1Z M4 24 h1 v1 h-1Z M5 24 h1 v1 h-1Z M6 24 h1 v1 h-1Z"/>
</svg>
```

## 🐞 提供 bug 反馈或建议

- [YG-API-SDK GitHub Issue](https://github.com/ye-guo/yeguo-api-sdk/issues/new/choose)
- [YG-API-Docs GitHub Issue](https://github.com/ye-guo/yeguo-api-docs/issues/new/choose)
