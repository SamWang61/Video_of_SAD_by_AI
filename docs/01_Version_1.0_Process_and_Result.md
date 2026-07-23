# Version 1.0：Gemini / Veo 循環動畫引擎
# Version 1.0: Gemini / Veo Seamless Loop Animation Engine

## 起點｜Starting Point

需求是以既有的 S.A.D. 角色參考圖，產生手機直式、約 4 秒、可無限循環的短影片。第一個場景為水手辛苦划船，並包含海浪、海鷗、船身晃動與同步環境音。

The goal was to use an existing S.A.D. character reference image to generate a vertical mobile video of approximately four seconds that could loop indefinitely. The first scene showed the sailor rowing with visible effort, accompanied by ocean waves, flying seagulls, rhythmic boat motion, and synchronized environmental sound.

## 問題拆解｜Problem Breakdown

1. 角色必須跨幀一致。  
   The character must remain visually consistent across all frames.
2. 主動作必須在 1–3 秒內完成一個閉合週期。  
   The main action must complete a closed cycle within 1–3 seconds.
3. 第一幀與最後一幀必須一致。  
   The first and last frames must match.
4. 船、海浪、海鷗、浮標與光暈也要各自完成循環。  
   The boat, waves, seagulls, buoy, and glow must each complete their own loops.
5. 音訊需要與動作節奏同步。  
   Audio must be synchronized with the movement rhythm.
6. 影片在正常速度與 2 倍速下都要自然。  
   The clip should remain readable and entertaining at both normal speed and 2× playback.

## v1.0 解法｜v1.0 Solution

建立參數化 Prompt Engine，固定角色、鏡頭、輸出規格、物理反應、循環規則與負面限制，只替換以下內容：

A parameterized prompt engine was created. Character identity, camera, output specifications, physics, loop requirements, and negative constraints remain fixed. Only the following elements are replaced:

- 場景｜Scene
- 主要重複動作｜Primary repeated action
- 背景動態｜Background motion
- 聲音細節｜Sound details
- 幽默設定｜Comedy setup and payoff
- 額外要求｜Additional requirements

## 成果｜Deliverables

- `prompts/Gemini_Veo_Animation_Engine_v1.0.md`
- `prompts/character_lock.md`
- `prompts/scene_template.yaml`
- `examples/001_endless_rowing.md`
- `examples/002_typing_forever.md`
- `examples/003_slow_jogging.md`

## v1.0 適用範圍｜Recommended Use Cases

v1.0 適合單一角色、單一固定鏡頭，以及約 4 秒的短循環動畫。它特別適合 Reels、Shorts、TikTok 與其他手機直式內容。

Version 1.0 is best suited for a single character, one locked camera angle, and a short loop of approximately four seconds. It is particularly suitable for Reels, Shorts, TikTok, and other vertical mobile content.

若需要跨平台生成、配音、背景音樂、發布規劃、內容系列化或品牌資產管理，請使用 v2.0。

For cross-platform generation, voice-over, background music, publishing plans, content series management, or brand-asset governance, use Version 2.0.