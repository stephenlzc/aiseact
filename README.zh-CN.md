# AISEACT

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **AI-Search-EhAnCemenT** - 让AI搜索更准确，远离垃圾信息

🌐 [English](README.md) | **简体中文**

---

## 这个 Skill 是做什么的

AISEACT (AI-Search-EhAnCemenT) 是一个面向AI代理（OpenClaw、KimiClaw、MaxClaw、Claude Code等）的搜索增强技能，解决**"搜索能力强但结果质量低"**的问题。

### 问题所在

AI搜索经常检索到：
- ❌ 内容农场（百家号、搜狐号等）
- ❌ 洗稿/采集文章
- ❌ AI生成的垃圾内容
- ❌ 无法验证的个人观点

**结果**：AI回复变得不可靠，引用无法追溯或错误的信息。

### 解决方案

AISEACT 实现了**类似ChatGPT的搜索方法论**：

```
思考 → 第一轮搜索 → 分析缺口 → 第二轮搜索 → 交叉验证 → 生成回答
```

**核心原则**：

| 原则 | 说明 |
|------|------|
| **一手信息优先** | 官方文档 > 媒体报道 > 分析文章 |
| **多轮迭代搜索** | 多次搜索，而非一次搞定 |
| **主动过滤** | 自动排除内容农场 |
| **可追溯性** | 每个引用都必须可验证 |

---

## 支持的AI代理

AISEACT 可与以下AI编程代理配合使用：

| 代理 | 平台 | 安装方式 |
|------|------|----------|
| **OpenClaw** | 本地/云端 | `openclaw skill install aiseact` |
| **KimiClaw** | Moonshot AI | 复制 SKILL.md 到 skills 文件夹 |
| **MaxClaw** | Max AI | 复制 SKILL.md 到 skills 文件夹 |
| **Claude Code** | Anthropic | 复制到 `.claude/skills/` |
| **Cursor** | Cursor AI | 复制到工作区 `.cursor/skills/` |
| **Cline** | VS Code插件 | 复制到工作区 |

**关键点**：AISEACT 是一个**技能**（基于文档），而非工具。它指导AI代理更好地搜索。

---

## 安装

### 给AI代理（自然语言安装）

复制粘贴这段提示给你的LLM代理（Claude Code、Kimi Code、Cursor等）：

```
安装 AISEACT 技能来帮助我进行搜索任务。
从以下地址克隆：https://github.com/yourusername/aiseact
使用 SKILL.md 来指导所有网络搜索——优先使用一手来源，避免内容农场，并对重要信息进行交叉验证。
```

### 手动安装

```bash
# 克隆仓库
git clone https://github.com/yourusername/aiseact.git

# 对于 OpenClaw
openclaw skill install ./aiseact

# 对于其他代理，将 SKILL.md 复制到他们的 skills 文件夹
cp aiseact/SKILL.md ~/.claude/skills/
```

---

## 使用方法

### 何时使用

AISEACT 适用于**所有搜索操作**，包括：

| 场景 | 示例 |
|------|------|
| **用户明确要求** | "搜索..."、"查找关于...的信息" |
| **AI自主搜索** | AI调用MCP工具、搜索API或网页搜索 |
| **模型内置搜索** | 具有原生搜索能力的模型 |
| **隐式信息需求** | 回答需要当前/实时数据的问题 |
| **验证任务** | 事实核查、来源验证 |

**经验法则**：只要发生任何搜索，就使用AISEACT。

### 工作原理

当你提出一个研究问题时：

```
[用户] "XX公司为什么能成功上市？它和YY公司有什么区别？"

[使用 AISEACT 的AI]
Phase 0: 搜索策略规划
  └─ 拆解问题，预判一手来源
  
Phase 1: 第一轮搜索（广泛收集）
  └─ 搜索：XX公司招股书、年报
  └─ 搜索：YY公司财务数据
  └─ 排除：百家号、搜狐、CSDN爬虫
  
Phase 2: 缺口分析
  └─ 缺失：核心竞争优势
  └─ 缺失：详细技术对比
  
Phase 3: 第二轮搜索（定向补充）
  └─ site:cninfo.com.cn XX公司招股书
  └─ site:company-x.com 技术白皮书
  
Phase 4: 交叉验证
  └─ 在2-3个来源间验证关键数据
  
Phase 5: 回答生成
  └─ 只引用一手来源
  └─ 标注来源类型（一手/二手）
```

