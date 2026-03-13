<h1 align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&weight=700&size=40&duration=2000&pause=800&color=3B82F6&center=true&vCenter=true&width=500&lines=AISEACT" alt="AISEACT" />
</h1>

<h3 align="center">
  AI-Search-EhAnCemenT — An Optional Methodology for Higher-Quality Search Results
</h3>

<p align="center">
  <!-- Badges -->
  <img src="https://img.shields.io/badge/License-MIT-yellow.svg?style=flat&logo=license" alt="License: MIT" />
  <img src="https://img.shields.io/badge/Language-English-blue.svg?style=flat&logo=english" alt="Language" />
  <img src="https://img.shields.io/badge/Version-1.1.0-blue.svg?style=flat&logo=version" alt="Version" />
  <img src="https://img.shields.io/badge/Last%20Updated-March%202026-green.svg?style=flat&logo=calendar" alt="Last Updated" />
  <br>
  <img src="https://img.shields.io/badge/Source%20Quality-5%25→85%25-green.svg?style=flat&logo=quality" alt="Source Quality" />
  <img src="https://img.shields.io/badge/Trust-Transparent-blue.svg?style=flat&logo=trust" alt="Trust" />
</p>

---

<h3 align="center">
  <img src="https://readme-typing-svg.herokuapp.com?font=Fira+Code&size=18&duration=3000&pause=1500&color=10B981&center=true&vCenter=true&width=750&lines=From+I+think+to+I+know;From+uncertainty+to+facts;From+vague+citations+to+verifiable+sources" alt="Slogan" />
</h3>

<p align="center">
  🌐 <strong>English</strong> · <a href="README.zh-CN.md">简体中文</a> · <a href="https://github.com/stephenlzc/aiseact/stargazers"><img src="https://img.shields.io/github/stars/stephenlzc/aiseact?style=social" alt="Stars" /></a> · <a href="https://github.com/stephenlzc/aiseact/network/members"><img src="https://img.shields.io/github/forks/stephenlzc/aiseact?style=social" alt="Forks" /></a>
</p>

---

## ⚠️ Important Notice

**AISEACT is an optional enhancement methodology**, not a mandatory filter. You control when and how it's used.

### Why Use AISEACT?

| Benefit | Impact |
|---------|--------|
| 🔍 **Higher Source Quality** | P0 source usage: 5–15% → 85–100% |
| ⏱️ **Time Efficiency** | 75% less time on source verification |
| ✅ **Better Accuracy** | Fact-check error rate: −83% |
| 📋 **Professional Research** | Structured methodology for complex questions |
| 🔗 **Traceability** | Clear source labeling and citations |

📊 [Full Evaluation Report →](EVALUATION_REPORT.md)

---

## 🚀 Quick Start

### For Humans

Copy and paste this prompt to your AI agent (OpenCode, Claude Code, Kimi CLI, Cursor, etc.):

```
Install and configure aiseact skill by following the instructions here:
https://github.com/stephenlzc/aiseact
```

Or install manually:

```bash
# Clone the repository
git clone https://github.com/stephenlzc/aiseact.git

# Copy the entire directory to your AI agent's skills folder
# (replace 'destination' with your AI tool's skills path)

# OpenCode
cp -r aiseact ~/.config/opencode/skills/

# Claude Code
cp -r aiseact ~/.claude/skills/

# Kimi CLI
cp -r aiseact ~/.kimi/skills/
```

---

## How It Works

| Feature | Description |
|---------|-------------|
| 🔧 **Invocation** | Manual by default (explicit request required) |
| ⚙️ **Autonomous Mode** | Opt-in only; must be explicitly enabled |
| 🔄 **Override** | Always available; skip or customize anytime |
| 📖 **Transparency** | Source ratings are guidelines, not rules |

📖 [Trust & Transparency Report →](TRUST.md) · [Configuration Guide →](CONFIGURATION.md)

---

## What This Skill Does

AISEACT provides a **structured, optional methodology** for improving AI search quality when you need rigorous, well-sourced answers.

### When to Use AISEACT

**✅ Recommended for:**
- Academic or professional research
- Fact-checking and verification tasks
- Business or technical analysis where source quality matters
- Questions requiring traceable, authoritative sources

**❌ Not needed for:**
- Quick casual queries ("What's the weather?")
- Creative writing or brainstorming
- Subjective opinions or diverse perspectives

### The Problem It Solves

AI search often retrieves mixed-quality results:

- Content farms (百家号, scraper sites)
- Rewritten articles without original insight
- Unverifiable claims

**AISEACT offers a solution**: A systematic approach to prioritize primary sources and improve traceability — when you choose to use it.

---

## How It Works

### Core Methodology

```
Strategy → Search → Analyze → Supplement → Validate → Answer
```

### Guiding Principles

| Principle | Description |
|-----------|-------------|
| 📌 **Primary Source Priority** | Prefer official docs and original sources |
| 🔁 **Iterative Search** | Multiple rounds for complex questions |
| 🏷️ **Source Transparency** | Clear labeling of source types |
| 🎛️ **User Control** | You decide which sources to include |

### Example Usage

```
[User] "Use AISEACT to research what makes Company X successful"

[AI with AISEACT]
  Phase 0: Strategy Planning
    └─ Decompose question, identify primary source locations
    
  Phase 1: Initial Search
    └─ Search for: Company X prospectus, annual reports
    └─ Reference source quality guidelines
    
  Phase 2: Analysis
    └─ Identify missing information
    
  Phase 3: Targeted Search
    └─ site:cninfo.com.cn Company X prospectus
    └─ site:company-x.com official data
    
  Phase 4: Answer Generation
    └─ Cite verifiable sources
    └─ Label source types
    └─ Note any uncertainties
```

