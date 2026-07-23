# Video of S.A.D. by AI

以 AI 生成「憂鬱水手鬍渣男（S.A.D.／Sailor At Desk）」循環短影片，並善用社群平台的長按倍速播放，創造低成本、可重複、帶有黑色幽默的互動內容。

## 專案目標

這個倉庫提供一套可重複使用的 AI 動畫生成流程，讓使用者只需替換：

- 場景
- 重複動作
- 背景動態
- 聲音設計
- 額外限制

即可快速產生 4 秒左右、9:16、首尾一致的循環影片。

核心角色為 **S.A.D.（Sailor At Desk）**：一位疲憊、厭世、留著鬍渣的水手型角色。正常播放時節奏緩慢，長按社群短影音畫面後，平台原生 2 倍速會讓畫面與聲音同步加速，形成反差式幽默。

## 快速開始

1. 準備一張 S.A.D. 角色參考圖。
2. 開啟 `prompts/scene_template.yaml`。
3. 修改場景、主要動作、背景動態、聲音與特殊要求。
4. 將內容套入 `prompts/Gemini_Veo_Animation_Engine_v1.0.md`。
5. 把角色參考圖與 Prompt 一起上傳至 Google Gemini / Veo。
6. 生成 4 秒、9:16、固定鏡頭、首尾一致的循環影片。
7. 上傳至 Reels、Shorts 或 TikTok。
8. 在畫面加入「長按紅點」等引導，利用平台內建倍速播放製造互動效果。

## 倉庫結構

```text
Video_of_SAD_by_AI/
├── README.md
├── CHANGELOG.md
├── CONTRIBUTING.md
├── LICENSE
├── docs/
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

## 影片標準規格

| 項目 | 建議值 |
|---|---|
| 比例 | 9:16 |
| 解析度 | 1080 × 1920 |
| 時長 | 4 秒 |
| 幀率 | 24 fps |
| 鏡頭 | 固定鏡頭 |
| 動作循環 | 1–3 秒 |
| 首尾畫面 | 必須一致 |
| 音訊 | 與畫面同步，可在倍速時同步加速 |

## 幽默效果設計公式

```text
緩慢、認真、略顯荒謬的重複動作
            +
觀眾長按畫面觸發平台 2 倍速
            +
同步加速的環境音與角色動作
            =
反差式幽默與偽互動體驗
```

範例：

- 水手慢慢划船 → 長按後瘋狂趕路
- 水手無奈打字 → 長按後像月底報表爆炸
- 水手超慢跑 → 長按後像被 KPI 追殺

## 重要限制

社群貼文中的紅點通常不是「真正可程式化的按鈕」。真正產生加速的是平台原生的長按倍速功能。因此應使用清楚的引導文案，例如：

> 長按紅點，不要放開。

並在發布後使用 iPhone、Android 與不同帳號實測。

## 版本

- **v1.0**：Gemini / Veo 循環影片 Prompt Engine。
- **v2.0**：跨平台 AI 動畫宇宙工作流，涵蓋角色、影片、音效、配音、社群發布與版本管理。

## 授權

本倉庫程式與文件採 MIT License。角色名稱、人物設定、圖像與品牌資產仍由原作者保留相關權利。
