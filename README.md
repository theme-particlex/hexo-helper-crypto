# Hexo-Helper-Crypto

[Hexo-Helper-Crypto](https://github.com/argvchs/hexo-helper-crypto) 插件，用于在模板文件内加/解密数据，使用 Crypto-js

## 安装

```bash
npm i hexo-helper-crypto -S
```

## 使用

在模板文件（以下使用 EJS 模板引擎）中，添加：

```ejs
<% const CryptoJS = cryptojs(); %>
```

然后可以直接使用 `CryptoJS`

以下例子获取了页面标题的 SHA256 值，并用 Base64 编码

```ejs
<% const CryptoJS = cryptojs(); %>
<%= CryptoJS.SHA256(page.title).toString(CryptoJS.enc.Base64) %>
```
