# 图表叙事家风格指南

## 使用方式

这个文件不是每次都要全读。

- 先在主入口文件中完成模块选择和版本判断
- 只有在风格已经确定后，再读取对应风格部分
- 不需要把四种风格全部塞进一次调用的上下文

## 用户可见风格说明

当需要让用户选择风格时，优先用下面这张表，而不是临场口头发挥：

| 风格名称 | 风格代号 | 简介 | 适合场景 |
| --- | --- | --- | --- |
| 简约现代 | minimal | 白色背景，黑白为主，黄色点缀，整体干净克制、留白更多 | 清爽传播、简洁展示 |
| 活泼明亮 | vibrant | 颜色更鲜明，视觉更有冲击力，整体更有传播感 | 社媒传播、视觉吸引 |
| 深色科技 | dark | 深色背景，高对比度，偏科技感和未来感 | 趋势主题、科技内容 |
| 学术论文 | academic | 更正式、更规整，像研究报告或论文图表页 | 评审展示、专业汇报 |

推荐配合密度选择一起询问：

- 标准版：信息更精炼，适合快速理解
- 高密度版：信息更丰富，适合完整展示

## 通用禁止项

无论使用哪种风格，都默认禁止以下元素：

- 平台 logo
- app UI 元素
- 水印式角标
- 社交媒体品牌标识
- 仿小红书、仿公众号、仿应用截图式装饰

如果需要传播感，应通过版式、节奏和视觉层级表达，而不是通过平台品牌元素表达。

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
- Background: cream (#fffef7)
- Primary: charcoal (#374151)
- Accent: burgundy (#9b2c2c) for important data only
- Formal presentation
- Precise alignment
- Section numbering

### 配色规则

- 背景：浅米白 / 奶油白
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

### 修正方法

- 重申 `burgundy for important data only`
- 重申 `formal presentation`
- 重申 `precise alignment`
- 如果背景过暖，可把 cream 往更冷的浅色收

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
