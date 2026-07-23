# Gemini / Veo Animation Engine v1.0

## 使用方式

1. 上傳 S.A.D. 角色參考圖。
2. 複製 `character_lock.md` 內容。
3. 依 `scene_template.yaml` 填寫場景參數。
4. 將下方模板中的 `{{變數}}` 全部替換。
5. 將完整 Prompt 貼入 Gemini / Veo。

---

## Master Prompt

```text
Use the uploaded reference image as the canonical identity of S.A.D. (Sailor At Desk). Preserve the exact same face, beard, hairstyle, sailor hat, sailor outfit, shoes, body proportions, colors and stylized 3D CGI appearance across every frame. Do not redesign or reinterpret the character.

Create a {{DURATION}}-second vertical cinematic animation in 9:16 format, 1080x1920 resolution, 24 fps.

SCENE
Location: {{LOCATION}}
Time of day: {{TIME_OF_DAY}}
Mood: melancholic, subtly humorous, cinematic and emotionally restrained.

CAMERA
Use a completely static locked camera. No zoom, pan, tilt, rotation, handheld movement, cuts or transitions. Keep the composition unchanged throughout the clip.

MAIN ACTION
S.A.D. continuously performs this action: {{MAIN_ACTION}}.
The action must be slow, physically believable, visibly tiring and rhythmically repeatable.
One complete action cycle lasts {{ACTION_CYCLE}} seconds.
The character must return naturally to the exact starting pose at the end.

BACKGROUND MOTION
{{BACKGROUND_MOTION}}
All background movement must be subtle, independent and cyclic. Do not let secondary elements distract from the main action.

SECONDARY CHARACTER MOTION
Add subtle movement to hair, beard, clothing and accessories according to the environment. Allow one slow natural blink only if it can return to the initial eye state before the final frame.

PHYSICS
Use believable weight, inertia, resistance, contact, momentum and secondary motion. Prevent floating objects, sliding feet, disconnected hands or deforming tools.

AUDIO
Create synchronized natural sound design:
{{AUDIO_DETAILS}}
No narration. No human speech. {{MUSIC_REQUIREMENT}}
Use spatial depth so some sounds feel near and others distant.

INTERACTIVE VISUAL CUE
Keep a red circular visual cue in the upper safe area. It remains fixed and may have only a subtle breathing halo. Do not generate text inside the video unless specifically requested.

PERFECT LOOP REQUIREMENT
This must be a perfect seamless infinite loop.
The first and final frame must match in character pose, facial expression, camera position, object placement, lighting, shadows, background state and motion phase.
Design every moving element as a closed motion cycle. There must be no visible jump, pause, flash, crossfade, reset or direction reversal at the loop point.

EXTRA REQUIREMENTS
{{EXTRA_REQUIREMENTS}}

NEGATIVE REQUIREMENTS
No character redesign, face drift, beard drift, costume changes, body proportion changes, extra limbs, missing fingers, object morphing, flicker, lighting variation, camera movement, cuts, subtitles, watermark, unwanted text, fast motion, exaggerated acting, broken physics or broken loop.
```

## 必填變數

| 變數 | 說明 | 範例 |
|---|---|---|
| `{{DURATION}}` | 影片長度 | 4 |
| `{{LOCATION}}` | 場景 | small wooden boat on a calm sea |
| `{{TIME_OF_DAY}}` | 時段 | soft afternoon daylight |
| `{{MAIN_ACTION}}` | 重複主動作 | slowly rowing with visible effort |
| `{{ACTION_CYCLE}}` | 單次循環 | 2 |
| `{{BACKGROUND_MOTION}}` | 背景動態 | seagulls glide, waves move gently |
| `{{AUDIO_DETAILS}}` | 音效 | waves, oar friction, distant gulls |
| `{{MUSIC_REQUIREMENT}}` | 音樂 | No music |
| `{{EXTRA_REQUIREMENTS}}` | 額外限制 | keep buoy rising gently |

## 生成後驗收

- 角色是否與參考圖一致。
- 動作是否能在 1–3 秒內完成閉環。
- 首幀與尾幀是否可直接接續。
- 音效節奏是否與主要動作一致。
- 2 倍速播放時是否仍然清楚、有趣且不過度混亂。
