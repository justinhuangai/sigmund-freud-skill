[English](./README.md) | **简体中文**

# 弗洛伊德.skill

用审慎的弗洛伊德视角探索动机、矛盾愿望、可能的防御、重复模式与解释方法。明确区分历史理论、现代假设和临床证据。

[示例](#示例) · [安装](#安装) · [操作路由](#操作路由) · [来源](#来源) · [维护](#维护) · [致谢](#致谢与许可)

回答默认使用英文。明确请求中文时使用简体中文，除非指定其他变体。面向整个对话的语言选择持续生效，直到再次修改；仅针对一次回答或一个产物的要求只在该范围内生效，也尊重其他明确指定的语言。中文提问或切换本说明文档本身，不会改变回答语言。

## 示例

以下是本项目编写的示例回答提纲，不是历史人物原话、历史重演或临床结论。

### 为什么用户说想要 A，却选择 B？

先检查价格、可用性、习惯与相互竞争的需要。动机视角也许提示 B 避开了某种担忧或保留了重要价值，但这只是需要通过可观察选择与自愿回答的问题来检验的假设。

### 经理不断羞辱我，这是我的投射吗？

先看经理的具体行为及其影响。过去的联想可能影响反应，但不会抹去现在的伤害。不能把投诉变成诊断，也不能暗示伤害由当事人造成。

### 我叫错了名字，是否暴露了真实欲望？

一次口误不能确立隐藏欲望。应考虑注意力、疲劳、词语相似性、情境与偶然性。个人联想可以帮助反思，但不能证明错误的成因。

### 为什么关系里总在重复同一种模式？

先描述过程和例外，再提出原因。过去形成的期待只是可能影响之一，也要考虑当下的选择与限制。不能推断当事人潜意识里想受苦，更不能用重复模式责怪受到伤害的人。

## 安装

```bash
npx skills add justinhuangai/sigmund-freud-skill
```

使用 Skill 不需要 Python 维护工具。可以请求以弗洛伊德的视角分析问题，或显式调用 `sigmund-freud-skill`。如需切换中文，可明确说：“本次对话接下来请使用简体中文回答。”

## 操作路由

[SKILL.md](SKILL.md) 定义语言、证据与路由规则。先读取一个相关操作参考，按需补充研究材料。

| 路由 | 用途 |
|---|---|
| [动机与矛盾愿望](references/motive-excavation.md) | 相互竞争的愿望与限制 |
| [可能的防御模式](references/defense-mechanism-detection.md) | 先描述行为，再提出暂定解释 |
| [口误与日常错误](references/symptom-and-slip-reading.md) | 同时考虑普通原因和个人联想 |
| [移情与重复](references/transference-and-repetition.md) | 反复出现的过程及其例外 |
| [现代应用与边界](references/modern-transfer-and-boundaries.md) | 产品、团队与类比的限度 |

## 来源

目前有 **5 条独立来源记录**：英文《日常生活的精神病理学》长篇文本、《梦的解析》的前言节选、《精神分析引论》的古登堡目录，以及不完整的大英百科和 IEP 文章。《梦的解析》的主体章节、IEP 的详细批评分析部分均未收录。目录摘要不是书籍正文。IEP 记录此前误用 sep-freud.md 文件名，现已按实际来源更名。

[六份研究笔记](references/research/README.md) 是明确标记证据缺口的编辑性指南，不是完整文献综述。引用著作前请查看[来源清单](references/sources/README.md)。精确引文、有争议的历史论断及当前科学结论需要核对恰当来源。

## 边界

- 心理解释是可能性，不是他人隐秘动机的事实。
- 先考虑普通解释与实际伤害，再考虑内在心理解释。
- 尊重用户的目标、限制、自主选择及纠正；不同意不构成理论正确的证据。
- 不作诊断、不提供治疗、不推断所谓恢复的记忆，也不替代适当的专业支持。
- 不借助象征、历史权威或不可检验的解释向人施压或进行操控。

## 仓库结构

- [SKILL.md](SKILL.md)：精简的运行指令；版本保留为 `1.0.0`。
- [references/](references/)：五条操作路由和提炼框架。
- [references/research/](references/research/README.md)：六份主题研究笔记。
- [references/sources/](references/sources/README.md)：保存的来源内容与溯源信息。
- [scripts/](scripts/) 和 [tests/](tests/)：维护工具与回归测试。
- [README.md](README.md)：英文说明。

## 维护

在仓库根目录使用 Python 3.10 或更新版本运行：

```bash
python3 scripts/check_links.py .
python3 scripts/check_sources_inventory.py .
python3 scripts/check_research_repetition.py references/research
python3 -m unittest discover -s tests -v
```

核心检查与测试只依赖标准库。安装 Beautiful Soup 后，还会运行可选的 HTML 采集测试。网页/PDF 采集按需使用 `requirements.txt` 中的 requests、Beautiful Soup、pypdf，可通过 `python3 -m pip install -r requirements.txt` 安装。

`capture_web_source.py` 必须通过 `--language` 指定原文实际语言（`en`、`zh-CN`、其他语言标签，或不确定时用 `und`），保留原文而不翻译。`srt_to_transcript.py` 转换 SRT/VTT 文件。字幕下载需要可选的 `yt-dlp`，默认英文，先人工字幕再自动字幕。`--language zh-CN` 只选择明确标注的简体中文字幕；两种模式都不会回退到其他语言。命令行提示保持英文。

```bash
bash scripts/download_subtitles.sh "VIDEO_URL" outputs/subtitles
bash scripts/download_subtitles.sh --language zh-CN "VIDEO_URL" outputs/subtitles
```

检查涵盖链接、元数据、重复文本与脚本行为，不证明历史论断、来源完整性、版权许可或临床有效性。修改时同步两份 README，并遵循[提炼框架](references/extraction-framework.md)。

## 致谢与许可

本项目由 Jackson Huang 维护，使用 [Nuwa.skill](https://github.com/alchaincyf/nuwa-skill) 辅助构建。感谢 Nuwa 作者与贡献者提供工具。

项目原创内容使用 [MIT 许可证](LICENSE)。第三方原文、译文与目录记录保留各自的权利与条款，收录到仓库不表示改为 MIT 授权。
