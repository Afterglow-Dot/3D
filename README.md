# 我的个人网站（3D 版）

这是我的个人网站仓库，基于 [jekyll-theme-chirpy](https://github.com/cotes2020/jekyll-theme-chirpy) 主题搭建。  
网站用于记录研究生期间的学习、科研和生活，也会分享课程笔记、代码实践和日常思考。

- 🌐 网站地址：<https://afterglow-dot.github.io/3D/>
- 📝 定位：研究生在读，通信工程，记录学习和生活。

---

## 📁 项目结构

| 目录 / 文件          | 作用                                                       |
| :------------------- | :--------------------------------------------------------- |
| `_config.yml`        | 网站全局配置：标题、作者、URL、baseurl、内容集合、默认设置 |
| `index.html`         | 首页入口，走 `_layouts/home.html`                          |
| `_posts/`            | 文章：技术方法、工具用法、文献精读、读研经验               |
| `_research/`         | 科研进展：实验记录、组会汇报                               |
| `_publications/`     | 学术成果：论文、专利、软著                                 |
| `_life/`             | 日常记录：心情、读书随感、小事                             |
| `_tabs/`             | 左侧导航栏各页面，`order` 控制排序                         |
| `_layouts/`          | 自定义布局：`home`、`3d`（3D 世界）、`custom-collection`   |
| `_includes/`         | `world-items` 给 3D 页喂数据；其余为主题同名文件的覆盖版   |
| `_plugins/`          | 生成分类/标签归档页、用 git 提交时间填最后修改时间         |
| `_data/`             | 数据文件：联系方式、分享平台                               |
| `assets/`            | 图片、CSS、JS 等静态资源                                   |
| `tools/`             | `run.sh` 本地预览、`test.sh` 生产构建与检查                |
| `.github/workflows/` | GitHub Actions 自动部署配置                                |

---

## ✍️ 写作栏目

四个栏目按内容性质分开，写的时候不用纠结「这篇放哪」。

- **文章**（`_posts/`）：写完能给别人看的正式内容，会进 RSS 订阅。
- **科研进展**（`_research/`）：记下「什么时候做了什么、结果如何」，以后写论文时翻这里。
- **学术成果**（`_publications/`）：一篇论文或一个专利一条记录。
- **日常记录**（`_life/`）：不用讲究结构，想到什么写什么。

新建文件命名 `YYYY-MM-DD-标题.md`，前三者用 `layout: post`，`_publications` 用 `layout: page`。

---

## 🚀 部署方式

每次向 `main` 分支推送代码，GitHub Actions 都会自动构建网站并部署到 GitHub Pages。不需要手动操作。

- 查看部署状态：进入 GitHub 仓库的 **Actions** 页面。
- 构建流程：Jekyll 构建 → htmlproofer 检查 → 发布 Pages。
- 如果 Actions 显示红色叉号，点进去查看报错日志，本地用 `bash tools/test.sh` 复现。

---

## 🎨 自定义外观

- **赛博皮肤**：`assets/css/cyber-skin.scss`，深空底色 + 霓虹渐变 + 玻璃拟态，**仅在暗色模式下生效**；亮/暗/跟随系统由侧栏按钮切换。
- **星空背景**：`assets/js/starfield.js`，全站固定 canvas 上的多层视差星点。
- **纵深交互**：`assets/js/cyber-depth.js`，文章滚动入场、3D 翻页过渡、回到顶部。
- **标签星球**：`assets/js/tag-sphere.js`，`/tags/` 页可拖拽旋转的标签球。
- **3D 世界**：`/world/` 页由 `assets/js/3d-world.js`（three.js）渲染，每个分类一座书架、每篇文章一本书。
- **减弱动效**：以上动效都尊重 `prefers-reduced-motion`，用户开启后自动退化为静态页面。

---

## 📄 许可证与致谢

- 主题：[jekyll-theme-chirpy](https://github.com/cotes2020/jekyll-theme-chirpy)，遵循 MIT 许可证。
- 3D 渲染：[three.js](https://threejs.org/)，遵循 MIT 许可证。
- 本站内容（博客文章、图片等）版权归 Dajie Li 所有，未经允许请勿转载。

---

© 2026 Dajie Li. 保留所有权利。
