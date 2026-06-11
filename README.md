# GitHub Actions Pages Lab

这是一个 GitHub 新手练习仓库，用来学习：

- Repository：项目仓库，保存代码和历史记录。
- Commit：一次保存，记录“改了什么”和“为什么改”。
- Branch：分支，用来安全尝试新改动。
- Pull Request：把分支改动提交给主分支前的讨论和检查区。
- Issue：任务、问题和想法的记录卡片。
- GitHub Actions：自动执行检查、构建和部署。
- GitHub Pages：把静态网页发布成可访问的网站。

## 练习目标

1. 创建仓库并提交 `README.md` 和 `index.html`。
2. 建立分支，修改首页文字。
3. 打开 Pull Request，查看差异并合并。
4. 用 GitHub Actions 发布 GitHub Pages。
5. 故意制造一次 Actions 失败，读懂日志，再修复。
6. 用 Issue 记录一个改进任务，并用 PR 关闭它。

## 文件说明

- `index.html`：练习网站首页。
- `.github/workflows/pages.yml`：GitHub Pages 自动部署流程。
- `.github/workflows/intentional-failure-demo.yml`：教学用失败流程，默认不会自动运行。
- `docs/learning-guide.md`：完整分步学习讲义。

## 推荐仓库设置

- Repository name：`github-actions-pages-lab`
- Visibility：`Public`
- GitHub Pages source：`GitHub Actions`
