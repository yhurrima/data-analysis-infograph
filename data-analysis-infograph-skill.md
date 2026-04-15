---
name: 数据分析信息图生成器
description: 从分析报告中自动提取关键数据和洞察，生成包含多种图表和说明文字的信息图，帮助用户快速理解报告核心内容，适合报告解读、数据传播、小红书分享等场景。
---

# 数据分析信息图生成器

## 1. 作品名称

**数据分析信息图生成器**

英文名：**Data Infographic Generator**

---

## 2. 作品简介

这是一个围绕 **"报告数据可视化"** 设计的 Wan Skill。  
用户上传分析报告后，Skill 会自动完成以下工作：

- 智能识别报告中的关键数据点
- 提取适合可视化的指标和对比关系
- 设计信息图布局（多图表 + 文字说明）
- 生成一张高密度信息图

这个 Skill 的核心不是"把数据画成图表"，而是：
- **自动发现**报告中值得可视化的内容
- **智能编排**多个图表和说明文字
- **一键生成**可直接用于汇报、分享、传播的信息图

它不是一个单纯的“图表海报生成器”，而是一套把报告内容转译成 **可读、可讲、可传播** 数据故事的自动化可视化流程。

---

## 3. 解决什么问题 / 面向什么场景

### 解决的问题

很多分析师、运营、产品经理有以下真实需求：

- 写了分析报告，但领导/客户没时间细读
- 想把报告精华分享到社交媒体，但缺少视觉化内容
- 需要做汇报PPT，但来不及一个个画图表
- 报告里的数据很好，但文字形式不够直观
- 想做一图读懂，但不会设计信息图

这个 Skill 解决的不是单纯"画图表"，而是 **从报告到信息图的自动化转化** 问题。

### 面向的场景

- 业务分析报告解读
- 用户研究/市场调研报告
- 季度/年度总结汇报
- 竞品分析报告
- 产品数据分析报告
- 小红书/公众号数据内容创作
- 会议汇报一图总结

### 为什么它比普通图表生成更有价值

- 它 **自动发现**报告中的关键数据，不需要用户手动提取
- 它生成的是 **多图表信息图**，不是单一图表
- 它包含 **文字说明和洞察**，不只是数据可视化
- 它适合 **社交传播和汇报展示**，商业价值明确

---

## 4. 核心创意与评审亮点

### 亮点 1：智能数据发现

Skill 不只是"画图表"，而是先：

- 识别报告中的数值、百分比、趋势、对比
- 判断哪些数据适合用柱状图、饼图、折线图、流程图
- 提取数据的业务含义和洞察结论

### 亮点 2：多图表编排

一张信息图通常包含：

- 1-2个核心图表（主视觉）
- 2-4个辅助图表（补充说明）
- 关键数字/指标卡片
- 简短的洞察说明文字
- 报告标题和来源标注

### 亮点 3：洞察驱动设计

不只是展示数据，而是：

- 突出关键发现（Key Findings）
- 标注数据变化趋势
- 添加对比基准线
- 用颜色区分正负向指标

### 亮点 4：可商品化

它可以扩展为：

- 企业报告自动化服务
- 数据分析师效率工具
- 内容创作者数据可视化工具
- 咨询公司交付物标准化

### 亮点 5：双阶段生成，兼顾准确性与美感

这个 Skill 不是把整份报告直接交给模型“自由发挥”，而是先做：

- 结构化数据提取
- 图表类型决策
- 信息层级编排
- 关键信息压缩

再进入 Wan 生图。

这让它相比“直接生成一张信息图”更有产品感，也更容易控制：

- 数据准确性
- 阅读顺序
- 信息密度
- 文字可读性

### 亮点 6：同时适合汇报和传播

大多数图表工具偏内部汇报，大多数视觉海报工具偏社交传播。

这个 Skill 的优势在于它同时服务两类场景：

- 对内：会议汇报、管理层扫读、一图读懂
- 对外：小红书、公众号、行业内容传播

因此它既是效率工具，也是内容工具。

---

## 5. 核心调用逻辑

Skill 的调用闭环为：

`用户输入报告 -> 数据提取与结构化 -> 中间方案生成 -> 图表类型决策 -> 布局编排 -> Prompt构建 -> Wan生图 -> 质量校验 -> 信息图交付`

### 步骤 1：收集输入

必须询问并确认以下内容：

1. **分析报告内容**（文本/PDF/链接）
2. **风格偏好**（必选）
   - 简约现代（黑白+黄）
   - 活泼明亮（紫+玫红+黄）
   - 深色科技（霓虹青+紫）
   - 学术论文（米白+墨黑）
3. **重点方向**（可选）
   - 突出趋势变化
   - 突出对比分析
   - 突出关键指标
   - 突出用户画像

**默认配置：**
- 模型：wan2.7-image-pro
- 分辨率：4K (1774×2364，3:4比例)

### 步骤 2：数据提取与结构化

从报告中提取：

