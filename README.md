# SiteNote 官网

> 静态站。无 JS 依赖，无构建工具。HTML + CSS。

---

## 本地预览

```bash
cd /Users/banruo/Developer/sitenote-website
python3 -m http.server 8000
```

浏览器访问：<http://localhost:8000/>

按 `Ctrl+C` 停止。

---

## 部署到 GitHub Pages

```bash
cd /Users/banruo/Developer/sitenote-website
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/<你的用户名>/sitenote-site.git
git push -u origin main
```

然后在 GitHub repo Settings → Pages → Deploy from main branch / root → Save。

等 1-2 分钟，URL 形如：
```
https://<你的用户名>.github.io/sitenote-site/
```

把这个 URL 填进：
- App Store Connect → App Information → Privacy Policy URL: `https://.../privacy.html`
- App Store Connect → Support URL: `https://.../support.html`
- App Store Connect → Marketing URL: `https://.../`（首页）

---

## 文件结构

```
sitenote-website/
├── index.html        # 首页（hero + features + scenarios + trust）
├── privacy.html      # 隐私政策（中英双语）
├── support.html      # 支持 + FAQ
├── terms.html        # 使用条款
├── css/
│   └── style.css     # 全部样式
├── images/
│   └── icon.png      # App icon (1024x1024)
└── README.md         # 本文件
```

---

## 设计原则

- **Industrial 极简**：与 App 内 Ink 配色一致（黑/白/橙）
- **无第三方依赖**：纯 HTML + CSS，没有 framework
- **可离线**：所有资源都是相对路径
- **响应式**：手机、平板、桌面都能看
- **A11y**：语义化 HTML、合理的对比度

---

## 后续扩展

- [ ] 上架后加入真实 App Store 截图
- [ ] 加 "下载" 按钮指向 App Store URL（拿到链接后）
- [ ] 加 v1.1 / v2 更新日志页
- [ ] 加博客（如果你想写工地工程师 + AI 相关的）
- [ ] 加 favicon variants（16x16, 32x32, 等）

---

## 改文案

每个 HTML 都是独立文件。改文字直接在 HTML 编辑即可。
所有页面共享 `css/style.css`，改样式只需要改这一个文件。
