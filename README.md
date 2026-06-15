# YinRu Portfolio

B 端 UX / 产品设计师个人作品集网站。项目是纯静态站点，正式可部署文件位于 `outputs/`。

## 本地预览

```bash
cd outputs
python -m http.server 8080
```

打开：

```text
http://127.0.0.1:8080/index.html
```

## 推荐部署方式

推荐使用 Cloudflare Pages 或 Netlify，连接 GitHub 仓库后可自动部署，后续每次 `git push` 都会触发线上更新。

### Cloudflare Pages

在 Cloudflare Pages 创建项目并连接 GitHub 仓库：

```text
Framework preset: None
Build command: 留空
Build output directory: outputs
Root directory: /
```

Cloudflare Pages 会发布 `outputs/index.html` 以及 `outputs/assets/` 中的静态资源。

### Netlify

项目已包含 `netlify.toml`，连接 GitHub 仓库后 Netlify 会自动读取发布目录：

```text
Publish directory: outputs
Build command: 留空
```

## 迭代流程

```bash
git add .
git commit -m "update portfolio"
git push
```

部署平台会自动生成新版本。建议日常改版使用新分支，确认无误后再合并到主分支。

## 目录说明

```text
outputs/
  index.html        正式页面
  assets/           页面图片、logo、favicon 等静态资源
  _headers          静态资源缓存与安全响应头
work/               设计过程截图与临时对照素材
```

