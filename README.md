## 这个项目是什么

这是一个基于 [**magic-akari/lrc-maker**](https://github.com/magic-akari/lrc-maker) 项目的分支

## 跟原仓库有什么差别

我觉得一些热键的调整跨度有点太长了，对它们进行了修改：

| 按键                        | 功能                     | 原跨度 |
| --------------------------- | ----------------------- | ------ |
| <kbd>←</kbd> / <kbd>a</kbd> | 播放进度回退 3 秒        | 5 秒   |
| <kbd>→</kbd> / <kbd>d</kbd> | 播放进度前进 3 秒        | 5 秒   |
| <kbd>-</kbd> / <kbd>+</kbd> | 当前行时间标签微调 0.1 秒 | 0.5 秒 |

## 想再调整参数？

目前原仓库还没有可以在网页直接更改这部分参数的功能，若您想自定义，请参考下方的修改方式：

| 功能 | 配置文件位置 | 修改参考 |
| -------------------- | ---------------- | ---------------- |
| 播放进度调整跨度 | [**src/components/footer.tsx#L71-L78**](https://github.com/Interstellar750/lrc-maker/blob/master/src/components/footer.tsx#L71-L78) | [**FEBE472**](https://github.com/Interstellar750/lrc-maker/commit/ea40d5c8f218be22c484c36bdda69f5b99c66d2a#diff-febe472312c34362d6340a54dd876572b5ef8731d37a0d895c9b6b1f2ead8a8e) |
| 时间标签微调跨度 | [**src/components/synchronizer.tsx#L135-L145**](https://github.com/Interstellar750/lrc-maker/blob/master/src/components/synchronizer.tsx#L135-L145) | [**C7498EC**](https://github.com/Interstellar750/lrc-maker/commit/ea40d5c8f218be22c484c36bdda69f5b99c66d2a#diff-c7498ecf24d1df92d5ed2b7f5211b82283db2118770b092ae4ed5def85ee4dd3) |

## 部署修改后的项目

修改完成后，您可以按照原项目的 [**本地开发**](https://github.com/magic-akari/lrc-maker/blob/master/README.md#本地开发) 章节来在本地运行

也可以导入到 Vercel 进行部署，以下是对应的部署命令：

| 构建命令 | 输出目录 | 安装命令 |
| --------------------------- | ----------------------- | ------ |
| `npm run build` | `build` | `yum install rsync -y && npm i` |
