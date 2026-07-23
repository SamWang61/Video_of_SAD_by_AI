# Video of S.A.D. by AI

> 中文｜English bilingual documentation

## 專案簡介｜Project Overview

本倉庫提供一套可重複使用的 AI 循環短影片生成流程，以「憂鬱水手鬍渣男（S.A.D.／Sailor At Desk）」為核心角色，透過 Google Gemini / Veo 等生成工具，製作 9:16、首尾一致、可無限循環的短影片。

This repository provides a reusable AI workflow for creating seamless looping short videos featuring **S.A.D. — Sailor At Desk**, a tired and melancholic bearded sailor. The workflow is designed for Google Gemini / Veo and similar generative-video tools, producing vertical 9:16 clips whose first and last frames match.

正常播放時，角色以緩慢、認真又略顯荒謬的節奏重複工作；觀眾長按支援倍速播放的社群短影音畫面後，平台原生加速會讓動作與內嵌音效同步加快，形成反差式幽默。

At normal speed, the character performs a slow, serious, slightly absurd repetitive task. When viewers long-press on a social platform that supports accelerated playback, the video and embedded audio speed up together, creating contrast-based comedy.

---

## 專案目標｜Project Goals

使用者只需替換以下參數，即可建立新的循環影片：

Users only need to replace the following parameters to create a new looping video:

- 場景｜Scene
- 重複動作｜Repeated action
- 背景動態｜Background motion
- 聲音設計｜Sound design
- 幽默設定｜Comedy setup and payoff
- 額外限制｜Additional constraints

預設輸出目標為約 4 秒、1080 × 1920、24 fps、固定鏡頭與無縫循環。

The default output target is approximately 4 seconds, 1080 × 1920, 24 fps, a locked camera, and a seamless loop.

---

## 快速開始｜Quick Start

1. 準備 S.A.D. 角色參考圖。  
   Prepare a reference image of the S.A.D. character.
2. 開啟 `prompts/scene_template.yaml`。  
   Open `prompts/scene_template.yaml`.
3. 修改場景、主要動作、背景動態、聲音與特殊要求。  
   Edit the scene, main action, background motion, sound, and special requirements.
4. 將內容套入 `prompts/Gemini_Veo_Animation_Engine_v1.0.md`。  
   Insert the parameters into `prompts/Gemini_Veo_Animation_Engine_v1.0.md`.
5. 將角色參考圖與提示詞一起交給 Google Gemini / Veo。  
   Upload the reference image and prompt to Google Gemini / Veo.
6. 生成 4 秒、9:16、固定鏡頭、首尾一致的循環影片。  
   Generate a 4-second, vertical, locked-camera seamless loop.
7. 上傳至 Reels、Shorts、TikTok 或其他短影音平台。  
   Publish it to Reels, Shorts, TikTok, or another short-video platform.
8. 加入「長按紅點」等視覺引導，利用平台內建倍速播放製造幽默互動。  
   Add a visual cue such as “Press and hold the red dot” to use native speed-up playback as a humorous pseudo-interaction.

---

## 倉庫結構｜Repository Structure

```text
Video_of_SAD_by_AI/
├── README.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── docs/
│   ├── 00_Bilingual_Documentation_Standard.md
│   ├── 01_Version_1.0_Process_and_Result.md
│   ├── 02_Version_2.0_AI_Animation_Universe.md
│   ├── 03_How_to_Create_Seamless_Loops.md
│   ├── 04_Social_Media_Speedup_Effect.md
│   ├── 05_Character_Consistency_Guide.md
│   └── 06_Audio_Design_Guide.md
├── prompts/
│   ├── Gemini_Veo_Animation_Engine_v1.0.md
│   ├── AI_Animation_Universe_Engine_v2.0.md
│   ├── character_lock.md
│   ├── negative_prompt_library.md
│   └── scene_template.yaml
└── examples/
    ├── 001_endless_rowing.md
    ├── 002_typing_forever.md
    └── 003_slow_jogging.md
```

---

## 影片標準規格｜Recommended Video Specifications

| 項目 Item | 建議值 Recommended value |
|---|---|
| 比例 Aspect ratio | 9:16 |
| 解析度 Resolution | 1080 × 1920 |
| 時長 Duration | 4 seconds |
| 幀率 Frame rate | 24 fps |
| 鏡頭 Camera | 固定鏡頭 Locked camera |
| 動作循環 Action cycle | 1–3 seconds |
| 首尾畫面 First and last frame | 必須一致 Must match |
| 音訊 Audio | 與畫面同步，倍速時同步加速 Synchronized with motion and speed-up playback |

---

## 幽默效果公式｜Comedy Formula

```text
緩慢、認真、略顯荒謬的重複動作
Slow, serious, slightly absurd repetition
                +
觀眾長按畫面觸發平台倍速
Viewer long-presses to trigger native speed-up
                +
同步加速的動作與環境音
Motion and sound accelerate together
                =
反差式幽默與偽互動體驗
Contrast comedy and pseudo-interactive fun
```

範例｜Examples:

- 水手慢慢划船 → 長按後像在逃離暴風雨  
  Slow rowing → after speed-up, it looks like an emergency escape.
- 水手無奈打字 → 長按後像月底報表爆炸  
  Tired typing → after speed-up, it becomes month-end reporting chaos.
- 水手超慢跑 → 長按後像被 KPI 追殺  
  Very slow jogging → after speed-up, it looks like he is being chased by KPIs.

---

## 重要限制｜Important Limitation

畫面中的紅點不是影片內真正可程式化的按鈕；它是視覺引導。真正的加速效果來自支援此功能之社群平台的原生長按倍速播放。發布後務必使用不同手機、帳號與平台版本實測。

The red dot is not a programmable button inside the video. It is a visual cue. The actual acceleration comes from the social platform’s native long-press speed-up feature. Always test the published post on different devices, accounts, and app versions.

推薦文案｜Suggested cue:

> 長按紅點，不要放開。  
> Press and hold the red dot. Do not release.

---

## 版本｜Versions

- **v1.0**：Gemini / Veo 循環影片提示詞引擎。  
  Gemini / Veo seamless-loop prompt engine.
- **v2.0**：跨平台 AI 動畫宇宙工作流，涵蓋角色、影片、音效、配音、社群發布與版本管理。  
  Cross-platform AI animation-universe workflow covering character consistency, video, sound, voice, publishing, and version control.

## 文件語言｜Documentation Language

本倉庫所有主要說明文件應同時提供繁體中文與英文。提示詞本體可優先使用英文，以提高生成模型的理解穩定度，但必須附上中文用途與操作說明。

All primary documentation in this repository should be provided in both Traditional Chinese and English. Production prompts may remain primarily in English for model reliability, but they must include Chinese usage notes and explanations.

## 授權｜License

本倉庫程式與文件採 MIT License。角色名稱、人物設定、圖像與品牌資產仍由原作者保留相關權利。

Code and documentation are released under the MIT License. Character names, character designs, images, and brand assets remain the property of their original creator.