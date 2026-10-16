# Language and translation / 语言与翻译

## Current decision / 当前选择

| Part / 部分 | Language / 语言 | Purpose / 用途 |
|---|---|---|
| README.md | English | Public introduction and setup / 对外介绍与安装 |
| README.zh-CN.md | 简体中文 | Full introduction for Chinese readers / 中文完整说明 |
| SKILL.md body and references | 简体中文 | One authoritative workflow / 一套权威规则 |
| Skill description | English + 中文关键词 | Discovery context / 技能发现信息 |
| Display name and starter prompt | English | A concise public entry point / 简洁的公开入口 |
| Example guide | English + 中文 | Make the sample understandable without translating every rule / 独立解释演示案例 |

The fetched [official skill format](https://learn.chatgpt.com/docs/build-skills) specifies metadata and supporting files without stating that the instruction body must be English. Our publishing choice is therefore an editorial decision, not a format requirement. No claim is made that all hosts or models handle every language equally well.

核对过的官方技能格式说明没有将“正文必须是英文”列为要求。因此，这里的语言安排属于发布与维护选择，不代表所有宿主或模型的跨语言表现完全相同。

## How to use another response language / 如何使用其他回复语言

Mention the skill and ask explicitly, for example: `Use $poster-assembly and respond in English.` Start with a planning-only request and check whether the agent preserves the workflow and critical distinctions.

中文可直接说：`使用 $poster-assembly，用中文回复。` 先做不生成图像的规划任务，检查是否正确理解阶段、授权及交付范围。

## When a full translation becomes useful / 何时值得完整英译

A complete English instruction set is useful when non-Chinese maintainers need to review or edit the rules, or a target host does not handle the current body reliably. It should be reviewed for behavioral equivalence before being advertised as supported.

当主要协作者无法审阅中文规则，或目标宿主不能可靠理解现有正文时，再维护完整英译更有价值。不能仅凭英文 README 就宣称技能全文已有英文版本。

Maintain a translation checklist for trigger scope, stage gates, existing authorizations, print versus screen specs, QR units, and truthful delivery. Do not install two skill folders with the same name merely to offer two languages; use one chosen instruction set or an explicit routing design if full translations are introduced.

翻译核对重点为触发范围、阶段确认、授权复用、印刷与屏幕规格、二维码单位和实际交付状态。新增完整译本时明确对应版本，避免安装两个同名技能导致重复出现。
