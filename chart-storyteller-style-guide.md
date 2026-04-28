# 图表叙事家风格指南

## 使用方式

这个文件不是每次都要全读。

- 先在主入口文件中完成模块选择和版本判断
- 只有在风格已经确定后，再读取对应风格部分
- 不需要把四种风格全部塞进一次调用的上下文

## 用户可见风格说明

当需要让用户选择风格时，优先用下面这张表，而不是临场口头发挥：

| 风格名称 | 简介 | 适合场景 |
| --- | --- | --- |
| 简约现代 | 白色背景，黑白为主，黄色点缀，整体干净克制、留白更多 | 清爽传播、简洁展示 |
| 活泼明亮 | 颜色更鲜明，视觉更有冲击力，整体更有传播感 | 社媒传播、视觉吸引 |
| 深色科技 | 深色背景，高对比度，偏科技感和未来感 | 趋势主题、科技内容 |
| 学术论文 | 暖灰米色背景（#E6DDC8），更正式、更规整，像研究报告或论文图表页 | 评审展示、专业汇报 |

面向用户确认风格时，只使用中文风格名，不展示 `minimal`、`vibrant`、`dark`、`academic` 这些内部代号。

推荐配合密度选择一起询问：

- 标准版：5 个模块，信息更精炼，适合快速扫读和汇报
- 高密度版：8 个模块，信息更完整，适合一图读懂和传播展示

## 生图模型选择

在正式生图前，需要确认用户当前可用的生图模型或 API。推荐话术：

```text
如果你使用的是 Codex，默认推荐使用 Codex 内置生图能力（GPT Image 2 模型）；如果不是在 Codex 环境中使用，或你希望走外部服务，请提供你可用的生图模型或 API。
```

选择规则：

- 如果用户使用的是 Codex，默认推荐 Codex 内置生图能力（GPT Image 2 模型）
- 如果不是在 Codex 环境中使用，或用户希望走外部服务，则使用用户提供的生图模型或 API
- 如果用户提供多个选项，优先选择最适合中文信息图、文字清晰度和 3:4 竖版高清输出的方案

## 通用禁止项

无论使用哪种风格，都默认禁止以下元素：

- 平台 logo
- app UI 元素
- 水印式角标
- 社交媒体品牌标识
- 仿小红书、仿公众号、仿应用截图式装饰

如果需要传播感，应通过版式、节奏和视觉层级表达，而不是通过平台品牌元素表达。

## 通用字体规则

无论使用哪种风格，都默认约束中文字体为黑体风格：

- 优先使用黑体、苹方、思源黑体、Noto Sans CJK SC、SimHei、Heiti 等无衬线中文字体风格
- 避免宋体、仿宋、楷体、手写体、花体或装饰性字体
- 标题、主数字和标签都应保持清晰、稳重、可读，不要使用过度艺术化字形

---

## Minimal

### 核心锚点词

- Ultra-minimalist design
- Maximum white space
- Clean white background
- Black and white as primary colors
- Yellow (#F59E0B) as the ONLY accent color
- Organic, free-flowing layout
- No rigid grids or boxes

### 配色规则

- 背景：白色
- 主体：黑 / 白
- 强调：黄色，仅此一种

### 版式规则

- 保留留白
- 用自由流动而不是过重卡片框
- 适合优雅、克制、编辑感布局

### 禁忌词

- purple accent
- gradient-heavy
- neon
- playful
- cute
- dark background

### 常见跑偏

- 跑成杂志海报风，装饰过多
- 黄色不够克制，扩散到大面积背景
- 高密度时失去留白感

### 修正方法

- 重申 `yellow is the ONLY accent color`
- 强调 `no rigid grids or boxes`
- 强调 `maximum white space`

---

## Vibrant

### 核心锚点词

- Bright but professional
- Vivid magenta, deep violet, warm yellow
- Clean editorial hierarchy
- Serious, information-rich

### 配色规则

- 背景：浅色或干净明亮底
- 主体：紫 / 洋红 / 灰
- 强调：黄用于重点数据

### 版式规则

- 保持编辑感和传播感
- 适合高密度模块编排
- 明亮但不要幼稚

### 禁忌词

- kawaii
- cute stickers
- childish
- cartoon

### 常见跑偏

- 变成少女风
- 装饰元素太多
- 标题和数字抢层级

### 修正方法

- 强调 `professional, not playful`
- 保持 `strong editorial hierarchy`

---

## Dark

### 核心锚点词

- Deep dark background
- Neon cyan / electric purple / vivid magenta
- Futuristic but professional
- High contrast

### 配色规则

- 背景：深色
- 主体：深灰 / 黑
- 强调：霓虹青、紫、电光高亮

### 版式规则

- 模块分区清晰
- 发光强调只能用于重点
- 不要网格噪音太重

### 禁忌词

- flat pastel
- beige background
- cute
- soft handmade

### 常见跑偏

- 跑成廉价赛博风
- 背景纹理太重
- 小字发虚

### 修正方法

- 强调 `futuristic but professional`
- 强调 `clean modular separation`
- 控制 glow 只用于重点数字和图形

---

## Academic

### 核心锚点词

- Scholarly, professional style
- Clean and precise layout
- Background: warm gray-beige (#E6DDC8)
- Warm gray-beige paper tone
- Not pure white
- Primary: charcoal (#374151)
- Accent: burgundy (#9b2c2c) for important data only
- Formal presentation
- Precise alignment
- Section numbering

### 配色规则

- 背景：暖灰米色，接近 `#E6DDC8`，不要纯白
- 主体：炭黑 / 深灰
- 强调：酒红，仅用于重要数据

### 版式规则

- 更像论文图表页，而不是时尚海报
- 编号感、正式感、精确对齐
- 适合研究报告、论文解读

### 禁忌词

- fashion poster
- glossy
- neon
- playful
- colorful decoration

### 常见跑偏

- 跑成杂志风黑白红海报
- 酒红使用过多
- 背景太黄，变成复古纸张感
- 背景退回纯白，失去学术论文风格识别度

### 修正方法

- 重申 `burgundy for important data only`
- 重申 `formal presentation`
- 重申 `precise alignment`
- 重申 `warm gray-beige background, not pure white`
- 如果背景过暖，可把暖灰米色往更克制的米色收，但不要退回冷白

---

## 风格选择建议

- `minimal`：适合强调审美、克制和传播图感
- `vibrant`：适合强调视觉冲击和内容传播
- `dark`：适合科技、趋势、未来感主题
- `academic`：适合研究报告、论文解读、正式展示

---

## 测试建议

- 同一份报告至少做一次 `standard` 和 `dense` 对比
- 同一风格至少测试一次“趋势型报告”和一次“结构型报告”
- 如果风格不稳定，优先先修风格锚点词，再考虑参考图图生图
