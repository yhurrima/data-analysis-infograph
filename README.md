# 数据分析信息图生成器

**Data Infographic Generator**

从分析报告中自动提取关键数据和洞察，生成高质量信息图，帮助用户快速理解报告核心内容。

## 功能特点

- **智能数据提取**：自动识别报告中的关键数据点、趋势、对比
- **多图表编排**：自动设计7模块布局，包含多种图表类型
- **4种视觉风格**：简约现代、活泼明亮、深色科技、学术论文
- **一键生成**：支持4K分辨率，适合小红书分享、汇报展示

## 风格展示

### 简约现代（Minimal Modern）
黑白为主，黄色强调，极简留白，优雅大气。

![简约现代风格](examples/minimal-modern-style.png)

### 活泼明亮（Vibrant Bright）
紫+玫红+黄配色，明亮专业，年轻受众首选。

![活泼明亮风格](examples/vibrant-bright-style.png)

### 深色科技（Dark Tech）
纯色深色背景，霓虹青+紫配色，未来感强。

![深色科技风格](examples/dark-tech-style.png)

### 学术论文（Academic Paper）
米白底色，墨黑线条，严谨规范，适合研究报告。

![学术论文风格](examples/academic-paper-style.png)

## 使用方法

### 1. 准备输入
提供分析报告内容（文本/PDF/链接）

### 2. 选择风格
从4种风格中选择一种：
| 风格 | 配色 | 适用场景 |
|------|------|---------|
| 简约现代 | 黑白+黄 | 小红书、社交媒体 |
| 活泼明亮 | 紫+玫红+黄 | 科普内容、年轻受众 |
| 深色科技 | 霓虹青+紫 | 科技公司、产品发布 |
| 学术论文 | 米白+墨黑 | 研究报告、论文解读 |

### 3. 生成信息图
使用 Wan2.7-Image 模型生成，默认配置：
- 模型：`wan2.7-image-pro`
- 分辨率：4K (1774×2364，3:4比例)

## 信息图结构

生成的信息图包含 **7个核心模块**：

1. **报告速览** - 标题、时间范围、核心指标标签
2. **核心发现** - 最重要的发现及数据支撑
3. **趋势分析** - 时间序列数据变化
4. **结构对比** - 分布或类别对比
5. **排名洞察** - TOP排名数据展示
6. **关键指标** - 核心数据指标卡片
7. **一句话结论** - 总结与数据来源

## 适用场景

- 业务分析报告解读
- 用户研究/市场调研报告
- 季度/年度总结汇报
- 竞品分析报告
- 小红书/公众号数据内容创作
- 会议汇报一图总结

## 文件说明

```
data-analysis-infograph-skill/
├── README.md                        # 项目说明
├── data-analysis-infograph-skill.md # 技能详细文档
└── examples/                        # 风格示例图片
    ├── minimal-modern-style.png     # 简约现代风格
    ├── vibrant-bright-style.png     # 活泼明亮风格
    ├── dark-tech-style.png          # 深色科技风格
    └── academic-paper-style.png     # 学术论文风格
```

## License

MIT License

<!-- AUTO-README-START -->

## Auto-generated Project Map

- Project: `data-analysis-infograph-skill`

This block is managed by `update-readme` and can be regenerated at any time.

<!-- AUTO-README-END -->