| 数据类型 | 示例 | 适合图表 |
|---------|------|---------|
| 数值对比 | A产品销量100万，B产品80万 | 柱状图 |
| 占比分布 | 60%用户来自一线城市 | 饼图/环形图 |
| 时间趋势 | Q1到Q4增长率分别为5%、8%、12%、15% | 折线图/面积图 |
| 排名列表 | TOP5城市：北京、上海、广州、深圳、杭州 | 横向柱状图 |
| 流程步骤 | 用户从了解到购买的5个阶段 | 流程图 |
| 关键指标 | DAU 100万，留存率45%，转化率3.2% | 指标卡片 |
| 对比分析 | 同比增长20%，环比下降5% | 对比图 |

### 步骤 3：图表类型决策

根据数据特征选择合适的可视化方式：

```
数据特征判断逻辑：

IF 数据是"部分占整体的比例" 
THEN 使用饼图/环形图

IF 数据是"不同类别的数值对比" 
THEN 使用柱状图/条形图

IF 数据是"时间序列的变化" 
THEN 使用折线图/面积图

IF 数据是"关键指标展示" 
THEN 使用数字卡片

IF 数据是"流程或步骤" 
THEN 使用流程图/路径图

IF 数据是"多维度对比" 
THEN 使用雷达图/矩阵图
```

### 步骤 4：信息图布局编排

标准信息图布局：

```
┌─────────────────────────────────────┐
│           报告标题 + 核心洞察          │
├─────────────────────────────────────┤
│                                     │
│      ┌─────────┐    ┌─────────┐    │
│      │ 主图表1  │    │ 主图表2  │    │
│      │ (柱状图) │    │ (饼图)  │    │
│      └─────────┘    └─────────┘    │
│                                     │
│  ┌──────┐ ┌──────┐ ┌──────┐ ┌──────┐│
│  │指标1 │ │指标2 │ │指标3 │ │指标4 ││
│  │ 100万│ │ 45% │ │ +20% │ │ TOP1 ││
│  └──────┘ └──────┘ └──────┘ └──────┘│
│                                     │
│  ┌─────────────────────────────┐   │
│  │ 趋势折线图 + 关键洞察说明     │   │
│  └─────────────────────────────┘   │
│                                     │
│  数据来源：XXX报告  时间：2026年Q1   │
└─────────────────────────────────────┘
```

### 步骤 5：Prompt 构建

将结构化数据转换为 Wan 可理解的 Prompt。

### 步骤 6：调用 Wan 生图

使用 wan2.7-image-skill 生成信息图。

### 步骤 7：质量校验

输出后检查：

- 标题、数字、标签是否清晰
- 关键数据是否与原文一致
- 是否出现文字溢出或图表拥挤
- 信息层级是否清楚
- 是否符合目标用途（汇报 / 社媒 / 一图读懂）

如发现问题，优先执行两类修正：

- 降低信息密度，减少模块或压缩说明文字
- 增加轻量约束，限制文字停留在各自区域内

### 步骤 8：交付成品

输出文件：
- `infographic.png`（信息图）
- `infographic_brief.md`（结构化摘要，可选）

---

## 6. 使用到的 Wan 能力

| Wan 能力 | 在本 Skill 中的作用 |
|------|------|
| 文本生成图像 | 根据结构化 Prompt 生成信息图 |
| 中文语义理解 | 理解报告内容、数据含义、业务洞察 |
| 信息图生成 | 支持多图表布局、数据可视化风格 |
| 风格化生成 | 支持简约、活泼、深色、学术等风格 |
| 文字渲染 | 在图中准确显示数字、标签、说明文字 |

### 本 Skill 对 Wan 的使用价值

这个 Skill 不是把 Wan 当成"单次图片生成器"，而是把它作为：

- 数据报告的视觉化引擎
- 从文字到信息图的自动化工具
- 分析师效率提升的关键能力

---

## 7. Prompt / 工作流 / 配置说明

### 7.1 用户输入项

用户必须提供：

- 分析报告内容（文本）
- 风格偏好（必选：简约现代/活泼明亮/深色科技/学术论文）

用户可选提供：

- 重点方向

**默认配置（无需用户选择）：**
- 模型：wan2.7-image-pro
- 分辨率：4K (1774×2364，3:4比例)

### 7.2 信息图风格配置

用户可选择以下风格，每种风格有不同的视觉特点和适用场景：

| 风格 ID | 风格名称 | 视觉特点 | 适用场景 | Prompt 特点 |
|--------|---------|---------|---------|------------|
| `minimal` | 简约现代 | 黑白为主、黄色强调、极简留白 | 小红书、社交媒体 | 黑白+黄配色，强调留白和优雅 |
| `vibrant` | 活泼明亮 | 明亮配色、专业严肃、无装饰 | 年轻受众、科普内容 | 紫+玫红+黄配色，去掉幼稚元素 |
| `dark` | 深色科技 | 纯色深色背景、霓虹色、未来感 | 科技公司、产品发布 | 纯色背景无网格，霓虹配色 |
| `academic` | 学术论文 | 米白底色、墨黑线条、严谨感 | 研究报告、论文解读 | 强调学术规范和数据精确 |

