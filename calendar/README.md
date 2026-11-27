# 黄历日历 · 在线更新源

这个仓库用作「黄历日历」App 的在线更新源，通过 GitHub Pages 提供更新包下载。

## 文件说明

| 文件 | 用途 |
|---|---|
| `index.html` | 日历页面本体（更新包） |
| `update.json` | 版本清单：版本号、版本码、更新说明、MD5 校验值 |
| `.nojekyll` | 空文件，确保 GitHub Pages 不跳过下划线开头的文件 |

## App 里要填的更新地址

开启 GitHub Pages 后，把下面这个地址填进 App 的「设置 → 软件更新 → 更新地址」：

```
https://你的用户名.github.io/仓库名/update.json
```

注意是 `update.json` 的完整网址，不是仓库首页。

## 以后怎么发新版

1. 把新的 `index.html` 覆盖上传到本仓库
2. 修改 `update.json`：
   - `code` 加 1（必须比上一个大，App 才会提示更新）
   - `version` 改成新版本号文字
   - `notes` 写更新说明（用 `\n` 换行）
   - `md5` 改成新 `index.html` 的 MD5（可用「更新包生成器.html」自动算）
3. 提交后等 1-2 分钟（GitHub Pages 刷新），用户打开 App 即会提示更新

`url` 字段留空即可，App 会自动下载同目录下的 `index.html`。
