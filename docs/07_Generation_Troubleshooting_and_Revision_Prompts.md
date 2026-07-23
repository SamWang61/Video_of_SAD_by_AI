# 生成結果不滿意時的處理方式｜Generation Troubleshooting and Revision Prompts

本文件提供 Gemini / Veo 生成循環影片後，若結果不符合預期時的修正策略、判斷原則與可直接使用的提示詞。

This document provides a practical troubleshooting workflow and ready-to-use revision prompts for Gemini / Veo when the generated looping video is not satisfactory.

---

## 一、核心處理原則｜Core Revision Principles

### 1. 一次只修正一類問題

不要在同一輪同時要求修正角色、鏡頭、海浪、音效、節奏與背景。一次改太多項，模型通常會犧牲原本正確的部分。

Do not try to fix character identity, camera, water, audio, timing and background in one regeneration. Changing too many variables at once often breaks parts that were already acceptable.

### 2. 保留原始 Prompt，只追加修正指令

若原始影片已有 70% 正確，不要整份重寫。保留原始 Prompt，追加一段針對問題的補充指令。

If the output is already mostly correct, keep the original prompt and append a focused correction prompt instead of rewriting everything.

### 3. 優先修正順序

1. 角色一致性
2. 肢體與物件物理
3. 鏡頭穩定
4. 循環接點
5. 背景動態
6. 音效
7. 幽默節奏

Recommended order:

1. Character consistency
2. Anatomy and object physics
3. Camera stability
4. Loop seam
5. Background motion
6. Audio
7. Comedic timing

### 4. 每輪都保存版本

建議命名：

```text
SAD_EP001_Endless_Rowing_v01.mp4
SAD_EP001_Endless_Rowing_v02_facefix.mp4
SAD_EP001_Endless_Rowing_v03_loopfix.mp4
```

Keep every version so successful corrections can be compared and reused.

---

## 二、角色變臉或造型漂移｜Character Identity Drift

### 常見症狀

- 臉型改變
- 鬍子忽長忽短
- 帽子或服裝變形
- 身材比例漂移
- 表情過度誇張

### 修正提示詞｜Revision Prompt

```text
Regenerate this video while preserving the uploaded character identity more strictly.

Use the uploaded reference image as the single canonical character source.
Do not alter the face, beard, hairstyle, sailor hat, clothing, shoes, colors or body proportions in any frame.
Reduce facial motion and secondary character motion.
Keep the same tired, melancholic and deadpan facial expression throughout the entire clip.
Prioritize identity stability over expressive animation.
No beautification, no age change, no redesign and no style reinterpretation.
```

### 中文補充指令

```text
請更嚴格鎖定附件角色，臉型、五官、鬍子、髮型、水手帽、服裝、鞋子、身材比例與色彩都不可變更。降低臉部表情與頭部動作，角色全程維持疲憊、厭世、面無表情的狀態。角色一致性優先於動畫誇張度。
```

---

## 三、循環接點跳格｜Visible Loop Jump

### 常見症狀

- 第 8 秒接回第 0 秒時人物突然跳動
- 船、海浪、浮標或海鷗瞬移
- 光線或陰影在接點變化
- 音訊突然中斷

### 修正提示詞｜Revision Prompt

```text
Regenerate with stricter periodic motion and a cleaner seamless loop.

Use two mathematically identical four-second motion cycles within the eight-second video.
At exactly 4.0 seconds and 8.0 seconds, restore the same character pose, facial expression, hand position, oar angle, boat position, water phase, bird positions, buoy tilt, lighting, shadows and audio phase as the first frame.
Remove all one-way drifting motion.
No fade, no crossfade, no reset, no pause and no direction reversal at the loop point.
The final frame must visually match the first frame as closely as possible.
```

### 中文補充指令

```text
請將影片設計為兩個完全相同的四秒循環。第 4 秒與第 8 秒時，人物姿勢、手部、船槳角度、船身位置、海浪相位、海鷗位置、浮標傾斜、光線、陰影與聲音節奏都要回到第一幀狀態。移除單向漂移、淡入淡出、突然停止與回彈。
```

---

## 四、船槳、手部或物件變形｜Oar, Hand or Object Deformation

### 常見症狀

- 多出船槳
- 船槳彎曲或縮短
- 手沒有握住船槳
- 手指融合或數量錯誤
- 船槳穿過船體

### 修正提示詞｜Revision Prompt

