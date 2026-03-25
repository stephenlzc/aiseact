<h1 align="center">
  AISEACT
</h1>

<h3 align="center">
  AI-Search-EhAnCemenT — 可选的高质量搜索方法论
</h3>

<p align="center">
  <!-- 徽章 -->
  <img src="https://img.shields.io/badge/License-MIT-yellow.svg?style=flat&logo=license" alt="License: MIT" />
  <img src="https://img.shields.io/badge/Language-简体中文-blue.svg?style=flat&logo=language" alt="语言" />
  <img src="https://img.shields.io/badge/Version-1.1.0-blue.svg?style=flat&logo=version" alt="版本" />
  <img src="https://img.shields.io/badge/Last%20Updated-2026年3月-green.svg?style=flat&logo=calendar" alt="最后更新" />
  <br>
  <img src="https://img.shields.io/badge/来源质量-5%25→85%25-green.svg?style=flat&logo=quality" alt="来源质量" />
  <img src="https://img.shields.io/badge/信任度-透明-blue.svg?style=flat&logo=trust" alt="信任透明" />
  <img src="https://img.shields.io/badge/准确率提升-83%25-orange.svg?style=flat&logo=accuracy" alt="准确率提升" />
  <img src="https://img.shields.io/badge/效率提升-节省时间-75%25-yellowgreen.svg?style=flat&logo=efficiency" alt="节省时间" />
</p>

---

<h3 align="center">
  从「我以为」到「我确定」· 从不确定到确凿事实 · 从模糊引用到可验证来源
</h3>

<p align="center">
  <a href="README.en.md"><img src="https://img.shields.io/badge/-English-blue?style=flat&logo=googletranslate&logoColor=white" alt="English" /></a>
  <a href="README.md"><img src="https://img.shields.io/badge/-中文-green?style=flat&logo=googletranslate&logoColor=white" alt="中文" /></a>
  ·
  <a href="https://github.com/stephenlzc/aiseact/stargazers"><img src="https://img.shields.io/github/stars/stephenlzc/aiseact?style=social" alt="Stars" /></a>
  <a href="https://github.com/stephenlzc/aiseact/network/members"><img src="https://img.shields.io/github/forks/stephenlzc/aiseact?style=social" alt="Forks" /></a>
</p>

---

## ⚠️ 重要提示

**AISEACT 是一个可选的增强方法论**，而非强制性过滤器。你控制何时以及如何使用它。

### 为什么使用 AISEACT？

| 优势 | 效果 |
|------|------|
| 🔍 **更高来源质量** | P0 来源使用率：5–15% → 85–100% |
| ⏱️ **时间效率** | 来源验证时间减少 75% |
| ✅ **更高准确性** | 事实核查错误率降低 83% |
| 📋 **专业研究** | 针对复杂问题的结构化方法论 |
| 🔗 **可追溯性** | 清晰的来源标注和引用 |

📊 [完整评估报告 →](EVALUATION_REPORT.md)

### 工作方式

| 特性 | 说明 |
|------|------|
| 🔧 **调用方式** | 默认手动（需明确请求） |
| ⚙️ **自动模式** | 仅可选开启；需明确启用 |
| 🔄 **覆盖控制** | 始终可用；可随时跳过或自定义 |
| 📖 **透明度** | 来源评级是参考指南，而非绝对规则 |

📖 [信任与透明度报告 →](TRUST.md) · [配置指南 →](CONFIGURATION.md)

---

## 🚀 快速开始

### 对于人类

复制以下提示词给你的 AI 代理（OpenCode、Claude Code、Kimi CLI、Cursor 等）：

```
请安装并配置 aiseact skill，参考以下说明：
https://github.com/stephenlzc/aiseact
```

或手动安装：

```bash
# 克隆仓库
git clone https://github.com/stephenlzc/aiseact.git

# 复制整个目录到你的 AI 代理的 skills 文件夹

# OpenCode
cp -r aiseact ~/.config/opencode/skills/

# Claude Code
cp -r aiseact ~/.claude/skills/

# Kimi CLI
cp -r aiseact ~/.kimi/skills/
```