### 7.2.1 中间结构化方案

为了提高稳定性，建议在正式生图前先生成一个“中间信息图方案”，至少包含：

- 报告标题
- 核心洞察一句话
- 主图表列表
- 辅助图表列表
- 关键指标卡片
- 数据来源
- 推荐风格

推荐格式：

```yaml
title: 2026年Q1用户增长分析
core_insight: 用户增长势头良好，留存率持续提升
main_charts:
  - type: line
    title: 用户增长趋势
  - type: pie
    title: 用户城市分布
supporting_blocks:
  - type: metric
    label: DAU
    value: 150万
  - type: metric
    label: 留存率
    value: 45%
source: 2026年Q1增长分析报告
style: business
```

这个中间层的价值在于：

- 让工作流不再是黑盒
- 便于人工复核数据
- 更适合作为比赛中的产品逻辑展示

#### 风格 1：简约现代（minimal）

**特点**：极简设计，黑白为主，黄色强调，大量留白

```text
Create a minimal modern data infographic.

【STYLE】
- Ultra-minimalist design
- Portrait 3:4 ratio
- Maximum white space
- Clean and elegant

【COLOR】
- Clean white background
- Black and white as primary colors
- Yellow (#F59E0B) as the ONLY accent color for highlights
- Minimal color palette (black, white, yellow only)

【LAYOUT】
- Organic, free-flowing layout
- No rigid grids or boxes
- Elegant spacing between elements

【CONTENT】
[数据内容]
```

#### 风格 2：活泼明亮（vibrant）

**特点**：明亮配色但专业严肃，紫色、玫红色、黄色和灰色配色，去掉装饰元素

```text
Create a bright and professional data infographic.

【STYLE】
- Bright, colorful but PROFESSIONAL
- Portrait 3:4 ratio
- Modern and clean, NOT childish

【COLOR - LIMITED PALETTE】
- Background: white ONLY
- Primary: purple (#8B5CF6) for main data
- Secondary: pink/magenta (#EC4899) for highlights  
- Accent: yellow (#F59E0B) for key numbers
- Neutral: gray (#6B7280) for supporting text
- NO more than 4 colors total
- NO pastel colors, NO gradients

【IMPORTANT - NO DECORATIONS】
- NO flowers, butterflies, ribbons, cute icons
- NO decorative borders or frames
- NO childish elements
- Keep it PROFESSIONAL and SERIOUS
- Focus on DATA, not decoration

【CHART STYLE】
- Clean, flat design charts
- Solid colors only (no gradients)
- Straight lines (no rounded corners)
- Professional typography

【CONTENT】
[数据内容]
```

#### 风格 3：深色科技（dark）

**特点**：纯色深色背景，无网格无装饰，霓虹配色，未来感强

```text
Create a dark mode tech-style data infographic.

【STYLE】
- Futuristic tech aesthetic
- Portrait 3:4 ratio
- Pure solid dark background, NO grid, NO patterns

【COLOR】
- Background: solid dark navy (#0f172a), NO gradients, NO textures
- Primary: cyan (#06b6d4)
- Secondary: purple (#8b5cf6)
- Subtle glow effects on key elements

【IMPORTANT - NO DECORATIONS】
- NO grid patterns
- NO background textures
- NO decorative borders or frames
- Keep it CLEAN and MINIMAL
- Focus on DATA, not decoration

【CONTENT】
[数据内容]
```

#### 风格 4：学术论文（academic）

**特点**：严谨、规范，适合研究报告

```text
Create an academic-style data infographic.

【STYLE】
- Scholarly, professional style
- Portrait 3:4 ratio
- Clean and precise layout

【COLOR】
- Background: cream (#fffef7)
- Primary: charcoal (#374151)
- Accent: burgundy (#9b2c2c) for important data only

【LAYOUT】
- Section numbering (1. 2. 3.)
- Formal presentation
- Precise alignment

【CONTENT】
[数据内容]
```

### 7.3 信息图尺寸配置

**默认配置：4K分辨率**

| 比例 ID | 比例名称 | 尺寸（4K） | 用途 |
|--------|---------|------|------|
| `v_3_4` | 竖屏 3:4 | `1774*2364` | 小红书封面、手机阅读（默认） |
| `v_9_16` | 竖屏 9:16 | `1774*3157` | 手机锁屏、竖屏传播 |
| `h_4_3` | 横屏 4:3 | `2364*1774` | PPT嵌入、汇报展示 |
| `h_16_9` | 横屏 16:9 | `3157*1774` | 宽屏展示、视频封面 |

### 7.5 信息图 Prompt 模板（丰富版）

**核心原则**：参考论文解读图的多模块结构，确保高信息密度和视觉丰富度。

**⚠️ 信息密度要求**：
- 一张图必须包含 **6-7 个核心模块**
- 每个模块必须包含**具体数据、指标名称、趋势箭头、对比结论**
- 画面整体应像一张**数据报告解读总览图**

