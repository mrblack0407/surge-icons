# surge-icons

自用的 Surge 策略组图标。收录主流图标库（Koolson/Qure、Orz-3/mini、lige47/QuanX-icon-rule、luestr/IconResource、Repcz/Tool 等）里**找不到**的图标，以及少数虽然有、但想换个版本自己托管的图标。

全部取自各公司官网素材，统一处理为 **256×256 PNG**。

## 图标

| 预览 | 文件 | 说明 | 原始素材 |
| --- | --- | --- | --- |
| <img src="icons/Blizzard.png" width="48"> | `Blizzard.png` | BLIZZ 字标，黑底蓝字，带透明圆角 | blizzard.com 官方 favicon，原生 256×256 RGBA |
| <img src="icons/Wargaming.png" width="48"> | `Wargaming.png` | Wargaming 红色环形箭头标识 | wargaming.net 官方 apple-touch-icon，180×180 放大至 256 |
| <img src="icons/Telegram.png" width="48"> | `Telegram.png` | 蓝色渐变圆形 + 白色纸飞机，圆外透明 | telegram.org 官方 `t_logo_2x.png`，原生 256×256 RGBA |

## 用法

在 Surge 配置的 `[Proxy Group]` 里用 `icon-url` 引用：

```
Blizzard  = select, DIRECT, 节点选择, icon-url=https://cdn.jsdelivr.net/gh/mrblack0407/surge-icons@main/icons/Blizzard.png
Wargaming = select, DIRECT, 节点选择, icon-url=https://cdn.jsdelivr.net/gh/mrblack0407/surge-icons@main/icons/Wargaming.png
Telegram  = select, DIRECT, 节点选择, icon-url=https://cdn.jsdelivr.net/gh/mrblack0407/surge-icons@main/icons/Telegram.png
```

jsdelivr 的 `@main` 有 CDN 缓存，图标更新后生效可能有延迟；要立刻看到改动就换 GitHub raw：

```
https://raw.githubusercontent.com/mrblack0407/surge-icons/main/icons/Blizzard.png
```

## 为什么不直接用官方直链

- blizzard.com 的 favicon 文件名带哈希，官网改版即失效；且服务端返回的 `Content-Type` 是 `image/vnd.microsoft.icon`（尽管内容是 PNG），部分客户端不渲染。
- wargaming.net 只提供 180×180 一档，没有更大尺寸。
- telegram.org 的图标链接本身稳定，但是境外域名，客户端拉图标时不一定走代理。

转存到这里可以保证链接稳定、`Content-Type` 正确。

## 关于版权

图标均为各公司的注册商标，著作权归 Blizzard Entertainment, Inc.、Wargaming Group Limited 与 Telegram 所有。此处转存仅用于个人代理配置的界面显示，不作任何商业用途，也不主张任何权利。原权利方如有异议请提 Issue，会立即移除。
