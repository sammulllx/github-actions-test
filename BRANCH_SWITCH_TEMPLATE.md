# 切分支超短操作模板

## 切到 `main` 时

适合场景：准备在主分支上查看最新内容，或从 `main` 新开分支。

```bash
git checkout main
git fetch origin
git pull --rebase
```

## 切到 `dev` 时

适合场景：准备继续开发已有的 `dev` 分支。

```bash
git checkout dev
git fetch origin
git pull --rebase
```

## 如果只是“看看”

只想切过去看文件，不马上开发，可以先不 `pull`：

```bash
git checkout main
```

或：

```bash
git checkout dev
```

## 最小心法

- 想先看看远端有没有变化：`git fetch origin`
- 想让当前分支跟上远端：`git pull --rebase`
- 准备正式开发前：先同步，再改代码

## 一句总结

切到要继续工作的分支后，通常先 `fetch`，再 `pull --rebase`。