```text
Create a high-density data infographic poster for Xiaohongshu (Little Red Book).

=== CRITICAL STYLE REQUIREMENTS ===

【OVERALL VISUAL CONCEPT】
- A one-page data report infographic
- High information density with 6-7 clearly separated modules
- Designed to help readers understand the report's key findings, trends, comparisons, and insights at a glance
- Strong editorial hierarchy, clear reading flow

【COLOR SYSTEM】
- Background: [根据风格配置]
- Primary structure color: [根据风格配置]
- Highlight color: [根据风格配置] for key numbers and trends

【LAYOUT & STRUCTURE】
- Portrait ratio: 3:4, optimized for Xiaohongshu
- Top area: Report title, time period, core insight banner
- Middle area: 4-5 structured modules with clear content zones
- Bottom area: Key takeaway and data source
- Reading flow: highly structured, like a visual executive summary

【GRAPHIC ELEMENTS - 必须包含】
- Report title block with time period
- Keyword tags for report theme
- Trend arrows (↑↓) and percentage indicators
- Bar charts and comparison bars
- Pie/ring charts for distributions
- Metric cards with trend indicators
- Ranking lists with visual bars
- Insight callout boxes
- Summary strip

【CHART LAYOUT - 图表元素布局约束】
- Bar charts: Labels placed ABOVE or BELOW bars, NOT overlapping with bars
- Bar width: Leave sufficient gap between bars (at least 20% of bar width)
- Data labels: Position clearly outside/beside visual elements
- Text blocks: Use clear bounding boxes or separate zones
- Pie/Ring charts: Labels positioned outside the chart with connecting lines
- Ranking bars: Text on the left side, bar on the right side, clearly separated
- Metric cards: Number centered, label below, adequate padding
- Trend arrows: Placed next to numbers with visible spacing

【IMPORTANT - AVOID OVERLAP】
- NO overlapping text on chart elements
- NO labels directly on top of bars or lines
- All text must be clearly readable without interference
- Maintain minimum spacing between all visual elements

【MODULE REQUIREMENTS - 7模块结构】
- Module 1【报告速览】: Report title, time period, theme tags, key numbers overview
- Module 2【核心发现】: The most important finding with supporting data
- Module 3【趋势分析】: Time-series trends with arrows showing direction
- Module 4【结构对比】: Distribution or comparison across categories
- Module 5【排名洞察】: Top performers or rankings with visual bars
- Module 6【关键指标】: 3-4 metric cards with values and trend arrows
- Module 7【一句话结论】: One-sentence takeaway and data source

【TYPOGRAPHY STYLE】
- Bold Chinese typography for titles
- Numbers and percentages should be LARGE and prominent
- Trend arrows (↑↓) clearly visible next to metrics
- Short insight text in smaller font under charts

【WHAT TO AVOID】
- No cute or playful style
- No excessive empty space
- No vague summaries without concrete data

【CONTENT FOR THIS IMAGE】

Main Title: [报告标题] 一图看懂
Sub Title: [核心洞察一句话]

Module 1 [报告速览]:
- 报告主题: [主题]
- 时间范围: [时间]
- 核心指标: [指标1]、[指标2]、[指标3]

Module 2 [核心发现]:
- 发现: [关键发现描述]
- 数据支撑: [具体数据]
- 趋势方向: ↑增长/↓下降

Module 3 [趋势分析]:
- [时间点1]: [数值1]
- [时间点2]: [数值2]
- [时间点3]: [数值3]
- 趋势洞察: [趋势结论]

Module 4 [结构对比]:
- [类别1]: [数值/占比]
- [类别2]: [数值/占比]
- [类别3]: [数值/占比]
- 对比洞察: [对比结论]

Module 5 [排名洞察]:
- TOP1: [名称] ([数值])
- TOP2: [名称] ([数值])
- TOP3: [名称] ([数值])
- 排名洞察: [排名结论]

Module 6 [关键指标卡片]:
- [指标1]: [数值] ↑[变化]
- [指标2]: [数值] ↓[变化]
- [指标3]: [数值] —[变化]
- [指标4]: [数值] ↑[变化]

Module 7 [一句话结论]:
- 核心结论: [总结一句话]
- 数据来源: [来源]
```

### 7.6 文字约束技巧（轻量版）

如果出现文字溢出问题，只需在一处添加轻量提醒：

```text
【TIP】Keep all text within its visual section, use line breaks if needed.
```

**不要添加过多约束**，如：
- ❌ 强制方框边界
- ❌ 固定内边距数值
- ❌ 严格的区块比例
- ❌ 布局验证清单

这些过度约束会破坏视觉美感。

### 7.6.1 质量优先重试策略

如果首轮输出存在问题，建议按以下顺序重试：

1. 降低信息密度  
   从 `6-7 个模块` 降到 `4-5 个模块`

2. 切换到更稳的风格  
   优先使用 `business` 或 `academic`

