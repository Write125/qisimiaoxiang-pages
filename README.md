# TikTok / Business API 合规站（GitHub Pages）

托管：**`app.bayme.store`** + **`www.bayme.store`** → CNAME `write125.github.io` · 仓库 [Write125/qisimiaoxiang-pages](https://github.com/Write125/qisimiaoxiang-pages)

## 双域名说明

| 子域 | 用途 | GitHub Pages |
|------|------|--------------|
| **app** | OAuth 回调、Terms/Privacy、developer 披露 | `CNAME` 文件主域（必开 HTTPS） |
| **www** | Business 表单「公司官网」 | Settings → Pages → **Add domain** 加第二域名 |

DNS 两条 CNAME 均已指向 `write125.github.io`。若 `app` 404 而 `www` 正常，说明 `CNAME` 文件与 Pages 设置不一致——以 **`app.bayme.store`** 为主（TikTok OAuth 依赖）。

**一次性配置（GitHub 网页）：**

1. 打开 [qisimiaoxiang-pages → Settings → Pages](https://github.com/Write125/qisimiaoxiang-pages/settings/pages)
2. Custom domain 应显示 `app.bayme.store`（来自仓库 `CNAME` 文件）
3. 点 **Add domain**，再填 `www.bayme.store` → 等两个域名的 HTTPS 证书生效（约 5～15 分钟）
4. 自检：`curl -I https://app.bayme.store/` 与 `https://www.bayme.store/` 均 **200**

| 页面 | URL | 用途 |
|------|-----|------|
| 首页 | https://app.bayme.store/ | 公司介绍 + Marketing API 用途 |
| **开发者披露** | https://app.bayme.store/developer.html | **Business 审核专用**（URL 表、数据、流程） |
| Terms | https://app.bayme.store/terms.html | 服务条款直链 |
| Privacy | https://app.bayme.store/privacy.html | 隐私政策直链 |
| OAuth | https://app.bayme.store/oauth.html | 授权回调 |
| URL 验证 | `tiktok*.txt` 根目录 | developers URL properties |

## 部署

```powershell
# 将本目录全部文件复制到 qisimiaoxiang-pages 后：
git add -A
git commit -m "Update Bayme compliance site for Marketing API"
git push origin main
```

等 1～3 分钟 HTTPS 生效。配置说明：[域名与邮箱-bayme.store.md](../TikTok广告自动化/docs/域名与邮箱-bayme.store.md)
