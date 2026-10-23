# poi-plugin-ooi-autofill

在 poi 里记录 [OOI](https://ooi.moe/) 登录页的账号和密码，并在地址匹配的登录页自动填入。

凭据只写入本机 poi 配置，不会上传。插件不会自动点击「登录游戏」。

## 安装

在 poi 的插件设置里安装 npm 包 `poi-plugin-ooi-autofill`。

也可以在 poi 的插件目录里安装：

```bat
cd %APPDATA%\poi\plugins
npm install poi-plugin-ooi-autofill
```

安装后重启 poi，打开插件设置，填写登录 ID 和密码。站点地址默认是 `ooi.moe`。

## 开发

按 [poi 插件文档](https://dev.poi.moe/docs/guides/debugging) 用 `npm link` 加载本地版本：

```bat
cd poi-plugin-ooi-autofill
npm link
cd %APPDATA%\poi\plugins
npm link poi-plugin-ooi-autofill
```

## 行为

- 只在主机名与设置完全一致，且页面含有 OOI 登录框时填入 `#login_id` 和 `#password`
- 可选自动勾选「在POI中运行」
- 不会自动点击「登录游戏」