### Example Output

**Standard Search:**
> According to an online article, Company X IPO'd because...
> *(Source: unspecified blog post)*

**With AISEACT:**
> According to Company X's prospectus [1], their IPO core advantages include:
> - 2,000+ patents in battery technology
> - Revenue of 19.997 billion RMB in 2017
> 
> **Sources:**
> [1] Company X Prospectus (Shanghai Exchange) — Primary Source

---

## Installation

### Supported AI Agents

| Agent | Platform | Installation |
|-------|----------|--------------|
| 🦞 **OpenClaw** | Local/Cloud | `openclaw skill install aiseact` |
| 🐙 **KimiClaw** | Moonshot AI | Copy SKILL.md to skills folder |
| 🤖 **Claude Code** | Anthropic | Copy to `.claude/skills/` |
| 📝 **Cursor** | Cursor AI | Copy to `.cursor/skills/` |

### Manual Installation

```bash
# Clone the repository
git clone https://github.com/stephenlzc/aiseact.git

# Copy to your AI agent's skills folder
cp aiseact/SKILL.md ~/.claude/skills/
```

---

## Usage

### Manual Mode (Default)

Explicitly request AISEACT when you need it:

```
"请用AISEACT搜索..."
"Use AISEACT to research..."
"用AISEACT验证这个说法"
```

### Autonomous Mode (Optional)

Enable automatic invocation in your configuration:

- Set `disable-model-invocation: false` for this skill
- Even enabled, you can override per-query: `"不用AISEACT，直接搜索..."`

### Override Options

When AISEACT is active, you retain full control:

| Command | Effect |
|---------|--------|
| `"包含 [source]"` | Include a specific source regardless of ratings |
| `"排除 [source]"` | Exclude a specific source |
| `"显示所有来源"` | Don't filter; show all found sources |
| `"不用AISEACT"` | Skip the methodology for this query |
| `"用宽松模式"` | Reduce filtering strictness |

📖 See [CONFIGURATION.md](CONFIGURATION.md) for more options.

---

## Key Features

### 1. Source Quality Reference

Reference lists of commonly rated sources (see `references/`):

- ⚠️ **Unreliable sources**: Content farms, sites with low fact-check standards
- ✅ **Authoritative sources**: Official documents, reputable media, academic sources

> **Important**: These are reference materials based on third-party assessments. You can always request any source you need.

### 2. Primary Source Priority

| Source Type | Description | Use Case |
|-------------|-------------|----------|
| 📄 **Primary** | Original documents, official sources | Facts and data |
| 📑 **Secondary** | Analysis based on primary sources | Context and interpretation |
| 📰 **Tertiary** | Rewritten or aggregated content | Use with caution |

### 3. Search Syntax Guide

```bash
# Government info
policy_name site:gov.cn

# Company announcements (A-share)
company_name prospectus site:cninfo.com.cn

# Company announcements (Hong Kong)
company_name site:hkexnews.hk

# Technical docs
technology_name site:github.com filetype:pdf
```

---

## Project Structure

```
aiseact/
├── README.md                    # This file
├── README.zh-CN.md              # Chinese documentation
├── SKILL.md                     # Core methodology (for AI agents)
├── TRUST.md                     # Trust & transparency report
├── CONFIGURATION.md             # Configuration guide
├── EVALUATION_REPORT.md         # Performance evaluation report
├── SECURITY.md                  # Security documentation
└── references/
    ├── unreliable-sources.md    # Source quality reference
    ├── authority-sources.md     # Authoritative source recommendations
    ├── quick-reference.md       # Bilingual quick reference
    ├── workflow.md              # Detailed workflow guide
    ├── search-strategies.md     # Search techniques
    └── case-studies.md          # Examples
```

---

## Trust & Transparency

### User Autonomy

- **Default:** Manual invocation only
- **Override:** Always available
- **Source Control:** You decide what to include

### Acknowledged Limitations

- **Western-centric bias** — Evaluation frameworks favor Western sources
- **Mainstream preference** — May undervalue independent/alternative sources
- **Temporal limitations** — Ratings are snapshots, not permanent

### Data Privacy

- No data storage
- No external servers beyond standard search APIs
- No credential requirements

📖 [Full Trust Report →](TRUST.md)

---

## Why AISEACT?

### Use Case: Research Quality

When you need:

- ✅ Verifiable claims with source URLs
- ✅ Primary sources over rewritten content
- ✅ Structured methodology for complex questions

AISEACT provides an optional framework — without forcing it on every query.

### Comparison

| Aspect | Standard Search | With AISEACT |
|--------|-----------------|--------------|
| Speed | Fast | Moderate (more thorough) |
| Source Quality | Mixed | Higher |
| User Control | Full | Full (optional) |
| Best For | Quick answers | Research, verification |

---

## Documentation

- [SKILL.md](SKILL.md) — Core methodology for AI agents
- [TRUST.md](TRUST.md) — Trust, transparency, and user control
- [CONFIGURATION.md](CONFIGURATION.md) — Customization options
- [EVALUATION_REPORT.md](EVALUATION_REPORT.md) — Performance metrics
- [references/workflow.md](references/workflow.md) — Detailed workflow
- [references/authority-sources.md](references/authority-sources.md) — Source recommendations

---

## License

MIT © [stephenlzc](https://github.com/stephenlzc)

---

<div align="center">

**AISEACT** — Search Smarter, When You Need To 🔍

*Trust, verify, and always stay in control.*

[English](README.md) · [中文](README.zh-CN.md)

</div>
