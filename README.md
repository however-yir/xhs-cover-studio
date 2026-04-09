# xhs-cover-studio

A Codex skill for generating Xiaohongshu (小红书) cover HTML/PNG files from 58 DESIGN.md-inspired brand templates, with support for long-copy multi-variant output (up to 3 covers in one run).

## What This Skill Does

This skill helps you go from idea or copy to publish-ready cover images quickly. It keeps the selected brand style intact, lets you edit content fields, and exports deterministic `1500x2000` PNG files through local scripts.

## Best For

- 小红书图文封面制作
- DESIGN.md 风格封面复刻
- 一键 HTML + PNG 导出
- 长文案拆分为多版本封面
- A/B 封面对比（最多 3 张）
- 快速替换标题、副标题、卖点卡片

## Inputs

Typical inputs:

- style name (for example `apple`, `notion`, `linear`)
- topic or core message
- headline and subheadline copy
- optional feature-card copy and tags
- optional long-form copy for multi-variant generation
- output directory and filename prefix

## Outputs

Typical outputs:

- one or more editable HTML files
- matching PNG files in `1500x2000` resolution
- consistent style across generated variants
- absolute output paths for immediate use

## Non-goals

This skill is not aimed at:

- generating brand-new visual systems from scratch
- heavy layout redesign across template CSS
- social strategy or post body writing itself
- monthly content planning workflows

## Example Prompts

- `用 apple 风格做一张“AI 工具推荐”小红书封面，直接导出 PNG。`
- `这段长文案帮我拆成 3 张不同角度的封面，保持 notion 风格。`
- `给我一套 linear 风格封面，标题更偏求职项目包装。`
- `先列出可用风格，然后用 figma 风格生成一版。`

## Repository Structure

```text
.
├── README.md
├── SKILL.md
├── agents/
│   └── openai.yaml
├── assets/
│   └── covers/
│       └── <58 style folders>
├── examples/
│   └── showcase.md
├── references/
│   └── style-catalog.md
└── scripts/
    ├── build_cover.py
    └── capture.sh
```

## Showcase Examples

See [examples/showcase.md](./examples/showcase.md) for practical one-cover and three-cover generation examples.

## Included Files

- [SKILL.md](./SKILL.md): trigger logic, workflow, and command patterns
- [scripts/build_cover.py](./scripts/build_cover.py): core generator for single/multi cover output
- [scripts/capture.sh](./scripts/capture.sh): Chrome headless screenshot helper
- [references/style-catalog.md](./references/style-catalog.md): style list reference
- [examples/showcase.md](./examples/showcase.md): ready-to-run command examples
- [LICENSE](./LICENSE): MIT license

## Pair Well With

- `xiaohongshu-content-studio`
- `copywriting`
- `content-humanizer`
- `generate-image`
- `frontend-design`

## License

Released under the MIT License. See [LICENSE](./LICENSE).

## Notes

Use `--copy-text --auto-variants 3` when your copy is long and you want quick A/B/C cover options in one command.
