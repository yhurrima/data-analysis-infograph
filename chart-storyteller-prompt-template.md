# 图表叙事家 Prompt 模板

## 使用原则

- 不固定模块名字和数量
- 先确定版本：`standard` 或 `dense`
- 再把入选模块按顺序填入 Prompt
- 只描述本次真正存在的数据内容
- 先结构化，再写视觉 prompt
- 模块内容尽量字段化，避免正文被模型误判成副标题
- 只有在报告内容、输出密度、目标风格三项都确认后，才进入 prompt 编写
- 默认生成配置：`wan2.7-image-pro` + `1774*2364`（3:4 竖版）

---

## Prompt 模板

```text
Create a narrative data infographic poster for mobile-friendly vertical reading.

=== CORE REQUIREMENTS ===

【OUTPUT MODE】
- Edition: [standard or dense]
- If edition is standard: use exactly 5 modules
- If edition is dense: use exactly 8 modules
- Keep all modules clearly separated with strong editorial hierarchy

【VISUAL GOAL】
- Transform a report into a readable visual story
- Prioritize clear reasoning, insight flow, and data-backed storytelling
- Make the poster feel like an executive summary plus a clean social-friendly infographic

【STYLE】
- Visual style: [minimal / vibrant / dark / academic]
- Portrait ratio: 3:4
- Clear Chinese typography
- Strong contrast for titles, key numbers, and labels

【LAYOUT】
- Top area: title + subtitle + report context
- Middle area: selected modules arranged in a clean reading flow
- Bottom area: takeaway + source
- Keep enough spacing between text and graphic elements

【TEXT SAFETY】
- No overlapping labels
- No text directly on bars or charts
- Keep all text inside its own visual section
- Use short phrases instead of long paragraphs
- Each module should have only one visible title
- Do not create extra sub-headings inside a module
- Do not include any platform logo
- Do not include app UI elements
- Do not include watermark-like badges
- Do not include Xiaohongshu branding or social media brand marks

【NARRATIVE STRUCTURE】
- Always include:
  1. 报告速览
  2. 核心发现
  3. 一句话结论
- Also include these selected dynamic modules:
  [模块A]
  [模块B]
  [模块C]
  [模块D]
  [模块E]

【MODULE CONTENT】
Main Title: [报告标题]
Sub Title: [核心洞察一句话]
Report Period: [时间范围]
Source: [数据来源]

Module 1 [报告速览]:
- 主题: [主题]
- 研究对象: [对象]
- 关键词: [标签1] / [标签2] / [标签3]
- 核心指标概览: [指标概览]

Module 2 [核心发现]:
- 主数字: [核心数字]
- 变化标签: [趋势值]
- 短结论: [主结论]
- 补充说明: [支持句]
- 对比说明: [对比句]

Module 3 [[动态模块名称]]:
- 数据项: [仅填该模块真实存在的数据]
- 结论项: [仅填该模块真实存在的结论]
- 推荐图形: [bar / line / pie / cards / flow / matrix]
- 洞察: [对应洞察]

Module 4 [[动态模块名称]]:
- 数据项: [仅填该模块真实存在的数据]
- 结论项: [仅填该模块真实存在的结论]
- 推荐图形: [bar / line / pie / cards / flow / matrix]
- 洞察: [对应洞察]

Module 5 [[动态模块名称]]:
- 数据项: [仅填该模块真实存在的数据]
- 结论项: [仅填该模块真实存在的结论]
- 推荐图形: [bar / line / pie / cards / flow / matrix]
- 洞察: [对应洞察]

Module 6 [[动态模块名称]]:
- 数据项: [仅在 dense 版本启用]
- 结论项: [仅在 dense 版本启用]
- 推荐图形: [bar / line / pie / cards / flow / matrix]
- 洞察: [对应洞察]

Module 7 [[动态模块名称]]:
- 数据项: [仅在 dense 版本启用]
- 结论项: [仅在 dense 版本启用]
- 推荐图形: [bar / line / pie / cards / flow / matrix]
- 洞察: [对应洞察]

Module 8 [一句话结论]:
- 总结: [总结一句话]
- 数据来源: [来源]

【IMPORTANT】
- Do not force a structure comparison module if the report has no distribution data
- Do not force ranking if the report has no ranking evidence
- If the report is qualitative, prefer insight cards, causal analysis, and action recommendations
- Every module must be grounded in actual report content
- Do not add platform branding, app logos, UI chrome, or social-media watermarks
```

---

## 字段化写法建议

为了提升中文信息图的结构稳定性，以下写法优先级更高：

推荐：

```text
Module 2 [核心发现]:
- 主数字: 768.0万对
- 变化标签: +12.4%
- 短结论: 2023年结婚登记止跌回升
- 补充说明: 结束连续多年下滑趋势
```

不推荐：

```text
Module 2 [核心发现]:
- 2023年结婚登记 768.0万对，同比增长12.4%
```

原因：

- 推荐写法更容易让模型区分“标题 / 数字 / 正文”
- 不推荐写法容易触发“2023年结婚登记”被误当成副标题

---

## 标题安全规则

写 prompt 时建议显式加入类似约束：

```text
- Each module can have only one visible title
- Do not create secondary headings
- Do not convert body text into a new title
```

尤其是以下模块最容易出问题：

- `核心发现`
- `区域对比`
- `一句话结论`

这些模块中，正文的第一句必须避免长得像一个标题。

---

## 模块名建议映射

| 模块名 | 推荐图形 |
|-------|---------|
| 趋势分析 | line / area |
| 结构对比 | pie / ring / stacked bar |
| 排名洞察 | horizontal bar |
| 关键指标卡片 | cards |
| 用户画像 | cards / matrix / icon clusters |
| 流程拆解 | flow / funnel |
| 原因归因 | causal diagram / matrix |
| 行动建议 | cards / checklist blocks |

---

## 版本化填充示例

### 标准版

```text
Selected dynamic modules:
- 趋势分析
- 关键指标卡片

最终模块顺序：

1. 报告速览
2. 核心发现
3. 趋势分析
4. 关键指标卡片
5. 一句话结论
```

### 高密度版

```text
Selected dynamic modules:
- 趋势分析
- 结构对比
- 排名洞察
- 关键指标卡片
- 行动建议

最终模块顺序：

1. 报告速览
2. 核心发现
3. 趋势分析
4. 结构对比
5. 排名洞察
6. 关键指标卡片
7. 行动建议
8. 一句话结论
```
