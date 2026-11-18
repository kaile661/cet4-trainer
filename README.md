# cet4-trainer

四级 / 初中英语单词训练程序（三阶段 + 间隔重复 + 遗忘曲线）。

这个仓库同时充当**远程更新的发布源**：

- `e4/` —— 发布包。手机 App 里「设置 → 远程更新 → 服务器地址」填
  `https://<用户名>.github.io/<仓库名>/e4/`，App 就会从这里检查新版本、
  下载新的题库 / 例句 / 程序本身（每个文件都带 sha256 校验）。

`e4/` 里有什么：

| 文件 | 说明 |
|---|---|
| `version.json` | 版本清单（程序版本、内容版本、每份数据的地址与 sha256） |
| `app.html` | 主程序（界面 + 词库 + 例句全内联，约 2.3 MB） |
| `data/words.json` | 四级词库 2000 词 |
| `data/sentences.json` | 四级例句 5522 句 |
| `data/junior_words.json` | 初中词库 2329 词 |
| `data/junior_sentences.json` | 初中例句 4604 句 |
| `apk/app-release.apk` | 安卓安装包 |

发布新版本：在本地跑 `node publish.js` 生成发布包，再整体覆盖 `e4/` 即可。
