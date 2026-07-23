# 雙語文件規範｜Bilingual Documentation Standard

## 目的｜Purpose

本倉庫以繁體中文與英文雙語維護，讓中文使用者可以直接操作，也讓國際讀者能理解工作流程、提示詞結構與社群應用方式。

This repository is maintained in both Traditional Chinese and English so that Chinese-speaking users can follow the workflow directly while international readers can understand the prompt structure, production process, and social-media applications.

## 文件原則｜Documentation Rules

1. 主要標題必須中英文並列。  
   Primary headings must be shown in both Chinese and English.
2. 每段重要中文說明後應提供英文對照。  
   Every important Chinese explanation should be followed by an English equivalent.
3. 表格欄位應使用雙語標題。  
   Table headers should be bilingual.
4. 技術名稱、模型名稱與檔案路徑保留原文。  
   Technical names, model names, and file paths should remain in their original form.
5. 生成模型使用的正式 Prompt 可優先採英文，以提高模型理解穩定性。  
   Production prompts may be written primarily in English to improve model reliability.
6. 英文 Prompt 前後必須附中文用途、參數與操作說明。  
   English prompts must be accompanied by Chinese usage notes, parameters, and operating instructions.
7. 範例文件必須同時說明正常速度與加速後的幽默效果。  
   Example files must explain both the normal-speed behavior and the accelerated comedy payoff.

## 建議格式｜Recommended Format

```markdown
## 場景設定｜Scene Setup

中文說明。

English explanation.
```

## 提示詞與音訊｜Prompts and Audio

提示詞中的動作、鏡頭、物理與負面限制建議使用英文；聲音設計則同時列出中文名稱與英文生成描述。

Motion, camera, physics, and negative constraints should preferably be written in English. Sound design should list both the Chinese sound name and the English generation description.

範例｜Example:

```yaml
audio:
  zh-TW:
    - 海浪聲
    - 遠近交錯的海鷗叫聲
    - 船槳與船身的木頭摩擦聲
  en:
    - gentle ocean waves
    - near and distant seagull calls
    - rhythmic wooden oarlock and hull creaks
```

## 維護要求｜Maintenance Requirement

新增或修改主要文件時，應同步更新中英文內容，避免兩種語言版本出現規格不一致。

Whenever primary documentation is added or changed, both language sections should be updated together to prevent specification drift.