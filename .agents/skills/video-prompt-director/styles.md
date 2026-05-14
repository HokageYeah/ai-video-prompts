---
name: video-styles
description: AI 视频预设风格库详细参考 — 多种核心风格的 CG 术语、光影参数、色彩空间定义
---

# Preset Style Library Reference

本文档为预设风格提供精确的术语和参数参考，供 prompt 生成时直接引用。

---

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

---

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

---

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

---

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

---

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

---

## Style 6: 黑色电影 Film Noir

| 维度 | 关键术语 |
|------|---------|
| 渲染 | High contrast B&W, deep crushed shadows, single-source hard lighting |
| 镜头 | Dutch angles, deep focus, low-key lighting compositions, venetian blind shadow patterns |
| 光照 | Single hard key light, venetian blind shadows, cigarette smoke catching light beams, rain-streaked windows |
| 色彩 | Monochrome with optional selective color (red lips, green eyeshadow), silver gelatin print quality |
| 材质 | Wet black streets, trench coat gabardine texture, fedora felt, cigarette smoke volume |
| 特效 | Rain streaks, fog/mist layers, shadow play on walls, light through blinds |

**Prompt 关键词**: `classic film noir, high contrast black and white, venetian blind shadow patterns, single hard key light, deep shadows, cigarette smoke catching light, wet streets reflecting street lamps, trench coat detective, 1940s cinematography`

---

## Style 7: 日系恐怖 J-Horror

| 维度 | 关键术语 |
|------|---------|
| 渲染 | Desaturated cool tones, high contrast in shadows, film grain, slight green/teal color shift |
| 镜头 | Static locked-off shots, slow deliberate pans, deep focus revealing background details |
| 光照 | Cold fluorescent overhead, underlit faces, shadows with implied presence, unnatural light flicker |
| 色彩 | Desaturated blue-green palette, sickly pale skin tones, cold white highlights |
| 材质 | Peeling wallpaper, damp surfaces, aged wood grain, dusty glass, stained concrete |
| 特效 | Subtle non-natural motion (glitchy, reversed), hair as entity, unnatural stillness, light flicker |

**Prompt 关键词**: `J-horror aesthetic, desaturated blue-green palette, cold fluorescent lighting, deep shadows with implied presence, static camera, damp peeling walls, unnatural stillness, slow deliberate camera movement, pale ghostly figures`

---

## Style 8: 蒸汽朋克 Steampunk

| 维度 | 关键术语 |
|------|---------|
| 渲染 | Warm bronze tones, mechanical detail rendering, patina and oxidation on metals |
| 镜头 | Close-up on mechanical details, rack focus between gears and character, warm tungsten lighting |
| 光照 | Warm tungsten/orange practicals, steam-lit environments, firelight, oil lamp glow |
| 色彩 | Warm bronze/copper/brass palette, deep mahogany browns, amber highlights, oxidized green accents |
| 材质 | Polished brass, steam-oxidized copper, tooled leather, mahogany wood, glass vacuum tubes |
| 特效 | Steam venting, gear rotation, piston motion, spark shower, clockwork precision |

**Prompt 关键词**: `steampunk Victorian aesthetic, polished brass and copper machinery, steam vents and gear mechanisms, warm amber tungsten lighting, tooled leather and mahogany, oxidized metal patina, intricate clockwork detail`

---

## Style 9: 韦斯·安德森对称美学 Wes Anderson

| 维度 | 关键术语 |
|------|---------|
| 渲染 | Flat, centered, symmetrical composition, pastel color palette, minimal depth |
| 镜头 | Dead-center symmetrical framing, flat frontal camera, occasional slow lateral tracking |
| 光照 | Even, flat lighting with minimal shadows, soft pastel-friendly illumination |
| 色彩 | Curated pastel palette (mustard yellow, dusty pink, mint green), complementary accent colors |
| 材质 | Wallpaper patterns, vintage fabric textures, whimsical props, taxidermy |
| 特效 | Whip pan transitions, slow-motion character walks, symmetrical group compositions |

