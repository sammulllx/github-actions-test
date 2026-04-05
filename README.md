# 🚀 github-actions-test

这是一个最小的 GitHub Actions 示例仓库。✨

它演示了两件事：📌

- 提交代码到 GitHub 后，自动运行测试 ✅
- 在拉取请求(PR, Pull Request)更新时，自动再次运行测试 🔁

分支流程示例：🌿

- 在 `dev` 分支上修改内容 ✍️
- 提交并推送到 GitHub ⬆️
- 创建拉取请求(PR, Pull Request)合并到 `main` 🔀
- GitHub Actions 自动检查这次 PR 🤖

核心文件：🧩

- `app.py`：一个非常小的示例函数
- `test_app.py`：对应测试
- `.github/workflows/test.yml`：GitHub Actions 工作流(workflow)配置

作者：sammul
