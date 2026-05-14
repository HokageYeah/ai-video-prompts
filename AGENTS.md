# AGENTS.md

This file provides guidance to Codex (Codex.ai/code) when working with code in this repository.

## Project Overview

AI Video Prompt Director — 将用户模糊的视频创意转化为极致详细、结构清晰、包含精准时间线与 CG 渲染术语的中英文双语提示词。目标平台：Sora, Kling, Runway Gen-3, Luma 等 AI 视频大模型。

**这不是代码项目，是提示词工程项目。** 仓库中没有 build/test/lint 命令。所有产出物为 Markdown 格式的提示词文档。

## Core Skill

使用 `/video-prompt` 触发核心工作流。技能定义在 `.Codex/skills/video-prompt-director/` 目录下：

| 文件 | 用途 |
|------|------|
| `SKILL.md` | 主工作流：三阶段流程（信息采集 → 风格选择 → 提示词生成）+ 输出格式规范 |
| `styles.md` | 五种预设风格的 CG 术语参数表（渲染/镜头/光照/色彩/材质/特效），生成时直接引用 |
| `glossary.md` | CG/VFX 中英文术语速查表，按类别整理（渲染/摄影/物理/光照/色彩） |

## Prompt Output Structure

每份提示词必须严格包含六个段落，中英文各一：

1. **Visual Style & Rendering** — 美学风格、镜头类型、渲染技术、光影氛围、色彩基调
2. **Characters & Props** — 体型/面部/表情/服装材质/道具材质的 CG 级描述
3. **Environment & Scene** — 背景环境/地面材质/天气/空气颗粒/景深虚化
4. **Physics & VFX** — 流体动力学/重力/碰撞反馈/毛发体积物理
5. **Camera Work** — 运镜方式（Dolly/Tracking/Crane/手持等）
6. **Action Timeline** — `[00:00-00:03]` 时间戳逐秒拆解动作/微表情/场景互动

每次生成输出两部分：**中文解析版**（面向用户理解）+ **English Prompt (Copy-Ready)**（可直接粘贴给 AI 视频工具）。

## Platform-Specific Tuning

根据用户指定的目标平台调整术语密度：
- **Sora**：物理一致性和长镜头连贯性
- **Kling**：角色表情细节和动作流畅度
- **Runway Gen-3**：运镜控制和风格化表现
- **Luma**：3D空间感和光影质量
- 未指定则默认通用高质量描述

## Output Location

生成的提示词存放在 `prompts/` 目录，文件命名格式：`{主题关键词}-{风格/类型}.md`

## Key Constraints

- 动作描述必须符合人体/动物工学，具有绝对连贯性
- 时间线拆解以秒为单位，总时长默认 5 秒（用户可指定）
- 不要擅自猜测缺失信息，缺失要素必须向用户提问确认
- CG/VFX 术语需参考 `glossary.md`，风格参数需参考 `styles.md`，不要凭空编造术语
