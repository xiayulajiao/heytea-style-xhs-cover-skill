# 喜茶风小红书封面 skill

面向 AI、FDE 与效率主题的封面风格 Skill。视觉基准为用户最终认可的记号笔手写封面。

![已确认风格](assets/approved-cover.png)

## 风格

- 白底和自然留白，默认竖版 3:4。
- 文字占主要视觉，插图较小。
- 拙朴、略歪、不齐的中等粗细记号笔字，避免书法笔锋与厚重刷漆字。
- 黑字与蓝色重点，配少量细线稿。

底色和个人 logo 仍处于讨论阶段，尚未纳入已确认的默认风格。

## 下载

仓库：https://github.com/xiayulajiao/heytea-style-xhs-cover-skill

下载全部文件后，把仓库目录命名为 `xhs-marker-cover`，安装到实际执行任务的 Agent 所支持的 Skills 目录。也可以通过下面的命令下载到一个全新的本地目录：

```bash
git clone https://github.com/xiayulajiao/heytea-style-xhs-cover-skill.git xhs-marker-cover
```

不要只下载 `SKILL.md`；必须保留 `assets/approved-cover.png` 及其相对路径。

## 让 Grokbot 调用

将下面的指令交给实际执行封面任务的 Grokbot：

```text
请下载 https://github.com/xiayulajiao/heytea-style-xhs-cover-skill 的完整内容，并将它安装为 xhs-marker-cover Skill。
先检查当前 Grokbot 的实际 Skills 加载方式，安装到执行封面任务的 Agent 能读取的位置。

每次调用时，读取 SKILL.md，并实际查看 assets/approved-cover.png。
将这张图作为视觉风格参考传给支持参考图输入的生图工具，替换为本期标题和辅助插图。
保留白底留白、拙朴记号笔字、蓝色重点、文字为主和小插图的关系。
逐字核对成品文字，实际查看结果后交付。

如果当前系统没有自动加载 Skills 的能力，则显式读取 SKILL.md 及对应参考图后执行。
如果缺少生图能力或图片输入能力，准确报告缺口；先提供可用提示词，不把提示词当成生成完成的图片。

完成安装后报告实际路径、所用仓库提交版本，以及是否成功加载了规则和参考图。
```

调用示例：

```text
用 xhs-marker-cover 制作小红书封面。
标题：用 AI 做业务，第一步该改哪里？
重点词：第一步
插图：小人连接业务流程与工具。
```

## 文件

- `SKILL.md`：可供 Agent 加载的核心规则与提示词骨架。
- `assets/approved-cover.png`：用户认可的完整参考图。
- `agents/openai.yaml`：Codex 展示元数据；其他 Agent 可忽略。
- `manifest.json`：文件校验信息。

这是一套规则和参考素材，需要使用方提供实际可用的生图工具。仓库不包含 API 密钥，也不会自动接通任何模型服务。

仓库名称描述视觉参考方向，与喜茶品牌无隶属关系。示例图中的标题和金额用于说明版式，不是后续文案的固定内容。
