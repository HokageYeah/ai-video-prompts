---
name: video-platform-sora
description: OpenAI Sora 平台提示词工程参考 — Five Pillars 框架、World Simulator 范式、Sora 2 新特性、提示词模板与关键词库
---

# Sora Platform Reference

## Sora Prompt Engineering Framework

### The Five Pillars (Sora 提示词五柱模型)

Every effective Sora prompt addresses five core dimensions:

| Pillar | 中文 | 核心问题 | 关键术语 |
|--------|------|---------|---------|
| Subject & Character | 主体与角色 | Who/What is in the scene? | species, body type, clothing, expression, material texture |
| Action & Motion | 动作与运动 | What is happening? | verb phrases, motion direction, speed, physical constraints |
| Environment & Setting | 环境与场景 | Where does it take place? | location, time of day, weather, atmospheric conditions |
| Cinematic Framing | 电影构图 | How is it filmed? | camera type, lens, angle, movement, depth of field |
| Aesthetic & Style | 美学与风格 | What is the visual look? | film stock, color grade, rendering technique, art movement |

### Sora Prompt Template

```
[SUBJECT] [ACTION] [ENVIRONMENT] [CAMERA] [STYLE] [AUDIO (Sora 2)]
```

Example:
```
A red fox with silver-tipped fur [SUBJECT]
trotting through fresh snow, leaving deep paw prints [ACTION]
in a birch forest at twilight, snowflakes drifting [ENVIRONMENT]
tracked by a Steadicam at eye level, shallow depth of field [CAMERA]
shot on 35mm film with warm amber color grading, cinematic [STYLE]
gentle crunching of snow, distant owl hoot, wind rustling branches [AUDIO]
```

### World Simulator Paradigm

Sora operates as a "world simulator" — it models miniature self-consistent worlds. To leverage this:

1. **Describe physical laws explicitly**: gravity direction, material density, fluid behavior
2. **Specify material properties**: metal reflectivity, cloth weight, skin translucency, glass refraction
3. **Environmental conditions**: air density, temperature (affects fog/steam), light scattering medium
4. **Temporal dynamics**: rate of change, acceleration curves, cause-and-effect chains

Example of World Simulator thinking:
```
Instead of: "water splashes"
Write: "water droplets launch from the impact point in a parabolic arc,
surface tension holding each drop spherical, catching and refracting
golden hour sunlight into miniature rainbows before gravity pulls
them back to the dark wet sand"
```

## Sora 2 Features (Released Sept 30, 2025)

| Feature | Description | Prompt Implication |
|---------|-------------|-------------------|
| Synchronized Audio | Generates matching audio from prompt | Add audio description: "sound of rain on tin roof, distant thunder" |
| Enhanced Physics | Improved physical consistency | Can describe complex physical interactions with confidence |
| Self-Insertion Cameos | Place yourself in generated video | Reference image + "person in red jacket" |
| Advanced Cinematic Control | Precise camera and timing | Use exact camera terminology for predictable results |
| Storyboard Mode | Multi-scene generation | Break timeline into scenes with distinct prompts |

## Sora Prompt Categories (Official Classification)

1. **Official Examples** — OpenAI's curated showcase prompts
2. **Viral Prompts** — Community-shared high-engagement prompts
3. **Hyperrealism & Landscapes** — Photorealistic natural/urban scenes
4. **Surreal & Imaginative** — Dream-like, physics-bending content
5. **Character-Driven Narratives** — Story-focused with emotional arcs
6. **Stylized & Animation** — Non-photorealistic artistic styles
7. **Historical & Archival** — Period-accurate, vintage film looks
8. **Cinematic Styles** — Specific film/director style emulation

## Sora Prompt Engineering Lessons

### What Works

1. **Sensory details are powerful**: temperature, texture, reflections, smell-related visual cues
2. **Implicit physics work**: "glass shattering on stone" → Sora infers shatter pattern
3. **Cinematic terms are leverage**: "shot on Arriflex 35mm" produces predictable film quality
4. **Brevity can win**: Short, precise prompts sometimes outperform verbose ones
5. **Temporal adverbs help**: "slowly", "suddenly", "gradually", "instantly"
6. **Emotional adjectives transfer**: "peaceful", "tense", "melancholic" influence camera and lighting

