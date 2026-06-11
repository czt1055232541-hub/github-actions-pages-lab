# GitHub 新手可视化学习讲义

## 0. 当前状态

本练习仓库通过 GitHub 插件写入和管理；如果浏览器可访问 GitHub，也可以对照网页界面观察每一步。
你可以把插件操作理解为“我替你点击了 GitHub 的保存按钮”，每次写入都会留下 commit 记录。

## 1. 认识 GitHub 的核心概念

- Repository：项目仓库，像一个带历史记录的项目文件夹。
- Commit：一次保存，像“给当前项目拍一张快照”。
- Branch：分支，像复制一条安全试验线，不直接影响主线。
- Pull Request：把分支改动合回主线前的展示、讨论和检查页面。
- Issue：任务卡片，用来记录问题、需求和待办。
- Actions：自动化机器人，帮你检查、构建、部署。
- Pages：GitHub 提供的静态网站托管。

## 2. 创建练习仓库

1. 打开 GitHub。
2. 点击右上角 `+`，选择 `New repository`。
3. Repository name 输入 `github-actions-pages-lab`。
4. 选择 `Public`。
5. 可以不勾选初始化 README，因为模板里已经准备好了。
6. 创建仓库。

## 3. 上传模板文件

推荐方式：

1. 在仓库首页点击 `Add file`。
2. 选择 `Upload files`。
3. 上传本文件夹里的全部内容。
4. Commit message 填：`Create GitHub Actions Pages lab`。
5. 点击 `Commit changes`。

如果你会用命令行，可以在本文件夹执行：

```powershell
git init
git branch -M main
git add .
git commit -m "Create GitHub Actions Pages lab"
git remote add origin https://github.com/<你的用户名>/github-actions-pages-lab.git
git push -u origin main
```

## 4. 练习分支和 Pull Request

1. 在仓库页面点击分支下拉框。
2. 输入 `feature/homepage-text` 并创建新分支。
3. 打开 `index.html`，点击编辑。
4. 修改页面中的一段文字。
5. Commit 到 `feature/homepage-text`。
6. 点击 `Compare & pull request`。
7. PR 标题写：`Update homepage text`。
8. 查看 `Files changed`，理解差异。
9. 点击 `Merge pull request`。

## 5. 启用 GitHub Pages 自动部署

1. 进入仓库 `Settings`。
2. 左侧打开 `Pages`。
3. Source 选择 `GitHub Actions`。
4. 回到 `Actions` 页面。
5. 找到 `Deploy static site to GitHub Pages`。
6. 等待运行成功。
7. 打开部署出来的 Pages URL。

## 6. 练习 Actions 失败和修复

1. 打开 `Actions`。
2. 选择 `Intentional failure demo`。
3. 点击 `Run workflow`。
4. 等待它失败。
5. 打开失败 job，看 `Fail intentionally` 这一步。
6. 理解：红叉不是灾难，是系统告诉你哪一步失败。
7. 修复方式：把 `.github/workflows/intentional-failure-demo.yml` 里的 `run: exit 1` 改成 `run: echo "Fixed"`。
8. 再运行一次，确认成功。

## 7. 用 Issue 管理任务

1. 打开 `Issues`。
2. 创建 Issue：`改进首页学习说明`。
3. 正文写：`让首页更清楚地说明这是 GitHub Actions 和 Pages 的练习项目。`
4. 新建分支修改首页。
5. 打开 PR，在描述里写 `Closes #1`。
6. 合并 PR 后，Issue 会自动关闭。

## 8. 自测清单

- 我知道 Repository、Commit、Branch、Pull Request、Issue、Actions、Pages 是什么。
- 我能创建仓库并上传文件。
- 我能创建分支并打开 PR。
- 我能看懂 PR 的文件差异。
- 我能合并 PR。
- 我能打开 Actions 日志。
- 我能启用 GitHub Pages 并访问部署页面。
- 我知道失败日志应该从红色步骤开始看。
