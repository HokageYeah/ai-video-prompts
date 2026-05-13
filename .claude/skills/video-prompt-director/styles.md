---
name: video-styles
description: AI 视频预设风格库详细参考 — 五种核心风格的 CG 术语、光影参数、色彩空间定义
---

# Preset Style Library Reference

本文档为五种预设风格提供精确的术语和参数参考，供 prompt 生成时直接引用。

## Style 1: 迪士尼/皮克斯 3D Animation

| 维度 | 关键术语 |
|------|---------|
| 渲染 | Pixar RenderMan, Path Tracing, SSS (Subsurface Scattering), Ambient Occlusion |
| 镜头 | 35mm spherical, deep depth of field, slight barrel distortion |
| 光照 | 3-point lighting with large soft key, warm rim light, colored bounce fill |
| 色彩 | High saturation, warm palette (amber/teal complementary), subtle color grading |
| 角色 | Exaggerated proportions (2-3 head ratio), large expressive eyes, stylized fur/cloth sim |
| 材质 | Stylized PBR, painted texture feel, controlled specularity, matte finish with select glossy accents |

**Prompt 关键词**: `Pixar-quality 3D animation, subsurface scattering skin, exaggerated cartoon proportions, vibrant saturated colors, soft volumetric lighting, physically-based cloth simulation, expressive facial rig`

## Style 2: 60年代原子朋克 Atompunk

| 维度 | 关键术语 |
|------|---------|
| 渲染 | Film grain overlay, chromatic aberration, anamorphic lens flare, vintage color halftone |
| 镜头 | Anamorphic widescreen (2.39:1), vintage Cooke lens characteristics, slight soft focus |
| 光照 | Hard directional light, dramatic shadow patterns, practical neon/fluorescent sources |
| 色彩 | Teal + burnt orange complementary, desaturated midtones, pushed contrast, Kodachrome fade |
| 材质 | Aged patina, rust textures, cracked paint, Bakelite plastic, brushed aluminum with oxidation |
| 特效 | Film scratch, gate weave, light leak, vignette, dust particles in light shafts |

**Prompt 关键词**: `1960s atompunk retro-futurism, anamorphic widescreen, teal and burnt orange color grade, heavy film grain, chromatic aberration, aged metallic surfaces, vintage sci-fi aesthetic, Kodachrome color palette`

## Style 3: 赛博朋克/霓虹暗黑 Cyberpunk

| 维度 | 关键术语 |
|------|---------|
| 渲染 | Ray-traced reflections, volumetric fog/haze, neon bloom, anamorphic streak flare |
| 镜头 | Anamorphic 2.39:1, low angle, Dutch tilt, shallow DOF with oval bokeh |
| 光照 | Neon practicals (magenta/cyan/amber), volumetric haze catching light, underlit faces, neon reflections on wet surfaces |
| 色彩 | Dominant cyan + magenta, deep shadows (crushed blacks), neon color bleeding, HDR highlights |
| 材质 | Wet asphalt with perfect reflections, brushed chrome, holographic surfaces, distressed concrete |
| 特效 | Rain particles, steam vents, holographic projections, lens condensation, light pollution glow |

**Prompt 关键词**: `cyberpunk noir, neon-lit wet streets, volumetric fog, ray-traced puddle reflections, anamorphic lens flare, cyan and magenta neon glow, crushed shadows, rain particle simulation, holographic UI elements`

## Style 4: 极致写实自然纪录片 BBC Earth

| 维度 | 关键术语 |
|------|---------|
| 渲染 | Photorealistic, 8K resolution, RAW sensor quality, minimal post-processing |
| 镜头 | 600mm telephoto compression OR 100mm macro, natural vignette, sharp throughout |
| 光照 | Natural golden hour / overcast diffused / dappled forest light, no artificial fill |
| 色彩 | Rec.2020 wide gamut, natural color accuracy, subtle highlight rolloff, organic tonal gradient |
| 材质 | Ultra-detailed biological textures (feather barbules, skin pores, leaf veins), micro-surface detail |
| 特效 | Natural depth of field, atmospheric haze, pollen/dust motes in backlight, natural motion blur |

**Prompt 关键词**: `BBC Earth documentary quality, 8K photorealistic, natural golden hour lighting, telephoto lens compression, ultra-detailed biological textures, shallow natural DOF, organic color palette, zero artificial styling`

## Style 5: 宫崎骏式手绘动画 Studio Ghibli

| 维度 | 关键术语 |
|------|---------|
| 渲染 | Cel-shaded characters, watercolor background plates, hand-painted texture feel |
| 镜头 | Flat/composition-driven framing, occasional subtle parallax, painted depth layers |
| 光照 | Soft diffused ambient, golden hour warmth, dappled light through foliage, no harsh shadows |
| 色彩 | Pastel warm palette, watercolor transparency, gentle gradient skies, earthy greens and sky blues |
| 材质 | Flat painted characters (limited shading), watercolor wash backgrounds, visible brush texture |
| 特效 | Wind-swept hair/grass (rhythmic wave motion), floating particles (dust motes, petals), cloud movement |

**Prompt 关键词**: `Studio Ghibli hand-drawn animation style, cel-shaded characters, watercolor background, soft golden hour lighting, pastel warm palette, wind-swept dynamic elements, gentle emotional atmosphere, visible brush stroke texture`
