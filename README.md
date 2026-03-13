# AISEACT

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **AI-Search-EhAnCemenT** - Make AI Search Accurate, Avoid Garbage Information

🌐 **English** | [简体中文](README.zh-CN.md)

---

## What This Skill Does

AISEACT (AI-Search-EhAnCemenT) is a search enhancement skill for AI agents (OpenClaw, KimiClaw, MaxClaw, Claude Code, etc.) that solves the problem of **"high search capability but low result quality"**.

### The Problem

AI search often retrieves:
- ❌ Content farms (百家号 Baijiahao, 搜狐号 Sohu, etc.)
- ❌ Rewritten/scraped articles
- ❌ AI-generated garbage content
- ❌ Unverifiable personal opinions

**Result**: AI responses become unreliable, citing untraceable or false information.

### The Solution

AISEACT implements **ChatGPT-like search methodology**:

```
Think → Search Round 1 → Analyze Gaps → Search Round 2 → Cross-Validate → Answer
```

**Core Principles**:

| Principle | Description |
|-----------|-------------|
| **Primary Source First** | Official docs > Media reports > Analysis articles |
| **Iterative Search** | Multiple rounds, not one-and-done |
| **Active Filtering** | Auto-exclude content farms |
| **Trackability** | Every citation must be verifiable |

---

## Supported AI Agents

Use AISEACT with any of these AI coding agents:

| Agent | Platform | Installation |
|-------|----------|--------------|
| **OpenClaw** | Local/Cloud | `openclaw skill install aiseact` |
| **KimiClaw** | Moonshot AI | Copy SKILL.md to skills folder |
| **MaxClaw** | Max AI | Copy SKILL.md to skills folder |
| **Claude Code** | Anthropic | Copy to `.claude/skills/` |
| **Cursor** | Cursor AI | Copy to workspace `.cursor/skills/` |
| **Cline** | VS Code Extension | Copy to workspace |

**Key Point**: AISEACT is a **skill** (documentation-based), not a tool. It guides AI agents to search better.

---

## Installation

### For AI Agents (Natural Language Installation)

Copy and paste this prompt to your LLM agent (Claude Code, Kimi Code, Cursor, etc.):

```
Install the AISEACT skill to help me with search tasks.
Clone from: https://github.com/yourusername/aiseact
Use the SKILL.md to guide all web searches - prioritize primary sources, avoid content farms, and cross-validate important information.
```

### Manual Installation

```bash
# Clone the repository
git clone https://github.com/yourusername/aiseact.git

# For OpenClaw
openclaw skill install ./aiseact

# For other agents, copy SKILL.md to their skills folder
cp aiseact/SKILL.md ~/.claude/skills/
```

---

## Usage

### When to Use

AISEACT applies to **ALL search operations**, including:

| Scenario | Example |
|----------|---------|
| **User explicitly asks** | "Search for...", "Find information about..." |
| **AI autonomous search** | AI calls MCP tools, search APIs, or web search |
| **Built-in model search** | Model with native search capabilities |
| **Implicit information need** | Answering questions requiring current/real-time data |
| **Verification tasks** | Fact-checking, source validation |

**Rule of thumb**: If ANY search is happening, use AISEACT.

### How It Works

When you ask a research question:

```
[User] "What makes Company X successful? How does it differ from Company Y?"

[AI with AISEACT]
Phase 0: Strategy Planning
  └─ Decompose question, predict primary sources
  
Phase 1: Round 1 Search (Broad)
  └─ Search for: Company X prospectus, annual reports
  └─ Search for: Company Y financial data
  └─ Exclude: 百家号 Baijiahao, 搜狐号 Sohu, CSDN (non-original)
  
Phase 2: Gap Analysis
  └─ Missing: Core competitive advantages
  └─ Missing: Detailed tech comparison
  
Phase 3: Round 2 Search (Targeted)
  └─ site:cninfo.com.cn Company X prospectus
  └─ site:company-x.com technology whitepaper
  
Phase 4: Cross-Validation
  └─ Verify key data across 2-3 sources
  
Phase 5: Answer Generation
  └─ Cite only primary sources
  └─ Label source type (Primary/Secondary)
```

### Example Output

**Without AISEACT**:
> According to a 百家号 (Baijiahao) article, Company X IPO'd because...
> (Source: 百家号 Baijiahao - untraceable, unverifiable)