---

## 工作原理

### 核心方法论

```
策略 → 搜索 → 分析 → 补充 → 验证 → 回答
```

### 指导原则

| 原则 | 说明 |
|------|------|
| 📌 **一手信息优先** | 优先使用官方文档和原始来源 |
| 🔁 **迭代搜索** | 针对复杂问题进行多轮搜索 |
| 🏷️ **来源透明** | 清晰标注来源类型 |
| 🎛️ **用户控制** | 你决定包含哪些来源 |

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

**标准搜索：**
> 根据一篇网络文章，XX 公司之所以能上市，是因为...
> *(来源：未指明的博客文章)*

**使用 AISEACT：**
> 根据 XX 公司招股书[1]，其上市的核心优势包括：
> - 电池技术领域 2,000+ 项专利
> - 2017 年营收 199.97 亿元人民币
> 
> **来源：**
> [1] XX 公司招股书（上交所）— 一手来源

---

## 安装

### 支持的 AI 代理

| 代理 | 平台 | 安装方式 |
|------|------|----------|
| 🦞 **OpenClaw** | 本地/云端 | `openclaw skill install aiseact` |
| 🐙 **KimiClaw** | Moonshot AI | 复制 SKILL.md 到 skills 文件夹 |
| 🤖 **Claude Code** | Anthropic | 复制到 `.claude/skills/` |
| 📝 **Cursor** | Cursor AI | 复制到 `.cursor/skills/` |

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
- 即使启用，你也可以按查询覆盖：`"不用 AISEACT，直接搜索..."`

### 覆盖选项

当 AISEACT 激活时，你保留完全控制权：

| 命令 | 效果 |
|------|------|
| `"包含 [来源]"` | 无论评级如何，包含特定来源 |
| `"排除 [来源]"` | 排除特定来源 |
| `"显示所有来源"` | 不过滤；显示所有找到的来源 |
| `"不用 AISEACT"` | 跳过此方法论 |
| `"用宽松模式"` | 降低过滤严格度 |

📖 更多选项参见 [CONFIGURATION.md](CONFIGURATION.md)。

---

## 核心功能

### 1. 来源质量参考

常见来源评级的参考列表（参见 `references/`）：

- ⚠️ **低可信度来源**：内容农场、事实核查标准低的网站
- ✅ **权威来源**：官方文档、知名媒体、学术来源

> **重要**：这些是基于第三方评估的参考材料。你始终可以请求你需要的任何来源。

### 2. 一手信息优先

| 来源类型 | 说明 | 适用场景 |
|----------|------|----------|
| 📄 **一手信息** | 原始文档、官方来源 | 事实和数据 |
| 📑 **二手信息** | 基于一手来源的分析 | 背景和解释 |
| 📰 **三手信息** | 改写或聚合内容 | 谨慎使用 |

### 3. 搜索语法指南

```bash
# 政府信息
政策名称 site:gov.cn

# 公司公告（A股）
公司名称 招股书 site:cninfo.com.cn

# 公司公告（港股）
公司名称 site:hkexnews.hk

# 技术文档
技术名称 site:github.com filetype:pdf
```

### 4. 增强搜索 - multi-search-engine

AISEACT 集成了 **multi-search-engine**，提供强大的多引擎搜索能力：

| 功能 | 说明 |
|------|------|
| **17 个搜索引擎** | 8 个中国 + 9 个全球 |
| **无需 API 密钥** | 开箱即用 |
| **高级搜索语法** | site:、filetype:、时间过滤 |
| **隐私选项** | DuckDuckGo、Brave、Startpage |
| **知识引擎** | WolframAlpha 用于计算和事实查询 |

**引擎选择指南**：

| 查询类型 | 主要引擎 | 备用引擎 |
|---------|---------|---------|
| 中国政策 | 百度 | 必应中国 |
| 科技/代码 | Google | DuckDuckGo |
| 隐私敏感 | DuckDuckGo | Brave |
| 计算查询 | WolframAlpha | - |
| 港股公司 | Google 香港 | - |
| 全球新闻 | Google | 必应 |

