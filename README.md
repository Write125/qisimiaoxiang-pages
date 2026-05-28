# TikTok / Business API 合规站（GitHub Pages）

托管：**`www.bayme.store`**（GitHub Pages 主域）· 仓库 [Write125/qisimiaoxiang-pages](https://github.com/Write125/qisimiaoxiang-pages)

## DNS 说明（2026-05-28）

| 主机 | DNS | 说明 |
|------|-----|------|
| **www** | CNAME → `write125.github.io` | 合规站主入口 ✅ |
| **@** | 4× A → GitHub Pages IP | 根域 `bayme.store` 由 GitHub 处理 |
| **app** | 可删除或保留 CNAME | GitHub 只绑一个域，`app` 不再单独 200 |

> DNSPod **显性 URL 转发** 需 ICP 备案，未备案请勿使用。TikTok 全部 URL 统一填 **`www.bayme.store`**。

## 页面

| 页面 | URL |
|------|-----|
| 首页 / 公司官网 | https://www.bayme.store/ |
| **开发者披露** | https://www.bayme.store/developer.html |
| Terms | https://www.bayme.store/terms.html |
| Privacy | https://www.bayme.store/privacy.html |
| OAuth | https://www.bayme.store/oauth.html |
| URL 验证 | https://www.bayme.store/tiktok*.txt |

## 部署

```powershell
# 复制 tiktok-pages/ 到 qisimiaoxiang-pages 后 push
git add -A
git commit -m "sync compliance pages"
git push origin main
```

说明：[域名与邮箱-bayme.store.md](../TikTok广告自动化/docs/域名与邮箱-bayme.store.md)