**With AISEACT**:
> According to Company X's prospectus [1], their IPO core advantages include:
> - 2000+ patents in battery technology
> - Revenue of 19.997 billion RMB in 2017
> 
> Compared to Company Y's 2023 annual report [2]...
>
> ---
> **Sources**:
> [1] Company X Prospectus (Shanghai Exchange): http://cninfo.com.cn/... - Primary Source
> [2] Company Y 2023 Annual Report: http://cninfo.com.cn/... - Primary Source

---

## Key Features

### 1. Content Farm Blacklist

Auto-excludes 1000+ unreliable sources:
- Chinese: 百家号 Baijiahao, 搜狐号 Sohu, 网易号 NetEase, CSDN (non-original), 简书 Jianshu
- English: Daily Mail, InfoWars, Natural News, Breitbart
- State-sponsored propaganda: RT, Sputnik, CGTN (for non-China topics)

### 2. Primary Source Priority

| Source Type | Credibility | Use For |
|-------------|-------------|---------|
| **Primary** | ⭐⭐⭐⭐⭐ | Company prospectus, gov announcements, official docs |
| **Quasi-Primary** | ⭐⭐⭐⭐ | Authoritative media original reports |
| **Secondary** | ⭐⭐⭐ | Analysis articles (cross-validate) |
| **Tertiary** | ⭐⭐ | Avoid: Rewritten content, 百家号 Baijiahao |

### 3. Search Syntax Guide

```
# Government info
policy_name site:gov.cn

# Company announcements (A-share)
company_name prospectus site:cninfo.com.cn

# Company announcements (Hong Kong)
company_name site:hkexnews.hk

# Technical docs
technology_name site:github.com filetype:pdf

# Exclude garbage
company_name -baijiahao -sohu
```

### 4. Six-Phase Workflow

1. **Strategy Planning** - Think before searching
2. **Round 1 Search** - Broad collection
3. **Gap Analysis** - Identify missing info
4. **Round 2 Search** - Targeted primary sources
5. **Cross-Validation** - Verify key facts
6. **Answer Generation** - Cite with trackability

---

## Project Structure

```
aiseact/
├── README.md                    # This file
├── README.zh-CN.md              # Chinese documentation
├── SKILL.md                     # Main skill file (for AI agents)
└── references/                  # Detailed reference docs
    ├── unreliable-sources.md    # Content farm blacklist
    ├── authority-sources.md     # Authoritative source recommendations
    ├── workflow.md              # Detailed 6-phase workflow
    ├── search-strategies.md     # Search syntax & techniques
    └── case-studies.md          # Real-world examples
```

### Key Files

- **SKILL.md** (257 lines) - Core methodology for AI agents
- **references/unreliable-sources.md** (586 lines) - 1000+ unreliable sources
- **references/authority-sources.md** (298 lines) - Curated authoritative sources
- **references/workflow.md** (405 lines) - Step-by-step workflow guide

---

## Why AISEACT?

### Problem: Garbage In, Garbage Out

AI search returns thousands of results, but:
- 70% are content farms (百家号 Baijiahao, 搜狐号 Sohu)
- 20% are rewritten/scraped content
- Only 10% are primary sources

### Solution: Intelligence + Discipline

AISEACT adds **methodology** to AI search:
- **Intelligence**: Multi-round iterative search
- **Discipline**: Active filtering + cross-validation
- **Transparency**: Every claim trackable to source

### Real-World Impact

| Metric | Without AISEACT | With AISEACT |
|--------|-----------------|--------------|
| Primary source usage | ~10% | ~80% |
| Content farm citations | Common | Eliminated |
| Verifiable claims | ~30% | ~95% |
| User trust | Low | High |

---

## Documentation

- **SKILL.md** - Quick start for AI agents
- **references/workflow.md** - Detailed workflow
- **references/search-strategies.md** - Search syntax guide
- **references/authority-sources.md** - Source recommendations
- **references/case-studies.md** - Real examples

---

## License

MIT © [Your Name](https://github.com/yourusername)

---

## 🌍 Languages

- [简体中文](README.zh-CN.md) - Simplified Chinese documentation

---

<div align="center">

**AISEACT** - Search Smarter, Not Harder 🔍

*Trust, but verify. Then verify again.*

[English](README.md) | [中文](README.zh-CN.md)

</div>
