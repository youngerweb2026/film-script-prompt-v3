# 影视脚本提示词3.0

把剧本、分镜、镜头想法和参考素材整理成 Seedance 2.5 中文视频提示词。每个生成段依次输出【素材绑定】【视觉风格锁定】【画面描述】【负面提示词】。

作者为不二何。 [GitHub 主页](https://github.com/youngerweb2026)

## 在 Codex 安装

把下面这段话复制到 Codex。

```text
请用 Skill Installer 安装「影视脚本提示词3.0」。仓库是 youngerweb2026/film-script-prompt-v3，Skill 目录是 skills/film-script-prompt-v3。请完整安装该目录，核对 SKILL.md、agents/openai.yaml 和 references 中的三个文件，并告诉我安装位置。
```

也可以在终端运行。

```bash
python3 "${CODEX_HOME:-$HOME/.codex}/skills/.system/skill-installer/scripts/install-skill-from-github.py" \
  --repo youngerweb2026/film-script-prompt-v3 \
  --path skills/film-script-prompt-v3
```

安装后在 Codex 中用 `$film-script-prompt-v3` 调用。

## 3.0 的写法

- **按内容标时间**。单条连续动作默认按顺序写成自然段。切镜时可标切换点或各镜时长。对白、音乐节拍、画面文字、参考视频对齐、局部编辑，以及符合时长和阶段条件的复杂动作，按需用时间区间或事件点。
- **逐个检查说话角色的音色**。有参考就在【素材绑定】明确角色和素材的对应关系。缺少参考就在【画面描述】暂用文字设定。同一角色在各镜头和生成段沿用同一音色。
- **可独立提交每个生成段**。按叙事安排时长、动作和接戏。新建内容默认无背景音乐，可保留环境声和动作音效。

[Skill 主文](skills/film-script-prompt-v3/SKILL.md) · [任务写法](skills/film-script-prompt-v3/references/task-patterns.md) · [完整示例](skills/film-script-prompt-v3/references/examples.md) · [模型资料与能力边界](skills/film-script-prompt-v3/references/model-notes.md)
