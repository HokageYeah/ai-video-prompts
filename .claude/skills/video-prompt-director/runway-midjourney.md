---
name: video-platform-runway-midjourney
description: Runway Gen-4.5 + Midjourney 视频平台提示词参考 — Midjourney 参数、提示词结构、Runway 当前产品线说明
---

# Runway & Midjourney Platform Reference

## Runway

### Current Product Lineup (2025-2026)

Runway 已从 Gen-3 迁移至新一代产品：

| Product | Description | Status |
|---------|-------------|--------|
| Gen-4.5 | 最新视频生成模型 | Current |
| Act-Two | 动作/运动控制 | Current |
| GWM-1 | General World Models | Active |
| Aleph | AI 创意工具 | Active |
| Robotics SDK | 机器人视觉 SDK | Active |
| API | 开发者接口 | Active |

> **Note**: Gen-3 is now legacy. Official documentation for prompt engineering has been removed from public access. Gen-4.5 prompts follow similar principles but with enhanced physics and consistency.

### Runway Prompt Tips (Community-Sourced Best Practices)

Based on community knowledge and legacy Gen-3 guidance:

1. **Structure**: Subject → Action → Environment → Style → Camera
2. **Camera terms work well**: "tracking shot", "crane shot", "dolly zoom"
3. **Motion Brush** (if available): Paint areas of the image to animate with directional control
4. **Style references**: Upload reference images for consistent visual style
5. **Keep prompts concise**: 1-3 sentences typically optimal
6. **Emotional keywords**: "dramatic", "serene", "tense" influence generation
7. **Negative prompting** via UI controls for unwanted elements

### Runway Limitations (Known)

- Gen-3 documentation removed; Gen-4.5 docs behind login
- Help articles returning 404 for public URLs
- Community tips vary in reliability
- No publicly accessible API documentation for prompt parameters

---

## Midjourney

### Video Parameters

Midjourney 的视频功能通过以下参数控制：

| Parameter | Values | Default | Effect |
|-----------|--------|---------|--------|
| --motion | low, high | (none) | 控制画面运动幅度 |
| --raw | (flag) | off | 减少创意增强，提升提示词控制精度 |
| --stylize | 0-1000 | 100 | 控制美学风格化强度 |
| --sw | 0-1000 | 100 | Style Reference 权重 |
| --sv | 1-4 | 4 | Style Reference 版本 |
| --weird | 0-3000 | 0 | 生成不寻常/怪异的结果 |
| --quality | 0.25, 0.5, 1 | 1 | 生成质量/细节花费 |

### Motion Levels

```
--motion low
  - 默认倾向静止场景
  - 低幅度镜头运动
  - 角色微小动作（呼吸、眨眼）
  - 适合：肖像、静物、氛围场景

--motion high
  - 大幅度镜头运动
  - 更大的角色动作
  - 可能出现画面 glitch
  - 适合：动作场景、运镜展示
```

### Stylize Presets

```
--stylize 50    Low      — 接近提示词字面描述
--stylize 100   Medium   — 平衡（默认）
--stylize 250   High     — 明显的艺术风格化
--stylize 750   Very High — 强烈风格化，可能偏离提示词
```

### Raw Mode

```
--raw
  - 减少Midjourney的创意增强
  - 提供更精确的提示词控制
  - 减少默认美学倾向
  - 适合需要精确还原描述的场景
```

### Midjourney Prompt Structure

Midjourney 官方推荐的提示词结构：

```
[Subject]: Who or what?
  person, animal, character, location, object

[Medium]: In what form?
  photo, painting, illustration, sculpture, doodle, tapestry

[Environment]: Where?
  indoors, outdoors, on the moon, underwater, in the city

[Lighting]: What kind?
  soft, ambient, overcast, neon, studio lights

[Color]: In what shades?
  vibrant, muted, bright, monochromatic, colorful, black and white, pastel

[Mood]: Feelings to evoke?
  playful, calm, gloomy, energetic

[Composition]: How is it framed?
  portrait, headshot, closeup, birds-eye view
```

### Example Midjourney Video Prompt

```
a weathered fisherman mending nets on a wooden dock, oil painting style,
foggy harbor at dawn, soft diffused golden light, muted teal and amber
color palette, contemplative mood, wide shot with shallow depth of field
--motion low --stylize 200 --ar 16:9
```

### Style Reference (--sref)

```
--sref URL           引用图片作为风格参考
--sref URL1 URL2     多图混合风格
--sw 200             风格权重（0-1000）
--sv 4               风格版本（最新=4）
```

### Character Reference (--cref)

```
--cref URL           引用角色外貌一致性
--cw 100             角色权重（0=面部only, 100=面部+服装+发型）
```

### Midjourney Style Keywords Collection

#### Film Stock Keywords

```
shot on 35mm film, shot on 120mm medium format, IMAX footage,
polaroid aesthetic, disposable camera, daguerreotype, tintype
```

#### Rendering Keywords

```
cinematic style, commercial quality, photorealistic, hyperrealistic,
4K resolution, 8K resolution, HDR, ultra-detailed, sharp focus
```

#### Depth & Focus Keywords

```
depth of field, bokeh effect, shallow DOF, deep focus,
tilt-shift, soft focus, motion blur, rack focus
```

#### Lens Effect Keywords

```
lens flare, chromatic aberration, anamorphic flare,
barrel distortion, vignette, light leak, film grain
```

#### Art Movement Keywords

```
impressionist, expressionist, art nouveau, art deco,
bauhaus, pop art, surrealism, minimalism, baroque
```

## Platform Comparison Matrix

| Feature | Sora | Kling | Runway Gen-4.5 | Midjourney |
|---------|------|-------|----------------|------------|
| Text-to-Video | Yes | Yes | Yes | No (image-first) |
| Image-to-Video | Yes | Yes | Yes | Yes (--motion) |
| Camera Control | Prompt-based | API params | UI + Prompt | Prompt-based |
| Multi-Shot | Storyboard | API multi_prompt | UI Timeline | No |
| Audio Generation | Yes (Sora 2) | Yes (sound: on) | Unknown | No |
| Max Duration | ~20s | 5-10s per shot | ~10s | ~4s |
| Negative Prompt | No | Yes | UI Controls | No |
| API Access | Limited | Yes | Yes | No |
| Prompt Limit | ~unlimited | 2500 chars | Unknown | ~6000 chars |

## Luma (Documentation Gap)

> **Status**: Luma has pivoted from "Dream Machine" to "Luma Agents" platform.
> Official documentation for prompt engineering is not publicly accessible.
> All help/learn pages return 403 Forbidden or network errors.
> Luma Agents now integrates multiple models (Uni-1, Ray3.14, Sora 2, Veo 3, Kling, etc.)
> as an agentic creative workflow rather than a standalone video generator.

### What We Know (From Product Page)

- Platform shifted to agent-based creative workflow
- Multiple model integration (including third-party models)
- Focus on creative workflow automation rather than direct prompt-to-video
- No public prompt engineering documentation available

### Recommended Approach for Luma

When users target Luma, use general best practices:
1. Apply Sora/Kling prompt structures as Luma integrates these models
2. Focus on clear subject + action + environment descriptions
3. Use cinematic terminology for camera and lighting
4. Describe materials and physics explicitly
5. Keep total prompt concise (under 500 words)
