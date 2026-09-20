# WenServer Wiki

服务器数据包中文百科导航站（整合全部子 Wiki）。

## 目录

```
WenServer Wiki/
├── index.html                 # 导航首页
├── assets/app.css
├── .nojekyll
├── gravestone/
├── DungeonsAndTaverns/
├── DnT-End-Castle/
├── DungeonsAndTaverns-Mineshaft/
├── Incendium/
├── DeadlyDeadlyDungeon/
├── RedasMoreStructures/
└── WenServer/
```

每个子文件夹内含完整站点（`index.html` + `assets/`），可单独部署。

## 本地预览

```bash
cd "WenServer Wiki"
python -m http.server 8080
# 打开 http://localhost:8080
```

## GitHub Pages（整站）

把 **本目录内全部文件** 推到仓库根，Settings → Pages 选 `main` / `(root)`。
导航页会通过相对路径进入各子站点。

## 单独部署某个子 Wiki

例如只部署地牢与酒馆：将 `DungeonsAndTaverns/` 内的 `index.html` 与 `assets/` 复制到仓库根后开启 Pages。

## 说明

- 版式仿 zh.minecraft.wiki，与 gravestone 子站一致
- 搜索：输入时只更新结果列表，不隐藏正文
- 中文名优先取数据包 lang / WenServer 材质包