### What to Avoid

1. Don't over-describe — Sora infers physics and details
2. Avoid contradictory descriptions (e.g., "dark shadows" + "bright noon sun")
3. Don't mix incompatible styles without explicit transition cues
4. Avoid abstract concepts without visual anchors

## Camera Keywords for Sora

| Category | Keywords |
|----------|----------|
| Camera Type | drone view, bird's eye view, worm's eye view, eye-level, overhead |
| Shot Size | extreme wide shot (EWS), wide shot (WS), medium shot (MS), close-up (CU), extreme close-up (ECU) |
| Lens | 35mm, 50mm, 85mm, 135mm, 600mm telephoto, 14mm wide-angle, anamorphic, macro lens |
| Movement | dolly in/out, tracking shot, crane shot, pan left/right, tilt up/down, handheld, steadicam, gimbal, whip pan, zoom in/out |
| Focus | shallow depth of field, deep focus, rack focus, soft focus, tilt-shift |
| Angle | low angle, high angle, Dutch angle/tilt, bird's eye, worm's eye, over-the-shoulder, POV |

## Lighting Keywords for Sora

| Category | Keywords |
|----------|----------|
| Natural | golden hour, blue hour, overcast, harsh noon sun, moonlight, dappled light, dappled shade |
| Artificial | neon lights, candlelight, street lamps, studio lighting, fluorescent, tungsten |
| Cinematic | high-key lighting, low-key lighting, Rembrandt lighting, butterfly lighting, split lighting |
| VFX | volumetric lighting, god rays, Tyndall effect, lens flare, rim light, backlight, silhouette |
| Quality | soft diffused, hard directional, ambient, dramatic, moody, flat, chiaroscuro |

## Color Grading Styles for Sora

| Style | Keywords | Color Palette |
|-------|----------|--------------|
| Cyberpunk | neon purples, blues, pinks, cyan | Magenta + Cyan + Deep Black |
| Orange Teal (Blockbuster) | teal and orange, complementary | Orange highlights + Teal shadows |
| Vintage Film | faded, warm yellow, desaturated | Warm amber + Faded greens |
| Saturated Color | hyper-saturated, vibrant, punchy | Full spectrum, pushed saturation |
| Black & White | monochrome, noir, silver gelatin | Grayscale only |
| 35mm Film Classic | shot on Kodak, film grain, classic | Warm midtones + Cool shadows |
| Bleach Bypass | desaturated, high contrast, metallic | Washed-out color + Deep blacks |
| Cross-Processed | unnatural colors, shifted hues | Green shadows + Magenta highlights |

## Motion & Physics Keywords for Sora

| Category | Keywords |
|----------|----------|
| Speed | slow motion, time-lapse, speed ramping, real-time, ultra slow-motion |
| Fluid | rippling water, flowing stream, rain drops, ocean waves, splashing, dripping |
| Air | blowing in the wind, floating, drifting, swirling dust, smoke rising, mist rolling |
| Physical | falling, bouncing, spinning, tumbling, vibrating, shaking, swinging, swaying |
| Transform | melting, crystallizing, evaporating, dissolving, shattering, bending, stretching |
| Biological | breathing, blinking, heart beating, hair swaying, cloth fluttering, grass bending |
| Camera Motion | parallax scrolling, zoom, orbit, fly-through, reveal, pull-back, push-in |

## Film Stock Emulation Keywords

| Film Stock | Keywords |
|------------|----------|
| Kodachrome 64 | kodachrome, warm tones, rich reds, deep blues, fine grain |
| Kodak Portra 400 | portra, soft pastel tones, natural skin, fine grain, warm |
| Fujifilm Velvia 50 | velvia, hyper-saturated, vivid greens and blues, fine grain |
| Ilford HP5 Plus | ilford, black and white, visible grain, high contrast |
| CineStill 800T | cinestill, tungsten balanced, halation glow, night photography |
| Kodak Vision3 500T | vision3, cinema film, tungsten, subtle grain, wide latitude |
| Polaroid | polaroid, instant film, washed out colors, white border, soft focus |