```text
Simplify the rowing motion and prioritize rigid object consistency.

Keep exactly two wooden oars.
Keep both oars rigid, symmetrical and permanently connected to the boat's oarlocks.
Keep both hands firmly attached to the handles throughout the motion.
Do not bend, duplicate, shorten, detach, merge or morph either oar.
Reduce the rowing range of motion by approximately 20 percent.
Use slower, cleaner and more symmetrical arm movement.
Prevent fused fingers, extra fingers, floating hands and disconnected wrists.
```

### 中文補充指令

```text
請簡化划船動作，只保留兩支固定、對稱、不可變形的木製船槳。雙手全程握住槳柄，船槳固定於槳架，不可彎曲、複製、縮短、脫落或穿過船體。動作幅度降低約 20%，優先維持手部與船槳的穩定。
```

---

## 五、海鷗瞬移或背景太亂｜Seagull Teleportation or Busy Background

### 常見症狀

- 海鷗突然出現或消失
- 鳥飛出畫面後無法回到起點
- 背景動態搶走角色焦點
- 雲層移動過快

### 修正提示詞｜Revision Prompt

```text
Reduce background complexity and constrain all bird movement.

Use no more than four distant seagulls.
Keep every seagull inside a small closed circular or oval flight path.
No bird may enter or permanently exit the frame.
Return every bird to its exact initial position, scale, orientation and wing phase at the final frame.
Move the clouds extremely slowly or keep them almost static.
Keep all background motion subtle and secondary to the main character.
```

### 中文補充指令

```text
請降低背景複雜度，海鷗最多四隻，全部限制在小範圍封閉圓形或橢圓路徑內，不可突然出現、消失或飛出畫面。影片結尾時，海鷗位置、大小、方向與翅膀相位必須回到第一幀。雲層幾乎靜止。
```

---

## 六、鏡頭不穩或構圖漂移｜Camera Instability or Framing Drift

### 常見症狀

- 自動推近或拉遠
- 鏡頭左右晃動
- 構圖中途改變
- 景深突然變化

### 修正提示詞｜Revision Prompt

```text
Use a completely static locked camera for the entire clip.

Do not zoom, pan, tilt, roll, rotate, reframe, crop, dolly, shake or change focal length.
Keep the character, boat, horizon and red interaction cue in the exact same screen positions throughout the video.
Use constant depth of field and constant focus.
Prioritize framing stability over cinematic camera movement.
```

### 中文補充指令

```text
請鎖定鏡頭，全程禁止推近、拉遠、平移、傾斜、旋轉、重新構圖、裁切、抖動與焦段變化。人物、船、地平線與紅色圓點在畫面中的位置必須保持固定。
```

---

## 七、音效太吵或不自然｜Audio Too Loud or Unnatural

### 常見症狀

- 海浪或海鷗聲太大
- 音效彼此搶頻率
- 船槳聲沒有對準動作
- 循環接點有爆音或斷裂

### 修正提示詞｜Revision Prompt

```text
Reduce overall audio intensity by approximately 40 percent.

Keep ocean waves soft and continuous.
Keep most seagull calls distant and infrequent.
Keep wooden creaks subtle and synchronized precisely with each rowing stroke.
Avoid any loud transient, isolated seagull call, sustained note or abrupt sound at the loop boundary.
Create a smooth eight-second repeatable audio rhythm.
No music, no narration and no human speech.
```

### 中文補充指令

```text
請將整體音量降低約 40%。海浪持續但柔和，海鷗聲以遠距離、低頻率為主，木頭摩擦聲需精準對準每次划槳。循環接點不可出現爆音、突然中斷或單一突出聲音。不要音樂、旁白與人聲。
```

---

## 八、動作不夠好笑｜Weak Comedic Contrast

### 常見症狀

- 正常速度太快
- 2 倍速後反差不明顯
- 表情太活潑，失去厭世感
- 動作沒有「努力卻沒進展」的荒謬感

### 修正提示詞｜Revision Prompt

```text
Strengthen the comedic contrast without changing the character design.

Make the normal-speed rowing approximately 20 percent slower, heavier and more visibly exhausting.
Keep the same four-second action cycle.
Preserve the deadpan, tired and emotionally restrained facial expression.
The boat should move very little despite the character's obvious effort.
At double-speed playback, the rowing, wood creaks and water sounds should become busier and more absurd while remaining readable.
Do not use exaggerated facial comedy.
```

### 中文補充指令

