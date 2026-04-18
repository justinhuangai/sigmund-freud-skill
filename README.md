**English** | [简体中文](./README.zh-CN.md)

# Sigmund Freud.skill

A skill for examining motive, ambivalence, possible defenses, repetition, and interpretation through a careful Freudian lens. It separates historical theory from modern hypotheses and clinical evidence.

[Examples](#examples) · [Installation](#installation) · [Routes](#routes) · [Sources](#sources) · [Maintenance](#maintenance) · [Credits](#credits-and-license)

Responses default to English. An explicit request for Chinese selects Simplified Chinese unless a different variant is specified. A conversation-wide language choice persists until changed; a request for one answer or artifact applies only there. Other explicitly requested languages are honored. A Chinese prompt or this README's language selector does not change the response language by itself.

## Examples

These are illustrative response outlines written for this project, not quotations, historical reconstructions, or clinical conclusions.

### Why do users ask for A but choose B?

Check price, usability, habit, and competing needs first. A motive lens may suggest that B avoids a feared cost or preserves something valued, but that remains a hypothesis to investigate through observable choices and voluntary questions.

### My manager keeps humiliating me. Am I projecting?

Begin with the manager's concrete behavior and its impact. A past association may affect a reaction, but it does not erase current mistreatment. Do not turn a complaint into a diagnosis or imply that the user caused the harm.

### I used the wrong name. Does that reveal my true desire?

A slip alone cannot establish a hidden desire. Consider attention, fatigue, word similarity, context, and chance. Personal associations can support reflection without proving the cause of the mistake.

### Why does a relationship pattern keep repeating?

Describe the sequence and its exceptions before proposing a cause. Earlier expectations are one possible influence alongside present choices and constraints. Never infer an unconscious wish to suffer or use repetition to blame a harmed person.

## Installation

```bash
npx skills add justinhuangai/sigmund-freud-skill
```

The Python maintenance tools are not required to use the skill. Ask for Sigmund Freud's perspective on a question or invoke `sigmund-freud-skill` explicitly. To select Chinese, say: `Please answer in Simplified Chinese for the rest of this conversation.`

## Routes

[SKILL.md](SKILL.md) defines language, evidence, and routing rules. Start with one operational reference and read research only as needed.

| Route | Purpose |
|---|---|
| [Motive and ambivalence](references/motive-excavation.md) | Competing wants and constraints |
| [Possible defensive patterns](references/defense-mechanism-detection.md) | Behavior before tentative interpretation |
| [Slips and everyday errors](references/symptom-and-slip-reading.md) | Ordinary explanations alongside associations |
| [Transference and repetition](references/transference-and-repetition.md) | Recurring sequences and their exceptions |
| [Modern application and limits](references/modern-transfer-and-boundaries.md) | Products, teams, and limits of analogy |

## Sources

There are **5 unique source records**: the long English text of Psychopathology of Everyday Life, a prefatory excerpt from The Interpretation of Dreams, a Gutenberg catalog for A General Introduction to Psychoanalysis, and partial Britannica and IEP articles. The Dreams chapters and IEP's detailed critical-evaluation section are absent. A catalog summary is not the book. The IEP record was formerly misleadingly named sep-freud.md; its filename now matches the actual source.

The [six research notes](references/research/README.md) are editorial guides with explicit evidence gaps, not a comprehensive literature review. Inspect the [source inventory](references/sources/README.md) before citing a work. Verify exact quotations, disputed historical claims, and current scientific assertions against appropriate sources.

## Boundaries

- Treat psychological interpretations as possibilities, not facts about another person's hidden motives.
- Consider ordinary explanations and actual mistreatment before an inward interpretation.
- Respect the user's goals, constraints, consent, and correction; disagreement does not prove a theory.
- Do not diagnose, provide treatment, infer recovered memories, or replace appropriate professional support.
- Do not use symbolism, historical prestige, or untestable explanations to pressure or manipulate people.

## Repository layout

- [SKILL.md](SKILL.md): concise runtime instructions; version remains `1.0.0`.
- [references/](references/): five operational routes and an extraction framework.
- [references/research/](references/research/README.md): six thematic notes.
- [references/sources/](references/sources/README.md): preserved source content and provenance.
- [scripts/](scripts/) and [tests/](tests/): maintenance utilities and regression tests.
- [README.zh-CN.md](README.zh-CN.md): Simplified Chinese overview.

## Maintenance

Run from the repository root with Python 3.10 or later:

```bash
python3 scripts/check_links.py .
python3 scripts/check_sources_inventory.py .
python3 scripts/check_research_repetition.py references/research
python3 -m unittest discover -s tests -v
```

Core checks and tests use the standard library. Optional HTML capture tests run when Beautiful Soup is installed. Web/PDF capture optionally requires the packages in `requirements.txt` (requests, Beautiful Soup, pypdf); install them with `python3 -m pip install -r requirements.txt` when needed.

`capture_web_source.py` requires `--language` for the actual source language (`en`, `zh-CN`, another tag, or `und` if unknown). It preserves source text rather than translating it. `srt_to_transcript.py` converts SRT/VTT files. Subtitle download requires optional `yt-dlp`, defaults to English, and tries manual before automatic tracks. `--language zh-CN` selects only explicitly labeled Simplified Chinese tracks; neither selection falls back to another language. CLI messages remain English.

```bash
bash scripts/download_subtitles.sh "VIDEO_URL" outputs/subtitles
bash scripts/download_subtitles.sh --language zh-CN "VIDEO_URL" outputs/subtitles
```

Checks validate links, metadata, repeated text, and script behavior; they do not prove historical truth, source completeness, rights clearance, or clinical efficacy. Keep both READMEs synchronized and use the [extraction framework](references/extraction-framework.md) when changing research.

## Credits and license

Maintained by Jackson Huang and assembled with [Nuwa.skill](https://github.com/alchaincyf/nuwa-skill). Thanks to Nuwa's authors and contributors for the tooling.

Original project content is available under the [MIT License](LICENSE). Third-party texts, translations, and catalog records retain their own rights and terms; their inclusion does not relicense them under MIT.