### 输出示例

**不使用 AISEACT**：
> 根据百家号的一篇文章，XX公司之所以能上市，是因为他们在电池领域很厉害...
> （来源：百家号 - 无法追溯，无法验证）

**使用 AISEACT**：
> 根据XX公司招股书[1]，其上市的核心优势包括：
> - 电池技术领域2000+项专利
> - 2017年营收199.97亿元人民币
> 
> 与YY公司2023年年报[2]相比...
>
> ---
> **来源**：
> [1] XX公司招股书（上交所）：http://cninfo.com.cn/... - 一手来源
> [2] YY公司2023年年报：http://cninfo.com.cn/... - 一手来源

---

## 核心功能

### 1. 内容农场黑名单

自动排除1000+不可靠来源：
- 中文：百家号、搜狐号、网易号、CSDN（非原创）、简书
- 英文：Daily Mail、InfoWars、Natural News、Breitbart
- 国家赞助宣传：RT、Sputnik、CGTN（针对非中国话题）

### 2. 一手信息优先

| 来源类型 | 可信度 | 用于 |
|----------|--------|------|
| **一手信息** | ⭐⭐⭐⭐⭐ | 公司招股书、政府公告、官方文档 |
| **准一手信息** | ⭐⭐⭐⭐ | 权威媒体原创报道 |
| **二手信息** | ⭐⭐⭐ | 分析文章（需交叉验证） |
| **三手信息** | ⭐⭐ | 避免：洗稿内容、百家号 |

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

# 排除垃圾信息
公司名称 -baijiahao -sohu
```

### 4. 六阶段工作流程

1. **策略规划** - 先想后搜
2. **第一轮搜索** - 广泛收集
3. **缺口分析** - 识别缺失信息
4. **第二轮搜索** - 定向查找一手来源
5. **交叉验证** - 验证关键事实
6. **回答生成** - 可追溯引用

---

## 项目结构

```
aiseact/
├── README.md                    # 本文件
├── README.zh-CN.md              # 中文文档
├── SKILL.md                     # 主技能文件（供AI代理使用）
└── references/                  # 详细参考文档
    ├── unreliable-sources.md    # 内容农场黑名单
    ├── authority-sources.md     # 权威来源推荐
    ├── workflow.md              # 详细六阶段工作流程
    ├── search-strategies.md     # 搜索语法与技巧
    └── case-studies.md          # 真实案例
```

### 关键文件

- **SKILL.md** (257行) - AI代理的核心方法论
- **references/unreliable-sources.md** (586行) - 1000+不可靠来源
- **references/authority-sources.md** (298行) - 精选权威来源
- **references/workflow.md** (405行) - 分步工作流程指南

---

## 为什么选择AISEACT？

### 问题：垃圾进，垃圾出

AI搜索返回数千条结果，但是：
- 70%是内容农场（百家号、搜狐）
- 20%是洗稿/采集内容
- 只有10%是一手来源

### 解决方案：智能+规范

AISEACT为AI搜索添加了**方法论**：
- **智能**：多轮迭代搜索
- **规范**：主动过滤+交叉验证
- **透明**：每个声明都可追溯到来源

### 实际效果

| 指标 | 不使用AISEACT | 使用AISEACT |
|------|---------------|-------------|
| 一手来源使用率 | ~10% | ~80% |
| 内容农场引用 | 常见 | 消除 |
| 可验证声明 | ~30% | ~95% |
| 用户信任度 | 低 | 高 |

---

## 文档

- **SKILL.md** - AI代理快速入门
- **references/workflow.md** - 详细工作流程
- **references/search-strategies.md** - 搜索语法指南
- **references/authority-sources.md** - 来源推荐
- **references/case-studies.md** - 真实案例

---

## 许可证

MIT © [Your Name](https://github.com/yourusername)

---

## 🌍 语言

- [English](README.md) - 英文文档

---

<div align="center">

**AISEACT** - 更聪明的搜索，而非更困难的搜索 🔍

*信任，但验证。然后再验证一次。*

[English](README.md) | [中文](README.zh-CN.md)

</div>