**Prompt 关键词**: `Wes Anderson symmetrical composition, centered framing, pastel color palette, flat even lighting, curated vintage aesthetic, mustard yellow and dusty pink, whimsical props, dead-center camera, whip pan transitions`

---

## Style 10: 梦幻童话 Fantasy Fairytale

| 维度 | 关键术语 |
|------|---------|
| 渲染 | Ethereal glow, soft bloom effect, enchanted particle systems, luminous atmosphere |
| 镜头 | Sweeping crane shots, gentle push-ins, shallow DOF with dreamy bokeh |
| 光照 | Bioluminescent sources, magical light emanating from objects, golden hour extended, starlight |
| 色彩 | Jewel tones (emerald, sapphire, amethyst), gold accents, luminous highlights |
| 材质 | Translucent magical materials, crystalline structures, enchanted wood grain, flowing silk |
| 特效 | Floating particles (fireflies, pollen, magical dust), light trails, ethereal fog, bioluminescent glow |

**Prompt 关键词**: `enchanted fairytale atmosphere, bioluminescent glow, ethereal particles, magical light emanating from objects, jewel-tone color palette, crystalline structures, sweeping crane shot, dreamy shallow DOF, luminous golden atmosphere`

---

## Color Grading Quick Reference

| 色彩风格 | 英文关键词 | 色彩特征 |
|---------|-----------|---------|
| 赛博朋克 | Cyberpunk neon | 品红 + 青色 + 深黑 |
| 青橙大片 | Orange Teal Blockbuster | 橙色高光 + 青色阴影 |
| 复古胶片 | Vintage Film | 暖琥珀 + 褪色绿 |
| 超饱和 | Hyper-Saturated | 全光谱，推高饱和度 |
| 黑白 | Monochrome / Noir | 纯灰度 |
| 35mm 经典 | 35mm Film Classic | 暖中间调 + 冷阴影 |
| 漂白旁路 | Bleach Bypass | 褪色 + 高对比 + 金属感 |
| 交叉冲洗 | Cross-Processed | 绿色阴影 + 品红高光 |
| 莫兰迪 | Morandi / Pastel | 灰调柔和、低饱和 |
| 日系清新 | Japanese Light & Airy | 过曝 + 低对比 + 淡蓝 |

---

## Film Stock Quick Reference

| 胶片型号 | 关键词 | 视觉效果 |
|---------|--------|---------|
| Kodachrome 64 | `kodachrome` | 暖色、丰富红蓝、细颗粒 |
| Kodak Portra 400 | `portra 400` | 柔和粉彩、自然肤色 |
| Fujifilm Velvia 50 | `velvia` | 超饱和、鲜艳绿蓝 |
| Ilford HP5 Plus | `ilford hp5` | 黑白、可见颗粒 |
| CineStill 800T | `cinestill 800t` | 钨丝灯平衡、光晕效果 |
| Kodak Vision3 500T | `vision3 500t` | 电影胶片、微妙颗粒 |
| Polaroid | `polaroid` | 褪色、白边框、柔焦 |

---

## Lighting Mood Quick Reference

| 情绪 | 光照方案 | 关键词 |
|------|---------|--------|
| 温暖/安全 | Golden hour, warm directional | `golden hour, warm light, soft shadows` |
| 紧张/不安 | Low-key, hard shadows, flicker | `low-key, harsh shadows, unstable light` |
| 神秘/未知 | Volumetric fog, single source, silhouette | `volumetric fog, silhouette, single beam` |
| 浪漫/梦幻 | Soft diffused, bokeh, lens flare | `soft diffused, dreamy bokeh, warm flare` |
| 冷酷/科技 | Blue-white fluorescent, no warmth | `sterile fluorescent, cold blue-white, no warmth` |
| 史诗/宏大 | Golden hour + rim light + wide lens | `epic golden hour, rim light silhouette, ultra-wide` |
| 恐怖/诡异 | Underlit, green shift, flicker | `underlit, sickly green, unstable flicker` |
| 怀旧/记忆 | Warm amber, soft vignette, grain | `warm amber glow, vignette, film grain, nostalgic` |
