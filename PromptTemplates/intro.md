# PromptTemplates

這個部分提供了不同類型的 prompt 模板，用作提問的範本。這些模板幫助詢問者擴展問題，並深入挖掘問題的核心。

## Prompt Type Template

這些模板用於引導和結構化您的 prompts，以便更精確地獲取所需信息。

### `analyze`: 分析型

用於要求深入分析一個主題或情境的 prompts。

```markdown
Template: "分析 [主題] 的主要因素，並提供對其影響的評估。"
```

### `game`: 遊玩型

```markdown
Template: "說明如何遊玩 [遊戲名稱]，包括基本規則和勝利條件。"
```

### `model`: 人物模組型

```markdown
Template: "構建一個名為 [角色名] 的角色模型，包括其背景故事、特點和動機。"
```

### `event`: 針對事件模型

```markdown
Template: "描述 [事件] 的發生過程，並分析其對 [相關人群/領域] 的影響。"
```

## Prompt Enhance

以下範本用於增強和豐富原有的 prompts。

### 指令強化型

```markdown
Template: "如何在 [情境] 中改進 [技術/策略]，並詳細說明其步驟和預期結果。"
```

### 多項合併型

```markdown
Template: "結合 [元素一] 和 [元素二]，創建一個新的概念，並說明其特性和創新點，並給出對比...。"
```

## How to make your prompt && make it better

提供指南和技巧，以幫助您構建更有效的 prompts。

```markdown
Template: "在創建 [類型] prompt 時，應考慮哪些關鍵要素？請列出並解釋這些要素如何影響 prompt 的效果。"
```

## Advanced Prompt Architecture

需有完整的結構 + 文體 + 語意 描述

```markdown

### Role:[給予模型核心名稱]

---
description: '可有可無' <- 描述模型功能，已供 LLM 理解
---

### background:[給予執行任務背景]

### steps|| flow :[模型步驟，最好是枚舉型，有思維鏈的]

### output:[可與給予 agent 輸出的指令，最好為限縮表達]

```

## Reference

請參閱以下資料以獲得更多有關 prompt 創建和優化的資訊：

John 大提供

- [ai-guide](https://ai-guide.future.mozilla.org/content/introduction/#if-youre-new-to-ai)
- [深度學習](https://zh.d2l.ai/index.html)
- [AGI 之路](https://waytoagi.feishu.cn/wiki/QPe5w5g7UisbEkkow8XcDmOpn8e)

@▢ － · － ▢ 提供

- [工程课程](https://learnprompting.org/zh-Hans/docs/trainable/discretized)
- [高效對話](https://gitlab.com/awesomeai/awesome-chatgpt-zh/-/blob/main/docs/ChatGPT_prompts.md)
- [學習 prompt](https://www.learnprompt.pro/docs/intro)
- [提示工程指南](https://www.promptingguide.ai/zh)

- [prompt store](https://promptport.ai/)
- [prompt agent store CN](https://aiweaver.feishu.cn/wiki/Nr20wfev0iH9oWkhxkVcFhQsn7g?table=tblIuot5sFDXcKqX&view=vewZgF9Ol5)


