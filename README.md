# 夜聊 Lite 网页发布包

这个文件夹用于把夜聊 Lite 发布成一个网页链接，方便 iPhone / iPad / 朋友内测访问。

## 包内文件

- `index.html`：夜聊 Lite 完整版页面
- `README.md`：发布说明

## 为什么建议网页发布

iOS 对本地 HTML 文件、微信/QQ 文件预览、Files 文件打开方式支持不稳定，可能出现按钮无响应、localStorage 不工作、弹窗异常等情况。

发布成 HTTPS 网页后，用 Safari 打开会稳定很多。

## 安全说明

- 页面本身不包含你的 API Key。
- API Key 由使用者自己填写。
- API Key 只保存在使用者自己的浏览器 localStorage 中。
- JSON 备份不会包含 API Key。
- 不建议把 API Key 写死进 `index.html`。

## 方式一：GitHub Pages

适合已经有 GitHub 账号的人。

1. 新建一个 GitHub 仓库，例如 `yeliao-lite`。
2. 上传本文件夹里的 `index.html`。
3. 进入仓库设置 `Settings`。
4. 找到 `Pages`。
5. Source 选择 `Deploy from a branch`。
6. Branch 选择 `main`，目录选择 `/root`。
7. 保存后等待 GitHub 生成网址。
8. 把生成的网址发给朋友。

常见网址格式：

```text
https://你的用户名.github.io/yeliao-lite/
```

## 方式二：Cloudflare Pages

适合想要更稳定访问和更快部署的人。

1. 登录 Cloudflare。
2. 进入 `Workers & Pages`。
3. 选择 `Create application`。
4. 选择 `Pages`。
5. 可以从 GitHub 仓库导入，也可以用直接上传方式。
6. 如果直接上传，把本文件夹作为静态站点上传。
7. 构建命令留空。
8. 输出目录填 `/` 或保持默认。
9. 部署完成后，把 Cloudflare 给的网址发给朋友。

## 内测建议

请朋友优先用 Safari 打开链接。

如果是在微信里收到链接，建议：

1. 点右上角菜单。
2. 选择在 Safari 中打开。
3. 再填写 API Key 测试。

## 发布前检查

发布前确认：

- `index.html` 可以在电脑浏览器打开。
- 页面标题是 `夜聊 Lite`。
- 没有把任何真实 API Key 写进文件。
- 上传的是这个发布包里的 `index.html`。