3. 增加轻量文字约束  
   只补充一句：

```text
Each text block must stay inside its own section and remain short and readable.
```

4. 拆分复杂内容  
   把流程图或复杂对比表拆到第二张图，不强塞进一张图里

### 7.7 工作流总结

```text
报告输入
-> 数据提取与结构化
-> 用户选择风格（必选）
-> 构建Prompt
-> Wan生图（默认：wan2.7-image-pro，4K分辨率）
-> 检查效果（如有文字溢出，加轻量约束重试）
-> 下载交付
```

**默认配置：**
- 模型：`wan2.7-image-pro`
- 分辨率：`4K` (1774×2364，3:4比例)

---

## 8. 如有代码，请附关键代码或仓库说明

### 关键代码说明

这个 Skill 的关键代码主要分五部分：

1. **数据提取模块**  
   从报告中提取数值、百分比、趋势、对比等数据

2. **图表决策模块**  
   根据数据特征判断最适合的可视化类型

3. **Prompt 编排模块**  
   将结构化数据转换为 Wan 可理解的 Prompt

4. **Wan 调用模块**  
   调用 wan2.7-image-skill 生成信息图

5. **质量校验模块**  
   检查结果是否存在文字拥挤、数据遗漏、层级混乱等问题

### 关键代码示例