```text
請將正常速度下的划船動作放慢約 20%，增加沉重與疲累感，但維持四秒循環。人物全程維持厭世、疲憊、面無表情。角色明明很努力，船卻幾乎沒有前進，以強化荒謬反差。不要使用誇張表情。
```

---

## 九、動作太快或太亂｜Motion Too Fast or Chaotic

### 修正提示詞｜Revision Prompt

```text
Reduce motion speed and complexity.

Use one simple, readable primary action only.
Reduce the amplitude of arm, torso, boat and water movement by approximately 25 percent.
Remove sudden acceleration and sharp direction changes.
Use smooth ease-in and ease-out timing.
Keep the motion physically believable and easy to understand at both normal speed and double speed.
```

---

## 十、角色與場景比例不正確｜Incorrect Character or Scene Scale

### 修正提示詞｜Revision Prompt

```text
Correct the scale and composition.

Keep S.A.D. as the clear central subject.
Show the full upper body, both hands, both oars and the complete boat without cropping.
Do not make the character too small or the boat oversized.
Keep the horizon behind the character and preserve a centered medium-wide portrait composition.
```

---

## 十一、紅色圓點移動或變形｜Red Interaction Cue Drift

### 修正提示詞｜Revision Prompt

```text
Keep exactly one clean red circular interaction cue in the upper safe area.

The red circle must remain fixed in the same screen position, size, shape and color throughout the complete clip.
It may use only a subtle closed-loop breathing halo.
No text, no additional symbols and no extra red circles.
```

---

## 十二、結果仍然不理想時的處理策略｜When the Result Is Still Unsatisfactory

### 策略 A：降低複雜度

先移除：

- 海鷗
- 浮標
- 雲層漂移
- 鬍子與衣服擺動
- 太複雜的水花

只保留角色、船、船槳與簡單海浪。

Strategy A: remove secondary motion and regenerate a simpler base clip first.

### 策略 B：分兩階段生成

第一階段只生成：

- 角色一致
- 固定鏡頭
- 主動作正確

第二階段再加入：

- 背景動態
- 音效
- 紅色圓點
- 幽默節奏

Strategy B: first solve identity and motion, then add environment and sound.

### 策略 C：重新挑選角色參考圖

若角色一直漂移，改用：

- 正面清楚
- 五官完整
- 背景簡單
- 服裝一致
- 全身比例明確

的單一主參考圖，避免多張圖互相衝突。

### 策略 D：重新生成，不要無限追修同一支

若同一版本已連續修正三次仍然失敗，建議回到原始 Prompt，保留成功條件並重新生成新版本。

If three consecutive corrections fail, restart from the base prompt instead of continuing to patch the same flawed output.

---

## 十三、每次修正前的診斷表｜Pre-Revision Diagnostic Checklist

| 問題 | 是否發生 | 優先級 |
|---|---:|---:|
| 角色變臉 |  | 高 |
| 手或船槳變形 |  | 高 |
| 鏡頭漂移 |  | 高 |
| 循環跳格 |  | 高 |
| 背景瞬移 |  | 中 |
| 音效不自然 |  | 中 |
| 幽默反差不足 |  | 低 |

每次只選一個最高優先問題進行修正。

Choose only one highest-priority issue for each regeneration round.

---

## 十四、建議修正流程｜Recommended Revision Workflow

```text
1. 完整播放影片五次
2. 記錄最嚴重的一個問題
3. 保留原始 Prompt
4. 追加對應的修正提示詞
5. 重新生成並另存新版本
6. 比較新舊版本
7. 再處理下一個問題
```

```text
1. Watch the full video at least five times.
2. Identify the single most serious defect.
3. Keep the original prompt.
4. Append one focused revision prompt.
5. Regenerate and save as a new version.
6. Compare old and new outputs.
7. Fix the next issue only after the previous one is acceptable.
```

---

## 十五、快速修正提示詞索引｜Quick Prompt Index

| 問題 | 使用章節 |
|---|---|
| 角色變臉 | 二 |
| 循環跳格 | 三 |
| 船槳或手變形 | 四 |
| 海鷗瞬移 | 五 |
| 鏡頭漂移 | 六 |
| 音效太吵 | 七 |
| 笑點不足 | 八 |
| 動作太亂 | 九 |
| 比例錯誤 | 十 |
| 紅點移動 | 十一 |

---

© 2026 S.A.D. — Sailor At Desk. X Shop Labs.
