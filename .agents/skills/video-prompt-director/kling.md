---
name: video-platform-kling
description: 快手 Kling AI 平台提示词工程参考 — API 参数、镜头控制、多镜头、Omni Video、提示词限制与最佳实践
---

# Kling AI Platform Reference

## API Models

| Model | 版本 | 说明 |
|-------|------|------|
| kling-v2-6 | V2.6 | 标准模型 |
| kling-v3 | V3 | 高质量模型 |
| kling-video-o1 | O1 | 推理增强模型 |
| kling-v3-omni | V3 Omni | 多模态融合模型 |

## Core Parameters

### Text-to-Video

```json
{
  "model_name": "kling-v3",
  "prompt": "描述文本（最多 2500 字符）",
  "negative_prompt": "反向提示词（最多 2500 字符）",
  "duration": "5|10",
  "mode": "std|pro",
  "sound": "on|off",
  "aspect_ratio": "16:9|9:16|1:1"
}
```

| Parameter | Values | Notes |
|-----------|--------|-------|
| model_name | kling-v2-6, kling-v3, kling-video-o1 | 选择模型版本 |
| prompt | string (max 2500 chars) | 正向提示词 |
| negative_prompt | string (max 2500 chars) | 排除不想要的元素 |
| duration | "5", "10" | 视频时长（秒） |
| mode | "std", "pro" | 标准/专业模式 |
| sound | "on", "off" | 是否生成音效 |
| aspect_ratio | "16:9", "9:16", "1:1" | 画面比例 |

### Negative Prompt Examples

```
blurry, low quality, distorted faces, extra limbs, deformed hands,
watermark, text overlay, logo, static image, jumpy motion
```

## Camera Control

Kling 支持精确的镜头控制参数：

### Simple Mode

```json
{
  "camera_control": {
    "type": "simple",
    "config": {
      "horizontal": 2.5,
      "vertical": 0,
      "pan": 0,
      "tilt": 0,
      "roll": 0,
      "zoom": 0
    }
  }
}
```

### Advanced Mode

```json
{
  "camera_control": {
    "type": "advanced",
    "config": [
      {
        "control_speed": 0.5,
        "timestamp": 0,
        "horizontal": 0,
        "vertical": 0,
        "pan": 0,
        "tilt": 0,
        "roll": 0,
        "zoom": 0
      },
      {
        "control_speed": 0.5,
        "timestamp": 5000,
        "horizontal": 5,
        "vertical": 2,
        "pan": 10,
        "tilt": -5,
        "roll": 0,
        "zoom": 1.5
      }
    ]
  }
}
```

### Camera Parameters Explained

| Parameter | Range | Effect |
|-----------|-------|--------|
| horizontal | -10 to 10 | 水平移动（负=左，正=右） |
| vertical | -10 to 10 | 垂直移动（负=下，正=上） |
| pan | -10 to 10 | 水平摇镜 |
| tilt | -10 to 10 | 垂直摇镜 |
| roll | -10 to 10 | 滚转（旋转镜头） |
| zoom | -10 to 10 | 缩放（正=推近，负=拉远） |
| control_speed | 0-1 | 镜头运动速度 |

## Multi-Shot (Storyboard Mode)

支持多镜头叙事，最多 6 个分镜：

```json
{
  "model_name": "kling-v3",
  "multi_prompt": [
    {
      "index": 1,
      "prompt": "Two friends talking under a streetlight at night. Warm glow, casual poses, no dialogue.",
      "duration": "2"
    },
    {
      "index": 2,
      "prompt": "A runner sprinting through a forest, leaves flying. Low-angle shot, focus on movement.",
      "duration": "3"
    }
  ],
  "multi_shot": true,
  "shot_type": "customize",
  "duration": "15",
  "mode": "pro"
}
```

| Parameter | Values | Notes |
|-----------|--------|-------|
| multi_shot | true/false | 启用多镜头模式 |
| shot_type | "customize", "intelligence" | 自定义分镜 / AI 自动分镜 |
| multi_prompt[].index | 1-6 | 分镜序号 |
| multi_prompt[].prompt | string | 该分镜的提示词 |
| multi_prompt[].duration | string | 该分镜时长（秒） |

## Omni Video (Multi-Modal Reference)

Kling V3 Omni 支持通过特殊标记在提示词中引用元素、图片和视频：

### Reference Types

```
<<<element_1>>>    引用元素（风格/角色/物体参考）
<<<image_1>>>      引用图片
<<<video_1>>>      引用视频片段
```

### Example Usage

```
<<<element_1>>> A person walking through a forest. <<<image_1>>> shows the person's
appearance. The scene transitions smoothly with <<<video_1>>> as reference for camera movement.
```

### Multi-Image Reference

支持同时参考多张图片：
- 人物外观参考
- 场景环境参考
- 风格参考
- 色调参考

## Kling Prompt Best Practices

### Prompt Writing Tips

1. **主体优先**: 先描述主要角色/物体，再描述环境和动作
2. **动作动词要具体**: 用 "sprinting" 不用 "running"，用 "staring intently" 不用 "looking"
3. **材质描述**: 明确物体材质有助于 Kling 生成更准确的质感
4. **运动方向**: 使用 "from left to right" / "toward camera" 指定运动方向
5. **利用 negative_prompt**: 明确排除不想要的元素比在 prompt 中避免更有效

### Character Description Template

```
[body type] [age/gender] wearing [clothing material and color],
[facial expression], [posture/pose], [hair style and color]
```

### Scene Description Template

```
[location type] during [time of day], [weather condition],
[lighting description], [atmospheric details],
[foreground elements], [background elements]
```

### Action Description Template

```
[subject] [specific verb] [direction/manner],
[secondary motion], [physical feedback],
[camera following/matching the action]
```

## Duration & Mode Recommendations

| Scenario | Duration | Mode | Notes |
|----------|----------|------|-------|
| Single action shot | 5s | std | 简单动作，标准质量 |
| Complex action sequence | 10s | pro | 复杂动作链，需要高质量 |
| Multi-shot narrative | 5s x N | pro | 分镜叙事 |
| Character close-up | 5s | pro | 面部细节要求高 |
| Landscape/Environment | 5-10s | std | 环境展示，标准质量即可 |

## Aspect Ratio Recommendations

| Ratio | Best For | Notes |
|-------|----------|-------|
| 16:9 | 电影风格、风景、叙事 | 最常用的宽屏比例 |
| 9:16 | 手机竖屏、人物特写、社交媒体 | TikTok/抖音风格 |
| 1:1 | 产品展示、社交媒体方形 | Instagram 风格 |
