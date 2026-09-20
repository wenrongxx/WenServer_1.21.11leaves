# 墓石地牢 Wiki — GitHub Pages 站点

本目录是 **GitHub Pages 的部署根**，只含网页所需文件。

## 目录结构

```
web/
├── index.html          # 入口页
├── assets/
│   ├── app.css         # 样式
│   ├── img/            # 图标与结构截图
│   ├── favicon-*.png
│   └── apple-touch-icon.png
├── site.webmanifest
├── .nojekyll           # 关闭 Jekyll
└── README.md           # 本文件
```

## 部署步骤

1. 新建 GitHub 仓库（例如 `gravestone-dungeons-wiki`）。
2. 把 **`web/` 目录里的内容**（不是 `web` 文件夹本身）推到仓库根目录：

```bash
cd web
git init
git add .
git commit -m "墓石地牢中文 Wiki"
git branch -M main
git remote add origin git@github.com:<用户名>/gravestone-dungeons-wiki.git
git push -u origin main
```

或在已有仓库中将 `web/*` 复制到仓库根后再推送。

3. **Settings → Pages**：
   - Source: `Deploy from a branch`
   - Branch: `main` / `(root)`
4. 访问 `https://<用户名>.github.io/gravestone-dungeons-wiki/`

页面使用相对路径，部署在子路径（`/仓库名/`）下无需修改。

## 本地预览

```bash
cd web
python -m http.server 8080
# 打开 http://localhost:8080
```

## 说明

- 离线单文件版见上级目录 `墓石地牢Wiki-离线版.html`（不参与 Pages 部署）。
- 数据包资料在上级目录 `datapack/`，与站点无关，可不必上传。