```python
#!/usr/bin/env python3
"""
数据分析信息图生成器
依赖：wan2.7-image-skill
"""

import os
import re
import subprocess
import requests
from dataclasses import dataclass
from typing import List, Optional
from enum import Enum


class ChartType(Enum):
    """图表类型枚举"""
    BAR = "柱状图"
    PIE = "饼图"
    LINE = "折线图"
    CARD = "指标卡片"
    FLOW = "流程图"
    RADAR = "雷达图"
    TABLE = "表格"


class StyleType(Enum):
    """信息图风格枚举"""
    MINIMAL = "简约现代"
    VIBRANT = "活泼明亮"
    DARK = "深色科技"
    ACADEMIC = "学术论文"


@dataclass
class DataPoint:
    """数据点结构"""
    name: str
    value: float
    unit: Optional[str] = None
    trend: Optional[str] = None  # "up", "down", "stable"
    comparison: Optional[str] = None  # 同比/环比变化


@dataclass
class Chart:
    """图表结构"""
    chart_type: ChartType
    title: str
    data_points: List[DataPoint]
    insight: Optional[str] = None


@dataclass
class InfographicModule:
    """信息图模块结构"""
    module_type: str  # 报告速览、核心发现、趋势分析、结构对比、排名洞察、关键指标、一句话结论
    title: str
    content: str
    data_items: List[str] = None
    insight: str = None


@dataclass
class InfographicLayout:
    """信息图布局（丰富版）"""
    title: str
    subtitle: str
    modules: List[InfographicModule]  # 6-7个模块
    data_source: str = None
    time_period: str = None


class DataExtractor:
    """数据提取器"""
    
    # 匹配数字和百分比的正则
    NUMBER_PATTERN = r'(\d+(?:\.\d+)?)\s*([%万亿千百]?)'
    PERCENTAGE_PATTERN = r'(\d+(?:\.\d+)?)\s*%'
    TREND_PATTERN = r'(同比增长?|环比增长?|增长?|下降?|提升?|降低?)\s*(\d+(?:\.\d+)?)\s*[%百分点]?'
    
    def extract_from_report(self, report_text: str) -> List[DataPoint]:
        """从报告中提取数据点"""
        data_points = []
        
        # 提取百分比数据
        for match in re.finditer(self.PERCENTAGE_PATTERN, report_text):
            value = float(match.group(1))
            # 尝试获取上下文作为名称
            context = self._get_context(report_text, match.start(), 50)
            name = self._extract_name_from_context(context)
            data_points.append(DataPoint(name=name, value=value, unit="%"))
        
        # 提取趋势数据
        for match in re.finditer(self.TREND_PATTERN, report_text):
            direction = "up" if "增长" in match.group(1) or "提升" in match.group(1) else "down"
            value = float(match.group(2))
            context = self._get_context(report_text, match.start(), 30)
            name = self._extract_name_from_context(context)
            data_points.append(DataPoint(
                name=name, 
                value=value, 
                unit="%",
                trend=direction,
                comparison=match.group(1)
            ))
        
        return data_points
    
    def _get_context(self, text: str, pos: int, length: int) -> str:
        """获取指定位置周围的上下文"""
        start = max(0, pos - length)
        end = min(len(text), pos + length)
        return text[start:end]
    
    def _extract_name_from_context(self, context: str) -> str:
        """从上下文中提取指标名称"""
        # 简化实现，实际可用NLP
        keywords = ["用户", "销量", "收入", "增长", "转化率", "留存率", 
                   "DAU", "MAU", "GMV", "占比", "份额"]
        for kw in keywords:
            if kw in context:
                return kw
        return "指标"


class ChartDecider:
    """图表类型决策器"""
    
    def decide_chart_type(self, data_points: List[DataPoint]) -> ChartType:
        """根据数据特征决定图表类型"""
        if not data_points:
            return ChartType.CARD
        
        # 检查是否是占比数据（所有值加起来接近100）
        total = sum(dp.value for dp in data_points if dp.unit == "%")
        if 95 <= total <= 105 and len(data_points) <= 6:
            return ChartType.PIE
        
        # 检查是否有趋势信息
        if any(dp.trend for dp in data_points):
            return ChartType.LINE
        
        # 检查数据点数量
        if len(data_points) <= 4:
            return ChartType.CARD
        elif len(data_points) <= 10:
            return ChartType.BAR
        else:
            return ChartType.TABLE


class PromptBuilder:
    """Prompt构建器（丰富版）"""
    
    # 默认模型和分辨率配置
    DEFAULT_MODEL = "wan2.7-image-pro"
    DEFAULT_SIZE = "1774*2364"  # 4K 3:4
    
    STYLE_CONFIGS = {
        StyleType.MINIMAL: {
            "background": "pure white (#FFFFFF)",
            "primary_color": "black and white",
            "accent_color": "yellow (#F59E0B)",
            "description": "minimal, elegant, black-white-yellow"
        },
        StyleType.VIBRANT: {
            "background": "white",
            "primary_color": "purple (#8B5CF6)",
            "accent_color": "pink/magenta (#EC4899)",
            "highlight_color": "yellow (#F59E0B)",
            "description": "bright, colorful but professional"
        },
        StyleType.DARK: {
            "background": "dark navy (#0f172a)",
            "primary_color": "cyan (#06b6d4)",
            "accent_color": "purple (#8b5cf6)",
            "description": "dark mode, neon, futuristic"
        },
        StyleType.ACADEMIC: {
            "background": "cream (#fffef7)",
            "primary_color": "charcoal (#374151)",
            "accent_color": "burgundy (#9b2c2c)",
            "description": "scholarly, classic, refined"
        }
    }
    
    def build_prompt(self, layout: InfographicLayout, style: StyleType, ratio: str) -> str:
        """构建完整的生图Prompt（丰富版）"""
        style_config = self.STYLE_CONFIGS[style]
        
        prompt = f"""Create a high-density data infographic poster for Xiaohongshu (Little Red Book).

=== CRITICAL STYLE REQUIREMENTS ===

【OVERALL VISUAL CONCEPT】
- A one-page data report infographic
- High information density with 6-7 clearly separated modules
- {style_config['description']} visual style
- Strong editorial hierarchy, clear reading flow

【COLOR SYSTEM】
- Background: {style_config['background']}
- Primary structure color: {style_config['primary_color']}
- Highlight color: {style_config['accent_color']} for key numbers and trends

【LAYOUT & STRUCTURE】
- Portrait ratio: {ratio}
- Top area: Report title "{layout.title}", subtitle "{layout.subtitle}"
- Middle area: 4-5 structured modules with clear content zones
- Bottom area: Key takeaway and data source

【GRAPHIC ELEMENTS - 必须包含】
- Report title block with time period
- Keyword tags for report theme
- Trend arrows (↑↓) and percentage indicators
- Bar charts and comparison bars
- Pie/ring charts for distributions
- Metric cards with trend indicators
- Ranking lists with visual bars
- Insight callout boxes
- Summary strip

【MODULE REQUIREMENTS - 7模块结构】
"""
        
        # 添加模块内容
        for i, module in enumerate(layout.modules, 1):
            prompt += f"""
Module {i} [{module.title}]:
{module.content}
"""
            if module.data_items:
                for item in module.data_items:
                    prompt += f"- {item}\n"
            if module.insight:
                prompt += f"- 洞察: {module.insight}\n"
        
        prompt += f"""
【TYPOGRAPHY STYLE】
- Bold Chinese typography for titles
- Numbers and percentages should be LARGE and prominent
- Trend arrows (↑↓) clearly visible next to metrics

【WHAT TO AVOID】
- No cute or playful style
- No excessive empty space
- No vague summaries without concrete data

【CONTENT SOURCE】
- 数据来源: {layout.data_source or '数据分析报告'}
- 时间范围: {layout.time_period or '统计周期'}
"""
        
        return prompt


class InfographicGenerator:
    """信息图生成器主类（丰富版）"""

    def __init__(self, style: StyleType = StyleType.MINIMAL,
                 ratio: str = "3:4",
                 script_dir: str = None):
        self.style = style
        self.ratio = ratio
        self.script_dir = script_dir or os.environ.get("WAN_SKILL_SCRIPTS_DIR", "./scripts")
        
        self.extractor = DataExtractor()
        self.decider = ChartDecider()
        self.prompt_builder = PromptBuilder()
    
    def generate(self, report_text: str, title: str = "数据分析报告") -> str:
        """从报告生成信息图（丰富版）"""
        
        # 1. 提取数据
        data_points = self.extractor.extract_from_report(report_text)
        
        if not data_points:
            raise ValueError("未能从报告中提取到有效数据")
        
        # 2. 构建7个模块
        modules = self._build_modules(report_text, data_points)
        
        # 3. 构建布局
        layout = InfographicLayout(
            title=title,
            subtitle=self._extract_core_insight(report_text),
            modules=modules,
            data_source=self._extract_data_source(report_text),
            time_period=self._extract_time_period(report_text)
        )
        
        # 4. 构建Prompt
        prompt = self.prompt_builder.build_prompt(layout, self.style, self.ratio)
        
        # 5. 调用Wan生成图片
        size = self._get_size_from_ratio()
        image_url = self._call_wan(prompt, size)
        
        return image_url

    def build_brief(self, report_text: str, title: str = "数据分析报告") -> dict:
        """生成结构化摘要，便于生图前人工复核"""
        data_points = self.extractor.extract_from_report(report_text)
        return {
            "title": title,
            "core_insight": self._extract_core_insight(report_text),
            "metrics": [
                {
                    "name": dp.name,
                    "value": dp.value,
                    "unit": dp.unit,
                    "trend": dp.trend,
                    "comparison": dp.comparison,
                }
                for dp in data_points[:6]
            ],
            "recommended_chart": self.decider.decide_chart_type(data_points).value if data_points else "指标卡片",
        }
    
    def _build_modules(self, report_text: str, data_points: List[DataPoint]) -> List[InfographicModule]:
        """从报告内容构建7个模块"""
        modules = []
        
        # 模块1: 报告速览
        modules.append(InfographicModule(
            module_type="报告速览",
            title="报告速览",
            content="报告主题和核心指标概览",
            data_items=[dp.name for dp in data_points[:3]],
            insight=None
        ))
        
        # 模块2: 核心发现
        modules.append(InfographicModule(
            module_type="核心发现",
            title="核心发现",
            content="最重要的发现",
            data_items=[f"{dp.name}: {dp.value}{dp.unit or ''}" for dp in data_points[:2]],
            insight=self._extract_core_insight(report_text)[:50]
        ))
        
        # 模块3: 趋势分析
        trend_items = [dp for dp in data_points if dp.trend]
        modules.append(InfographicModule(
            module_type="趋势分析",
            title="趋势分析",
            content="关键数据趋势",
            data_items=[f"{dp.name}: {dp.value}% {'↑' if dp.trend == 'up' else '↓'}" for dp in trend_items[:3]],
            insight="趋势洞察: 数据呈现明显变化"
        ))
        
        # 模块4: 结构对比
        percentage_items = [dp for dp in data_points if dp.unit == "%"][:5]
        modules.append(InfographicModule(
            module_type="结构对比",
            title="结构对比",
            content="数据分布情况",
            data_items=[f"{dp.name}: {dp.value}%" for dp in percentage_items],
            insight="对比洞察: 结构分布有特点"
        ))
        
        # 模块5: 排名洞察
        modules.append(InfographicModule(
            module_type="排名洞察",
            title="排名洞察",
            content="关键排名数据",
            data_items=[f"TOP{i+1}: {dp.name} ({dp.value}{dp.unit or ''})" for i, dp in enumerate(data_points[:3])],
            insight="排名洞察: 头部效应明显"
        ))
        
        # 模块6: 关键指标卡片
        modules.append(InfographicModule(
            module_type="关键指标",
            title="关键指标",
            content="核心数据指标",
            data_items=[f"{dp.name}: {dp.value}{dp.unit or ''} {'↑' if dp.trend == 'up' else '↓' if dp.trend == 'down' else '—'}" for dp in data_points[:4]],
            insight=None
        ))
        
        # 模块7: 一句话结论
        modules.append(InfographicModule(
            module_type="一句话结论",
            title="一句话结论",
            content=self._extract_core_insight(report_text),
            data_items=None,
            insight=f"数据来源: {self._extract_data_source(report_text)}"
        ))
        
        return modules
    
    def _extract_data_source(self, report_text: str) -> str:
        """提取数据来源"""
        keywords = ["来源", "数据来源", "报告来源", "统计", "研究"]
        for line in report_text.split('\n'):
            for kw in keywords:
                if kw in line:
                    return line.strip()[:50]
        return "数据分析报告"
    
    def _extract_time_period(self, report_text: str) -> str:
        """提取时间范围"""
        import re
        # 匹配年份和季度
        year_match = re.search(r'20\d{2}年', report_text)
        quarter_match = re.search(r'Q[1-4]|第[一二三四]季度', report_text)
        month_match = re.search(r'\d+月', report_text)
        
        parts = []
        if year_match:
            parts.append(year_match.group())
        if quarter_match:
            parts.append(quarter_match.group())
        elif month_match:
            parts.append(month_match.group())
        
        return ' '.join(parts) if parts else "统计周期"
    
    def _extract_core_insight(self, report_text: str) -> str:
        """提取核心洞察"""
        # 简化实现，实际可用LLM
        sentences = report_text.split('。')
        for sentence in sentences:
            if any(kw in sentence for kw in ['关键', '核心', '主要', '重要', '结论']):
                return sentence[:50] + "..."
        return "数据分析显示关键趋势"
    
    def _get_size_from_ratio(self) -> str:
        """根据比例获取尺寸（默认4K）"""
        ratio_map = {
            "3:4": "1774*2364",   # 4K 3:4（默认）
            "9:16": "1774*3157",  # 4K 9:16
            "4:3": "2364*1774",   # 4K 4:3
            "16:9": "3157*1774"   # 4K 16:9
        }
        return ratio_map.get(self.ratio, "1774*2364")  # 默认4K 3:4
    
    def _call_wan(self, prompt: str, size: str) -> str:
        """调用Wan API生成图片（默认使用wan2.7-image-pro）"""
        model = os.environ.get("WAN_MODEL", "wan2.7-image-pro")  # 默认使用pro模型
        cmd = [
            "python3",
            f"{self.script_dir}/image-generation-editing.py",
            "--user_requirement", prompt,
            "--n", "1",
            "--size", size,
            "--model", model
        ]
        
        result = subprocess.run(cmd, capture_output=True, text=True)
        
        # 提取URL
        for line in result.stdout.splitlines():
            if "result No." in line and "http" in line:
                return line.split(": ", 1)[1].strip()
        
        raise RuntimeError(f"Wan generation failed: {result.stderr}")
    
    def download_image(self, url: str, output_path: str = "infographic.png"):
        """下载生成的图片"""
        response = requests.get(url, timeout=60)
        response.raise_for_status()
        
        with open(output_path, 'wb') as f:
            f.write(response.content)
        
        print(f"✅ 信息图已保存: {output_path}")


# 使用示例
if __name__ == "__main__":
    report = """
    2026年Q1用户增长分析报告
    
    关键数据：
    - DAU达到150万，同比增长25%
    - MAU达到800万，环比增长12%
    - 用户留存率为45%，较上季度提升3个百分点
    - 新用户占比35%，老用户占比65%
    - 一线城市用户占比42%，二线城市占比38%，其他城市占比20%
    - 用户平均使用时长28分钟/天
    
    核心结论：用户增长势头良好，留存率持续提升。
    """
    
    generator = InfographicGenerator(
        style=StyleType.MINIMAL,
        ratio="3:4"
    )
    
    # 生成信息图
    url = generator.generate(report, title="2026年Q1用户增长分析")
    
    # 下载图片
    generator.download_image(url)
```

