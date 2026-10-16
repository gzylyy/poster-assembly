# GitHub 发布指南

这份目录是可单独上传的仓库内容。技能的本机审查记录、历史备份和临时验证依赖不属于该目录。

## 仓库信息

- 名称建议：`poster-assembly`。
- 作者：Fishking。
- 许可证：MIT，已写入仓库根目录及可独立分发的技能文件夹。
- 版本：`0.1.0`，首次公开发布前准备的版本号。
- 英文介绍可填：`A practical skill for poster planning, independent visual assets, editable typography, and production handoff.`
- Topics 可选：`agent-skills`、`codex`、`poster-design`、`design-workflow`、`typography`。

## 上传仓库

1. 在 GitHub 创建公开仓库，使用上述名称或你自己的名称。
2. 上传本目录的内容，让 `README.md`、`LICENSE`、`plugin.json` 和 `skills/` 直接位于仓库根目录。
3. 检查中英文说明切换、示例预览、技能参考链接和文件树。
4. README 已包含安装方式，不需要填一个尚不存在的仓库 URL；仓库创建后可以再加自己的真实链接。

完整源码包解压后有一层 `poster-assembly` 外层目录；上传的是这一层里面的文件。不要把整个本机工作目录或只有一个 ZIP 文件的空仓库作为源码发布。

## 创建首个 Release

建议标签与标题：`v0.1.0`、`Poster Assembly v0.1.0`。这是待发布资料，不表示 GitHub 上已经存在该标签或 Release。

发布说明可使用：

```text
Initial public release of Poster Assembly.

- Staged workflow for poster planning, independent assets, and editable layout.
- Screen and print resolution guidance, cropping checks, and delivery templates.
- Practical guidance for series consistency, compositing, typography, and QR checks.
- English and Simplified Chinese READMEs; Chinese authoritative skill instructions.
- Original SVG example showing layout, separate artwork, and final typography.
- MIT License. Maintained by Fishking.
```

将单独的 `poster-assembly-v0.1.0.zip` 作为技能下载附件。它的顶层目录为 `poster-assembly`，包含完整技能、参考文件、界面元数据和许可证。完整仓库包则用于源码移交或首次上传，二者用途不同。

GitHub 的 Release 用于按版本分发附件，参见 [GitHub 官方说明](https://docs.github.com/en/repositories/releasing-projects-on-github/about-releases)。本仓库提供便携式插件清单，但未包含插件市场目录或完成市场上架；需要市场分发时按对应宿主流程另行配置。

## 维护后续版本

先修改 `skills/poster-assembly` 中的权威文件，再同步受影响的示例和中英文首页。更新技能元数据及 `plugin.json` 中的版本号，复查链接、数值示例、构图确认与授权复用行为，再生成新下载包。