**安装方式**：
```bash
# OpenClaw 安装
openclaw skill install https://clawhub.ai/gpyAngyoujun/multi-search-engine

# 或通过 LobeHub CLI
npx -y @lobehub/market-cli skills install mushroomfu-openclaw-skills-multi-search-engine
```

📖 详细使用说明请参见 [references/multi-engine-guide.md](references/multi-engine-guide.md)

---

## 项目结构

```
aiseact/
├── README.md                    # 本文件
├── README.en.md                 # English documentation
├── SKILL.md                     # 核心方法论（供 AI 代理使用）
├── TRUST.md                     # 信任与透明度报告
├── CONFIGURATION.md             # 配置指南
├── EVALUATION_REPORT.md         # 性能评估报告
├── SECURITY.md                  # 安全文档
└── references/
    ├── unreliable-sources.md    # 来源质量参考
    ├── authority-sources.md     # 权威来源推荐
    ├── quick-reference.md       # 双语快速参考
    ├── workflow.md              # 详细工作流程指南
    ├── search-strategies.md     # 搜索技巧
    ├── multi-engine-guide.md    # multi-search-engine 集成指南
    ├── search-syntax.md        # 统一搜索语法参考
    └── case-studies.md         # 案例
```

---

## 信任与透明度

### 用户自主权

- **默认**：仅手动调用
- **覆盖**：始终可用
- **来源控制**：你决定包含什么

### 已承认的局限性

- **西方中心偏见** — 评估框架偏向西方来源
- **主流媒体偏好** — 可能低估独立/另类来源
- **时效性限制** — 评级是快照，非永久

### 数据隐私

- 不存储数据
- 无外部服务器（标准搜索 API 除外）
- 无需凭证

📖 [完整信任报告 →](TRUST.md)

---

## 为什么选择 AISEACT？

### 使用场景：研究质量

当你需要：

- ✅ 带有来源 URL 的可验证声明
- ✅ 一手来源而非改写内容
- ✅ 复杂问题的结构化方法论

AISEACT 提供一个可选框架来实现这些——而不会强制用于每个查询。

### 对比

| 方面 | 标准搜索 | 使用 AISEACT |
|------|----------|--------------|
| 速度 | 快 | 中等（更彻底） |
| 来源质量 | 混合 | 更高 |
| 用户控制 | 完全 | 完全（可选） |
| 最适合 | 快速答案 | 研究、验证 |

---

## 文档

- [SKILL.md](SKILL.md) — AI 代理的核心方法论
- [TRUST.md](TRUST.md) — 信任、透明度和用户控制
- [CONFIGURATION.md](CONFIGURATION.md) — 自定义选项
- [EVALUATION_REPORT.md](EVALUATION_REPORT.md) — 性能指标
- [references/workflow.md](references/workflow.md) — 详细工作流程
- [references/authority-sources.md](references/authority-sources.md) — 来源推荐
- [references/multi-engine-guide.md](references/multi-engine-guide.md) — multi-search-engine 集成指南

---

## 🙏 致谢

特别感谢抖音的 <img src="https://simpleicons.org/icons/tiktok.svg" width="16" height="16" alt="TikTok"/> **CHEN老师说AI**，感谢您的启发和见解，帮助塑造了这个项目。

感谢 **[@gpyAngyoujun](https://clawhub.ai/gpyAngyoujun/multi-search-engine)** 提出的17引擎聚合这一出色想法 — 这个概念启发了 AISEACT 的多引擎研究工作流。在这个 vibe coding 的时代，**点子才是真正的引擎**。

---

## 许可证

MIT © [stephenlzc](https://github.com/stephenlzc)

---

<div align="center">

**AISEACT** — 在需要时进行更聪明的搜索 🔍

*信任、验证，并始终掌控。*

<a href="README.en.md"><img src="https://img.shields.io/badge/-English-blue?style=flat&logo=googletranslate&logoColor=white" alt="English" /></a>
<a href="README.md"><img src="https://img.shields.io/badge/-中文-green?style=flat&logo=googletranslate&logoColor=white" alt="中文" /></a>

</div>