---

## 9. 效果示例

### 示例输入

```
2026年Q1电商销售分析报告

核心数据：
- 总销售额：5000万元，同比增长32%
- 活跃买家数：120万，环比增长15%
- 客单价：416元，较上季度提升8%
- 复购率：35%，同比提升5个百分点

品类占比：
- 服装鞋帽：42%
- 美妆个护：25%
- 食品饮料：18%
- 数码家电：10%
- 其他：5%

TOP5城市：上海、北京、广州、深圳、杭州

核心洞察：高客单价品类增长明显，复购率提升是关键驱动力。
```

### 示例输出

生成一张包含 **7个模块** 的高密度信息图：

- **模块1【报告速览】**：标题、时间范围、核心指标标签
- **模块2【核心发现】**：总销售额5000万↑32%，最重要的发现
- **模块3【趋势分析】**：销售额、买家数、客单价的趋势变化
- **模块4【结构对比】**：品类占比饼图（服装42%、美妆25%、食品18%等）
- **模块5【排名洞察】**：TOP5城市排名柱状图
- **模块6【关键指标卡片】**：4个指标卡片，带趋势箭头
- **模块7【一句话结论】**：高客单价品类增长明显，复购率提升是关键驱动力

同时可输出一份结构化摘要，帮助用户在正式交付前复核：

```yaml
title: 2026年Q1电商销售分析
core_insight: 高客单价品类增长明显，复购率提升是关键驱动力
recommended_chart: 饼图
metrics:
  - name: 销售额
    value: 5000
    unit: 万元
  - name: 活跃买家数
    value: 120
    unit: 万
  - name: 客单价
    value: 416
    unit: 元
  - name: 复购率
    value: 35
    unit: "%"
```

---

## 10. 注意事项

1. **信息密度**：一张信息图必须包含 **6-7 个核心模块**，确保高密度内容
2. **数据准确性**：生成的信息图中数据应与报告原文一致
3. **模块完整性**：每个模块必须包含具体数据、指标名称、趋势箭头或对比结论
4. **阅读顺序**：从上到下，模块1→模块7的顺序阅读
5. **配色一致性**：同一指标在不同模块中使用相同颜色编码
6. **文字可读性**：确保所有文字在生成图中清晰可读
7. **图形元素**：包含趋势箭头、对比条、饼图、排名柱状图、指标卡片等
8. **先审后发**：重要汇报场景建议先核对结构化摘要，再使用最终信息图

---

*Made with 📊 for data analysts everywhere*
