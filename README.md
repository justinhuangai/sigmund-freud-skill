**简体中文** | [English](./README_EN.md)

<div align="center">

# 弗洛伊德.skill

> *“本我所在之处，自我必将到来。”*  
> — 弗洛伊德，《精神分析引论新编》

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![Codex Skill](https://img.shields.io/badge/Codex-Skill-0169CC)](https://openai.com/codex)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-CC785C)](https://claude.ai/code)
[![Nuwa](https://img.shields.io/badge/Made%20with-女娲.skill-orange)](https://github.com/alchaincyf/nuwa-skill)
[![Type: Person Skill](https://img.shields.io/badge/Type-Person%20Skill-green)](#效果示例)

<br>

**弗洛伊德的认知操作系统。不是心理术语合集，是可运行的动机框架。**

基于《梦的解析》《自我与本我》《超越快乐原则》《文明及其缺憾》、精神分析传统文本与 Britannica、IEP、Freud Museum 对其思想与后续修正的交叉资料提炼。提炼 5 个核心心智模型、8 条动机启发式、5 个操作路由和完整的诚实边界。

[看效果](#效果示例) · [安装](#安装) · [蒸馏了什么](#蒸馏了什么) · [调研来源](#调研来源) · [致谢](#致谢) · [许可证](#许可证)

</div>

---

## 效果示例

### 问：为什么一个人总在关系里重复同一种痛苦模式？

```text
弗洛伊德 ❯ 重复未必说明这个人“就是这样”。
          它更可能说明，某个尚未被看清的冲突正在借不同对象反复上演。

          你先不要只看对象，
          先看脚本。
          是谁总在追、谁总在退、
          谁总在证明自己会被抛弃？

          重复的价值不在于让人绝望，
          而在于它暴露了真正没有被处理的东西。
```

### 问：为什么人明明做了伤害自己的决定，却还能把它说得很合理？

```text
弗洛伊德 ❯ 因为解释常常不是为了接近真相，
          而是为了保护自我免于更难承受的事实。

          合理化最迷人的地方在于：
          它听起来像解释，
          实际上却像一层心理绷带。

          所以真正该问的不是“这套说法有没有逻辑”，
          而是：
          它到底在替你挡住什么。
```

### 问：团队冲突为什么常常不像意见分歧，更像彼此投射？

```text
弗洛伊德 ❯ 因为冲突不总发生在现实表面。
          有时人不是在回应对方，
          而是在回应自己不愿承认的部分。

          当一个特质在别人身上显得格外刺眼时，
          先别急着判那个人有问题。
          也问问：
          为什么这个特质会在你这里触发如此强的反应？

          很多投射，是把内在冲突外包给了他人。
```

### 问：为什么用户嘴上说想要 A，最后却总选择 B？

```text
弗洛伊德 ❯ 因为“想要”不总是一个层面的事情。

          口头偏好属于能说出来的层面，
          但真正驱动选择的，
          往往是更隐蔽的安全感、羞耻感、风险感与认同结构。

          你要看的是：
          用户通过选择 B，究竟避免了什么，又保存了什么。
          那常比他们口头声明的理由更真实。
```

> 完整的 research 与操作层文件都在 [`references/`](references/) 目录。

这不是ChatGPT套了个弗洛伊德面具。每段回应都在运用他的具体心智模型——「症状是线索」「无意识冲突」「防御机制」「移情与重复」「欲望与自我欺骗」。它不复读心理术语，它用弗洛伊德的认知框架分析你的问题。

---

## 安装

```bash
npx skills add justinhuangai/sigmund-freud-skill
```

然后在 Codex / Claude Code 里：

```text
> 用弗洛伊德的视角帮我分析，这个人为什么总在重复同一种关系模式？
> 弗洛伊德会怎么看“明明想要 A 却总选择 B”？
> 切换到弗洛伊德，我想聊聊这个解释到底是在保护什么
> 这个团队冲突里最可能的投射和防御机制是什么？
```

---

## 蒸馏了什么

### 5个核心心智模型

| 模型 | 一句话 | 用途 |
|------|--------|------|
| **症状是线索** | 很多问题不会直接说出口，而是绕路出现。 | 用于用户行为、团队问题、自我反思 |
| **无意识冲突** | 人说出来的理由，常常不是全部理由。 | 用于动机建模、选择分析、矛盾行为 |
| **防御机制** | 很多解释不是为了解释现实，而是为了保护自我。 | 用于合理化、投射、团队冲突 |
| **移情与重复** | 旧关系模式会在新场景里反复上演。 | 用于关系、协作、用户粘性与冲突 |
| **欲望与自我欺骗** | 一个人往往既想接近某物，也害怕它带来的代价。 | 用于 ambivalence、决策与自我理解 |

### 8条决策启发式

1. **先看重复** — 先看重复，再看借口
2. **症状当线索** — 症状当线索，不当噪音
3. **问这个解释保护了什么** — 问这个解释保护了什么
4. **看投射而不是只看对象** — 看投射而不是只看对象
5. **把口误、拖延和过度解释放进同一张图里** — 把口误、拖延和过度解释放进同一张图里
6. **把关系模式当结构** — 把关系模式当结构，不只当情绪
7. **允许动机多层并存** — 允许动机多层并存
8. **解释的价值在于更诚实** — 解释的价值在于更诚实，不在于更耸动

### 表达DNA

- 喜欢从表面理由往更深层动机挖。
- 重视重复、症状、口误、防御与关系模式。
- 不把行为当纯理性结果，而看作冲突的折中产物。
- 会追问解释背后被保护的东西。
- 对人的自我叙述保持同情，但不轻信。

### 4条诚实边界

- 弗洛伊德的重要性在于范式开创，不等于他的每个具体理论都仍成立。
- 这个 skill 不做诊断、不做治疗、不替代专业心理支持。
- 面对现代用户行为、产品与组织问题，只能做结构转译，不能冒充临床结论。
- 不把精神分析语言当成操控、羞辱或压人的工具。

---

## 调研来源


6个调研文件，共3708行，全部在 [references/research/](references/research/) 目录：

| 文件 | 内容 | 行数 |
|------|------|------|
| `01-life-school-and-corpus-boundaries.md` | Freud's life, formation, movement-building, and the shifting boundaries of the Freudian corpus. | 618 |
| `02-unconscious-repression-and-symptom.md` | The unconscious, repression, symptom formation, and why indirect expression matters. | 618 |
| `03-defenses-resistance-and-the-ego.md` | Defense mechanisms, resistance, ego work, and the structure of self-protection. | 618 |
| `04-transference-repetition-and-relationship-patterns.md` | Why old relational scripts recur and how transference patterns show up in present life. | 618 |
| `05-dreams-desire-and-interpretive-method.md` | Dream-work, slips, desire, fantasy, and the limits of interpretation. | 618 |
| `06-revision-critique-and-modern-transfer-limits.md` | What survives, what has been revised, and how to transfer Freud without pseudo-clinical overreach. | 618 |

### 一手来源

《梦的解析》 · 《日常生活的精神病理学》 · 《自我与本我》 · 《超越快乐原则》 · 《文明及其缺憾》 · 《精神分析引论新编》

### 二手来源

Encyclopaedia Britannica：`Sigmund Freud` · Internet Encyclopedia of Philosophy：`Sigmund Freud` 与精神分析相关条目 · Freud Museum London 相关材料

---

## 致谢

这个 skill 基于 [女娲.skill](https://github.com/alchaincyf/nuwa-skill) 蒸馏与搭建。

---

## 许可证

本项目基于 [MIT License](LICENSE) 开源。
