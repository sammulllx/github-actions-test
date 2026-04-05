# Git / GitHub Actions 最小备忘单

## 最小流程

1. 从 `main` 切出开发分支

```bash
git checkout main
git pull
git checkout -b dev
```

2. 在 `dev` 上改代码

3. 本地先检查

```bash
python3 -m pytest -q
```

4. 提交并推送到远程 `dev`

```bash
git add .
git commit -m "你的改动说明"
git push -u origin dev
```

5. 去 GitHub 网页创建 PR

- `base: main`
- `compare: dev`

6. 等 GitHub Actions 跑完

- 绿勾：可以 merge
- 红叉：先修再 push

7. 在网页上点 `Merge pull request`

8. 可选：删掉 `dev`

- 网页点 `Delete branch`

## 关键概念

- `git commit`：本地记录
- `git push`：把本地改动送到远程分支
- PR：请求把 `dev` 合进 `main`
- `Merge pull request`：把 PR 的改动真正合进 `main`
- GitHub Actions：自动检查员

## 常见误区

- `push` 到 `dev` 不等于进了 `main`
- 网页上看到的内容取决于当前选中的分支，不一定是 `main`
- `behind main` 不一定表示文件内容不同，有时只是提交历史不同

## 一句总结

在 `dev` 开发，`push` 到远程，创建 `dev -> main` 的 PR，等 GitHub Actions 通过后再 merge。
