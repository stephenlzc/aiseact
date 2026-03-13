# AISEACT

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![信任: 透明](https://img.shields.io/badge/信任-透明-blue.svg)](TRUST.md)

> **AI-Search-EhAnCemenT** - 可选的高质量搜索方法论

🌐 [English](README.md) | **简体中文**

---

## ⚠️ 重要提示：用户可控工具

AISEACT 是一个**可选的增强方法论**，而非强制性过滤器。你控制何时以及如何使用它。
#JB|AISEACT 是一个**可选的增强方法论**，而非强制性过滤器。你控制何时以及如何使用它。
#KB|
#HM|### 为什么使用 AISEACT？（优势）
#QM|
#HB|| 优势 | 效果 |
#HQ||------|------|
#BM|| **更高来源质量** | P0 来源使用率从 5-15% 提升至 85-100% |
#RJ|| **时间效率** | 来源验证时间减少 75% |
#SK|| **更高准确性** | 事实核查错误率降低 83% |
#NT|| **专业研究** | 针对复杂问题的结构化方法论 |
#BQ|| **可追溯性** | 清晰的来源标注和引用 |
#JM|
#NR|📊 **[查看完整评估报告 →](EVALUATION_REPORT.md)**
#RJ|
| 特性 | 工作方式 |
|------|----------|
| **调用方式** | 默认手动（你明确请求时才使用） |
| **自动模式** | 仅可选开启；必须明确启用 |
| **覆盖控制** | 你始终可以请求任何来源或跳过此方法 |
| **透明度** | 来源评级是参考指南，而非绝对规则 |

📖 **[阅读我们的信任与透明度报告 →](TRUST.md)**
📖 **[配置指南 →](CONFIGURATION.md)**

---

## 这个 Skill 是做什么的

AISEACT (AI-Search-EhAnCemenT) 提供了一个**结构化的可选方法论**，用于在你需要严谨、来源可靠的答案时提升 AI 搜索质量。

### 何时使用 AISEACT

**✅ 推荐使用场景：**
- 学术或专业研究
- 事实核查和验证任务
- 需要高质量来源的商业或技术分析
- 需要可追溯、权威来源的问题

**❌ 不需要使用的场景：**
- 快速随意查询（"今天天气如何？"）
- 创意写作或头脑风暴
- 主观意见或需要多元视角的情况

### 解决的问题

AI 搜索经常检索到质量参差不齐的结果：
- 内容农场（百家号、采集站）
- 没有原创洞见的洗稿文章
- 无法验证的声明

**AISEACT 提供解决方案**：一种系统性的方法来优先选择一手来源并提升可追溯性——在你选择使用它时。

---

## 工作原理

### 核心方法论（可选）

```
策略 → 搜索 → 分析 → 补充 → 验证 → 回答
```

**指导原则**（在你请求 AISEACT 时应用）：

| 原则 | 说明 |
|------|------|
| **一手信息优先** | 优先使用官方文档和原始来源 |
| **迭代搜索** | 针对复杂问题进行多轮搜索 |
| **来源透明** | 清晰标注来源类型 |
| **用户控制** | 你决定包含哪些来源 |

### 使用示例

```
[用户] "用 AISEACT 研究 XX 公司成功的原因"

[使用 AISEACT 的 AI]
Phase 0: 策略规划
  └─ 拆解问题，识别一手来源位置
  
Phase 1: 初步搜索
  └─ 搜索：XX 公司招股书、年报
  └─ 参考来源质量指南
  
Phase 2: 分析
  └─ 识别缺失信息
  
Phase 3: 定向搜索
  └─ site:cninfo.com.cn XX 公司招股书
  └─ site:company-x.com 官方数据
  
Phase 4: 回答生成
  └─ 引用可验证来源
  └─ 标注来源类型
  └─ 注明任何不确定性
```

### 输出示例

**标准搜索**：
> 根据一篇网络文章，XX 公司之所以能上市，是因为...
> （来源：未指明的博客文章）

**使用 AISEACT**：
> 根据 XX 公司招股书[1]，其上市的核心优势包括：
> - 电池技术领域 2000+ 项专利
> - 2017 年营收 199.97 亿元人民币
> 
> **来源**：
> [1] XX 公司招股书（上交所）：http://cninfo.com.cn/... - 一手来源

---

## 安装

### 支持的 AI 代理

| 代理 | 平台 | 安装方式 |
|------|------|----------|
| **OpenClaw** | 本地/云端 | `openclaw skill install aiseact` |
| **KimiClaw** | Moonshot AI | 复制 SKILL.md 到 skills 文件夹 |
| **Claude Code** | Anthropic | 复制到 `.claude/skills/` |
| **Cursor** | Cursor AI | 复制到工作区 `.cursor/skills/` |

### 手动安装

```bash
# 克隆仓库
git clone https://github.com/stephenlzc/aiseact.git

# 复制到你的 AI 代理的 skills 文件夹
cp aiseact/SKILL.md ~/.claude/skills/
```

---

## 使用方法

### 手动模式（默认）

在需要时明确请求 AISEACT：

```
"请用 AISEACT 搜索..."
"用 AISEACT 验证这个说法"
"Use AISEACT to research..."
```

### 自动模式（可选）

在配置中启用自动调用：
- 设置 `disable-model-invocation: false`
- 即使启用，你也可以按查询覆盖："不用 AISEACT，直接搜索..."

### 覆盖选项

当 AISEACT 激活时，你保留完全控制权：

| 命令 | 效果 |
|------|------|
| "包含 [来源]" | 无论评级如何，包含特定来源 |
| "排除 [来源]" | 排除特定来源 |
| "显示所有来源" | 不过滤；显示所有找到的来源 |
| "不用 AISEACT" | 跳过此方法论 |
| "用宽松模式" | 降低过滤严格度 |

更多选项参见 [CONFIGURATION.md](CONFIGURATION.md)。

---

## 核心功能

### 1. 来源质量参考

常见来源评级的参考列表（参见 `references/`）：
- **低可信度来源**：内容农场、事实核查标准低的网站
- **权威来源**：官方文档、知名媒体、学术来源

**重要**：这些是基于第三方评估的参考材料。你始终可以请求你需要的任何来源。

### 2. 一手信息优先

| 来源类型 | 说明 | 适用场景 |
|----------|------|----------|
| **一手信息** | 原始文档、官方来源 | 最适合事实和数据 |
| **二手信息** | 基于一手来源的分析 | 适合背景和解释 |
| **三手信息** | 改写或聚合内容 | 谨慎使用；可能缺乏原创洞见 |

### 3. 搜索语法指南

```
# 政府信息
政策名称 site:gov.cn

# 公司公告（A股）
公司名称 招股书 site:cninfo.com.cn

# 公司公告（港股）
公司名称 site:hkexnews.hk

# 技术文档
技术名称 site:github.com filetype:pdf
```

---

## 项目结构

```
aiseact/
├── README.md                    # 本文件
├── README.zh-CN.md              # 中文文档
├── SKILL.md                     # 核心方法论（供 AI 代理使用）
├── TRUST.md                     # 信任与透明度报告
├── CONFIGURATION.md             # 配置指南
└── references/                  # 参考文档
    ├── unreliable-sources.md    # 来源质量参考（含免责声明）
    ├── authority-sources.md     # 权威来源推荐
    ├── workflow.md              # 详细工作流程指南
    ├── search-strategies.md     # 搜索技巧
    └── case-studies.md          # 案例
```

---

## 信任与透明度

### 用户自主权

- **默认**：仅手动调用
- **覆盖**：始终可用
- **来源控制**：你决定包含什么

### 已承认的局限性

- **西方中心偏见**：评估框架偏向西方来源
- **主流媒体偏好**：可能低估独立/另类来源
- **时效性限制**：评级是快照，非永久

### 数据隐私

- 不存储数据
- 无外部服务器（标准搜索 API 除外）
- 无需凭证

📖 **[完整信任报告 →](TRUST.md)**

---

## 为什么选择 AISEACT？

### 使用场景：研究质量

当你需要：
- 带有来源 URL 的可验证声明
- 一手来源而非改写内容
- 复杂问题的结构化方法论

AISEACT 提供一个可选框架来实现这些——而不会强制用于每个查询。

### 对比

| 方面 | 标准搜索 | 使用 AISEACT |
|------|----------|--------------|
| 速度 | 快 | 中等（更彻底） |
| 来源质量 | 混合 | 更高（应用方法论时） |
| 用户控制 | 完全 | 完全（方法论是可选的） |
| 最适合 | 快速答案 | 研究、验证 |

---

## 文档

- **[SKILL.md](SKILL.md)** - AI 代理的核心方法论
- **[TRUST.md](TRUST.md)** - 信任、透明度和用户控制
- **[CONFIGURATION.md](CONFIGURATION.md)** - 自定义选项
- **[references/workflow.md](references/workflow.md)** - 详细工作流程
- **[references/authority-sources.md](references/authority-sources.md)** - 来源推荐

---

## 许可证

MIT © [stephenlzc](https://github.com/stephenlzc)

---

## 🌍 语言

- [English](README.md) - 英文文档

---

<div align="center">

**AISEACT** - 在需要时进行更聪明的搜索 🔍

*信任、验证，并始终掌控。*

[English](README.md) | [中文](README.zh-CN.md)

</div>
