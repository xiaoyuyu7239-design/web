# 水千丞 188 男团人物关系星图

这是一个可部署到 GitHub Pages 的纯静态 MVP 原型，用一个交互式星云关系图展示人物、对象与关系线。

## 文件

- `index.html`：页面、样式、示例数据、交互逻辑都在这里。
- `.nojekyll`：让 GitHub Pages 直接按静态文件发布。

## 本地打开

直接双击 `index.html`，或在浏览器里打开这个文件即可运行。

也可以在项目目录启动一个简单本地服务：

```bash
python3 -m http.server 8080
```

然后访问 `http://localhost:8080`。

## GitHub Pages 部署

1. 新建一个 GitHub 仓库。
2. 上传本目录里的 `index.html`、`README.md`、`.nojekyll`。
3. 进入仓库 `Settings` → `Pages`。
4. 在 `Build and deployment` 里选择 `Deploy from a branch`。
5. 选择 `main` 分支和 `/root` 目录，保存。
6. 等待部署完成后，GitHub 会给出 Pages 访问地址。

## 数据结构

示例数据内置在 `index.html` 的 `graphData` 中：

- `nodes`：人物或对象节点，包含 `id`、`name`、`alias`、`category`、`rank`、`level`、`role`、`bio` 等字段。
- `edges`：关系线，包含 `source`、`target`、`relation`、`event`。

当前内容是 MVP 示例数据，适合先验证视觉和交互。后续可以直接替换 `graphData`，扩展更多人物、作品、事件、阵营、时代、派系或关系说明。
