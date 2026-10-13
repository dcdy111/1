# 微信智能跳转页面

一个基于纯 HTML 实现的轻量级智能跳转页面。

该项目通过识别用户访问环境，自动将用户引导至不同目标页面：

- 微信内置浏览器访问：跳转至企业微信用户入口；
- 普通浏览器访问：跳转至微信小店商品页面。

## 项目特点

- 纯前端实现，无需后端服务；
- 页面加载后自动检测浏览器环境；
- 根据 User-Agent 判断是否为微信环境；
- 部署简单，可直接用于 GitHub Pages、静态服务器等场景。

## 技术栈

- HTML5
- JavaScript
- CSS

## 项目结构

```text
.
├── index.html   # 主页面，实现环境判断和自动跳转
└── README.md    # 项目说明文档
```

## 工作流程

```text
用户访问页面
        |
        v
JavaScript 获取浏览器 User-Agent
        |
        +----------------+
        |                |
        v                v
微信内置浏览器       普通浏览器
        |                |
        v                v
企业微信入口       微信小店页面
```

## 使用方式

1. 下载项目：

```bash
git clone https://github.com/dcdy111/1.git
```

2. 使用浏览器打开 `index.html`。

3. 根据访问环境自动完成页面跳转。

## 部署方式

### GitHub Pages

1. 将仓库上传至 GitHub；
2. 开启 GitHub Pages；
3. 访问 Pages 提供的网址即可使用。

### 静态服务器

将项目文件放入任意 Web 服务器目录即可，例如：

- Nginx
- Apache
- CDN 静态托管服务

## 注意事项

- 跳转逻辑依赖浏览器 User-Agent 判断；
- 部分浏览器可能修改 User-Agent，导致识别结果异常；
- 修改跳转地址时，请编辑 `index.html` 中对应的 `window.location.href`。

## License

仅用于学习、测试和个人项目展示。