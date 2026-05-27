# TikTok / Business API 合规站（GitHub Pages）

托管：**`app.bayme.store`** → CNAME `write125.github.io` · 仓库 [Write125/qisimiaoxiang-pages](https://github.com/Write125/qisimiaoxiang-pages)

## 页面

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
