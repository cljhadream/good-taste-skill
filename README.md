<div align="center">

# Good Tast Skill

<em>Premium frontend Agent Skills, rebuilt with Chinese aesthetics.<br />高端前端 Agent Skills，融入中国审美的全新演绎。</em>

**[English](#english) · [中文](#中文)**

<p>
  <a href="LICENSE"><img src="https://img.shields.io/badge/license-MIT-24292f?style=flat&amp;logo=github&amp;logoColor=white" alt="MIT License" /></a>
  &nbsp;
  <a href="https://github.com/vercel-labs/agent-skills"><img src="https://img.shields.io/badge/Agent_Skills-compatible-24292f?style=flat&amp;logo=github&amp;logoColor=white" alt="Agent Skills compatible" /></a>
  &nbsp;
  <a href="#installing"><img src="https://img.shields.io/badge/Codex_%2F_Cursor_%2F_Claude-install-24292f?style=flat" alt="Codex, Cursor, Claude" /></a>
</p>

</div>

## Maintained by Gutast AI · 由 Gutast AI 维护

<table align="center">
  <tr>
    <td align="center" width="104" rowspan="2"><a href="https://www.gutast.com/?utm_source=github&amp;utm_medium=social&amp;utm_campaign=good_tast_skill"><img src="https://www.gutast.com/UI/logo/300_300.webp" alt="Gutast AI" width="52" height="52" /></a></td>
    <td><sub><b>EN</b> · <a href="https://www.gutast.com/?utm_source=github&amp;utm_medium=social&amp;utm_campaign=good_tast_skill"><strong>Gutast AI</strong></a> · <a href="https://www.gutast.com/claude-code?utm_source=github&amp;utm_medium=social&amp;utm_campaign=good_tast_skill">Claude Code direct-connect plans</a> (official client, Organization ID only) and <a href="https://www.gutast.com/chatgpt-plus?utm_source=github&amp;utm_medium=social&amp;utm_campaign=good_tast_skill">ChatGPT Plus / Codex official-channel recharge</a> — zero passwords, invoices included, active in minutes.</sub></td>
  </tr>
  <tr>
    <td><sub><b>中文</b> · <a href="https://www.gutast.com/?utm_source=github&amp;utm_medium=social&amp;utm_campaign=good_tast_skill"><strong>Gutast AI</strong></a> 提供 <a href="https://www.gutast.com/claude-code?utm_source=github&amp;utm_medium=social&amp;utm_campaign=good_tast_skill">Claude Code 终端直连套餐</a>（官方客户端、仅需 Organization ID）与 <a href="https://www.gutast.com/chatgpt-plus?utm_source=github&amp;utm_medium=social&amp;utm_campaign=good_tast_skill">ChatGPT Plus / Codex 官方渠道充值</a>——零密码、可开发票、几分钟开通。</sub></td>
  </tr>
</table>

---

<a id="english"></a>
## English

**Good Tast Skill** is an independent product built on the excellent open-source [Taste Skill](https://github.com/Leonxlnx/taste-skill) by [Leonxlnx](https://github.com/Leonxlnx). We keep the anti-slop engineering discipline of the upstream project and fold **Chinese aesthetics** into every skill's design rules: generous whitespace, editorial Chinese typography, asymmetric-but-balanced composition, and restrained premium palettes inspired by contemporary Chinese product design.

Portable **Agent Skills** that upgrade AI-built interfaces: stronger layout, typography, motion, and spacing instead of boilerplate-looking UIs. This repo also includes **image-generation skills** for reference boards (web, mobile, brand kits). Pair them with **ChatGPT Images** or similar generators, then hand the frames to Codex, Cursor, or Claude Code for implementation.

### Installing

The [`npx skills add`](https://github.com/vercel-labs/agent-skills) CLI scans the `skills/` folder in this repo, so **all skills below (code and image-generation) install the same way.**

```bash
npx skills add https://github.com/cljhadream/good-taste-skill
```

Install a single skill by its **install name** (the `name:` field inside the SKILL frontmatter, not the folder name):

```bash
npx skills add https://github.com/cljhadream/good-taste-skill --skill "design-taste-frontend"
```

You can also copy any `SKILL.md` into your project or paste it into ChatGPT / Codex conversations.

#### Install as a Claude Code plugin

If you only use Claude Code, you can install the whole repo as a plugin. Every skill is namespaced under `good-tast-skill:` (for example, `/good-tast-skill:imagegen-frontend-web`), so they won't collide with your other skills — no `npx skills` step required.

Run these inside Claude Code:

```
/plugin marketplace add cljhadream/good-taste-skill
/plugin install good-tast-skill@good-taste-skill
```

Run `/plugin update` later to upgrade installed plugins to new versions.

### Skills

Each skill does one job; you do not need all of them at once. **Implementation skills** output code. **Image-generation skills** output reference images only.

The `Install name` column is the exact value you pass to `--skill`.

| Skill (folder) | Install name | Description |
| --- | --- | --- |
| **[taste-skill](skills/taste-skill/SKILL.md)** | `design-taste-frontend` | 🆕 **v2 (experimental)** — the default skill. Reads the brief, infers the design language, tunes three dials (VARIANCE / MOTION / DENSITY), with Chinese-aesthetics composition rules on top. |
| **[taste-skill-v1](skills/taste-skill-v1/SKILL.md)** | `design-taste-frontend-v1` | The original v1, preserved for projects depending on its exact behavior. |
| **[gpt-tasteskill](skills/gpt-tasteskill/SKILL.md)** | `gpt-taste` | Stricter variant for GPT/Codex: higher layout variance, stronger GSAP direction, aggressive anti-slop. |
| **[image-to-code-skill](skills/image-to-code-skill/SKILL.md)** | `image-to-code` | Image-first pipeline: generate site references, analyze them, then implement the frontend to match. |
| **[redesign-skill](skills/redesign-skill/SKILL.md)** | `redesign-existing-projects` | Existing projects: audit the UI first, then fix layout, spacing, hierarchy, styling. |
| **[soft-skill](skills/soft-skill/SKILL.md)** | `high-end-visual-design` | Polished, calm, expensive UI with softer contrast, whitespace, premium fonts, spring motion. |
| **[output-skill](skills/output-skill/SKILL.md)** | `full-output-enforcement` | When the model ships half-finished work: full output, no placeholder comments. |
| **[minimalist-skill](skills/minimalist-skill/SKILL.md)** | `minimalist-ui` | Editorial product UI (Notion/Linear vibes), restrained palette, crisp structure. |
| **[brutalist-skill](skills/brutalist-skill/SKILL.md)** | `industrial-brutalist-ui` | Hard mechanical language: Swiss type, sharp contrast, experimental layout. |
| **[stitch-skill](skills/stitch-skill/SKILL.md)** | `stitch-design-taste` | Google Stitch-compatible rules, including optional `DESIGN.md` export format. |

### Image generation skills

These produce design images only (no code). Use with ChatGPT Images, Codex image mode, or any agent that generates images.

| Skill (folder) | Install name | Description |
| --- | --- | --- |
| **[imagegen-frontend-web](skills/imagegen-frontend-web/SKILL.md)** | `imagegen-frontend-web` | Website comps: hero, landing, multi-section with strong typography, spacing, anti-slop art direction. |
| **[imagegen-frontend-mobile](skills/imagegen-frontend-mobile/SKILL.md)** | `imagegen-frontend-mobile` | Mobile screens and flows: iOS/Android/cross-platform, mockups, readable type, coherent sets. |
| **[brandkit](skills/brandkit/SKILL.md)** | `brandkit` | Brand-kit boards: logo directions, palettes, type, identity applications across categories. |

### Which one should I use?

- Start with **taste-skill** for the safest general default.
- If you depend on the exact behavior of the original taste-skill, install **taste-skill-v1** instead.
- Use **gpt-taste** when you want the stricter GPT/Codex-oriented rules and motion/layout enforcement.
- Use **image-to-code-skill** for image → analyze → code website workflows.
- Use **redesign-skill** to improve an existing codebase instead of greenfield styling.
- Add **soft-skill**, **minimalist-skill**, or **brutalist-skill** when the visual direction is already chosen.
- Add **output-skill** if the agent keeps truncating output.
- Use **imagegen-frontend-web**, **imagegen-frontend-mobile**, or **brandkit** when the deliverable is **images** (comps, flows, identity boards), then pass results to your coding agent.

### Image-first tip

For **image-to-code-skill**, state the pipeline in the prompt, e.g.: `follow the skill: generate images, then analyze, then code`.

### Settings (taste-skill only)

Numbers at the top of the file are 1-10 dials:

- **DESIGN_VARIANCE**: Layout experimentation (lower: centered/clean · higher: asymmetric/modern).
- **MOTION_INTENSITY**: Animation depth (lower: hover · higher: scroll/magnetic).
- **VISUAL_DENSITY**: Information per viewport (lower: spacious · higher: dense dashboards).

### Examples

Created with Good Tast Skill:

<p>
  <img src="examples/floria-top.webp" width="400" />
  <img src="examples/floria-bottom.webp" width="400" />
</p>

### Credits

Good Tast Skill is built on [Taste Skill](https://github.com/Leonxlnx/taste-skill) (MIT) by [Leonxlnx](https://github.com/Leonxlnx). All upstream skill design work is credited to the original author and contributors; this fork adds Chinese-aesthetics tuning and maintains the bilingual documentation.

---

<a id="中文"></a>
## 中文

**Good Tast Skill**（好品味技能）是基于 [Leonxlnx](https://github.com/Leonxlnx) 的优秀开源项目 [Taste Skill](https://github.com/Leonxlnx/taste-skill) 修改而来的独立产品。我们保留了上游项目"反平庸（anti-slop）"的工程纪律，并将**中国审美**融入每条技能的设计规则：大量留白、编辑感的中文排印、不对称但均衡的构图，以及源自当代中国产品设计的克制高级配色。

这是一组可移植的 **Agent Skills**，用于提升 AI 生成界面的品质：更强的版式、字体、动效与间距，摆脱"模板味"UI。仓库还包含面向参考图板的**图像生成技能**（网页、移动端、品牌套件）。可以先配合 **ChatGPT Images** 等生成器出图，再把设计稿交给 Codex、Cursor 或 Claude Code 实现。

### 安装

[`npx skills add`](https://github.com/vercel-labs/agent-skills) CLI 会扫描本仓库的 `skills/` 目录，因此**下方所有技能（代码类与图像生成类）都以相同方式安装**：

```bash
npx skills add https://github.com/cljhadream/good-taste-skill
```

按**安装名**（SKILL frontmatter 中的 `name:` 字段，而非目录名）安装单个技能：

```bash
npx skills add https://github.com/cljhadream/good-taste-skill --skill "design-taste-frontend"
```

也可以把任意 `SKILL.md` 复制进项目，或直接粘贴到 ChatGPT / Codex 对话中使用。

#### 作为 Claude Code 插件安装

如果你只用 Claude Code，可以把整个仓库作为插件安装。所有技能以 `good-tast-skill:` 为命名空间（例如 `/good-tast-skill:imagegen-frontend-web`），不会与其他技能冲突，无需 `npx skills` 步骤。

在 Claude Code 中运行：

```
/plugin marketplace add cljhadream/good-taste-skill
/plugin install good-tast-skill@good-taste-skill
```

之后运行 `/plugin update` 即可升级到新版本。

### 技能列表

每条技能只做一件事，无需全部安装。**实现类技能**输出代码，**图像生成类技能**只输出参考图。`安装名` 是传给 `--skill` 的精确值。

| 技能（目录） | 安装名 | 说明 |
| --- | --- | --- |
| **[taste-skill](skills/taste-skill/SKILL.md)** | `design-taste-frontend` | 🆕 **v2（实验版）**——默认技能。读取需求简报、推断设计语言、调节三个拨盘（VARIANCE / MOTION / DENSITY），并在其上叠加中国审美构图规则。 |
| **[taste-skill-v1](skills/taste-skill-v1/SKILL.md)** | `design-taste-frontend-v1` | 保留的 v1 原始版本，供依赖其确切行为的项目使用。 |
| **[gpt-tasteskill](skills/gpt-tasteskill/SKILL.md)** | `gpt-taste` | 面向 GPT/Codex 的更严格变体：更高的版式变化、更强的 GSAP 指令、激进的反平庸规则。 |
| **[image-to-code-skill](skills/image-to-code-skill/SKILL.md)** | `image-to-code` | 图像优先流水线：先生成网站参考图，再分析，再照图实现前端。 |
| **[redesign-skill](skills/redesign-skill/SKILL.md)** | `redesign-existing-projects` | 面向现有项目：先审计 UI，再修复版式、间距、层级与样式。 |
| **[soft-skill](skills/soft-skill/SKILL.md)** | `high-end-visual-design` | 打磨过的高级感 UI：更柔和的对比、留白、premium 字体、弹性动效。 |
| **[output-skill](skills/output-skill/SKILL.md)** | `full-output-enforcement` | 治"半成品输出"：完整输出、不留占位注释。 |
| **[minimalist-skill](skills/minimalist-skill/SKILL.md)** | `minimalist-ui` | 编辑感产品 UI（Notion/Linear 风格），克制的配色、利落的版面结构。 |
| **[brutalist-skill](skills/brutalist-skill/SKILL.md)** | `industrial-brutalist-ui` | 硬核机械语言：瑞士排印、强对比、实验性版式。 |
| **[stitch-skill](skills/stitch-skill/SKILL.md)** | `stitch-design-taste` | 兼容 Google Stitch 的规则，含可选 `DESIGN.md` 导出格式。 |

### 图像生成技能

只产出设计图（不写代码）。配合 ChatGPT Images、Codex 图像模式或任何能生成图像的 Agent 使用。

| 技能（目录） | 安装名 | 说明 |
| --- | --- | --- |
| **[imagegen-frontend-web](skills/imagegen-frontend-web/SKILL.md)** | `imagegen-frontend-web` | 网页视觉稿：首页、落地页、多版块，强排印、好间距、反平庸美术指导。 |
| **[imagegen-frontend-mobile](skills/imagegen-frontend-mobile/SKILL.md)** | `imagegen-frontend-mobile` | 移动端界面与流程：iOS/Android/跨平台、样机、易读字号、成套一致。 |
| **[brandkit](skills/brandkit/SKILL.md)** | `brandkit` | 品牌套件画板：Logo 方向、配色、字体、跨行业识别应用。 |

### 该用哪一条？

- 通用场景首选 **taste-skill**（最稳的默认选择）。
- 依赖原版 taste-skill 确切行为时，改用 **taste-skill-v1**。
- 想要更严格的 GPT/Codex 规则与动效/版式约束，用 **gpt-taste**。
- 图像 → 分析 → 代码的网站工作流，用 **image-to-code-skill**。
- 改造现有代码库而非从零起样式，用 **redesign-skill**。
- 视觉方向已确定时，叠加 **soft-skill**、**minimalist-skill** 或 **brutalist-skill**。
- Agent 输出总被截断时，加 **output-skill**。
- 交付物就是**图片**（视觉稿、流程图、品牌画板）时，用 **imagegen-** 系列技能，再把结果交给编码 Agent。

### 图像优先小提示

使用 **image-to-code-skill** 时，在提示词里明确流水线，例如：`follow the skill: generate images, then analyze, then code`。

### 设置（仅 taste-skill）

文件顶部的数字是 1-10 的拨盘：

- **DESIGN_VARIANCE**：版式实验程度（低：居中干净 · 高：不对称现代）。
- **MOTION_INTENSITY**：动效深度（低：hover 悬停 · 高：滚动/磁吸）。
- **VISUAL_DENSITY**：每屏信息密度（低：疏朗 · 高：密集仪表盘）。

### 示例

由 Good Tast Skill 生成：

<p>
  <img src="examples/floria-top.webp" width="400" />
  <img src="examples/floria-bottom.webp" width="400" />
</p>

### 致谢

Good Tast Skill 基于 [Taste Skill](https://github.com/Leonxlnx/taste-skill)（MIT 协议）构建，感谢原作者 [Leonxlnx](https://github.com/Leonxlnx) 与所有上游贡献者。本分支在其基础上进行中国审美调优，并维护中英双语文档。

## License

[MIT License](LICENSE) · Based on Taste Skill, Copyright (c) 2026 Leonxlnx · Good Tast Skill is maintained by Gutast AI
