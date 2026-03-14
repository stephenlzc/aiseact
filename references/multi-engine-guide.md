# Multi-Search-Engine Integration Guide

This guide explains how to use multi-search-engine within AISEACT for enhanced search capabilities.

---

## Overview

**multi-search-engine** provides access to 17 search engines without requiring API keys. When combined with AISEACT's source quality methodology, it enables comprehensive, multi-source research.

### Key Benefits

| Benefit | Description |
|---------|-------------|
| **Coverage** | 17 engines = broader result coverage |
| **Verification** | Cross-engine validation |
| **Privacy** | Privacy-first options available |
| **No Setup** | No API keys required |

---

## Engine Categories

### China-Focused (8)

| Engine | Best For | URL |
|--------|----------|-----|
| Baidu | CN policy, local content, government | baidu.com |
| Bing CN | International results in CN | cn.bing.com |
| Sogou | WeChat indexing | sogou.com |
| WeChat | Chinese articles | wx.sogou.com |
| Toutiao | News, social content | toutiao.com |
| Jisilu | Finance, bonds | jisilu.cn |
| 360 | General CN search | so.com |
| Baidu INT | International with CN context | baidu.com (INT) |

### International (9)

| Engine | Best For | Privacy |
|--------|----------|---------|
| Google | Tech, academic, global | Low |
| Google HK | HK/Taiwan content | Low |
| DuckDuckGo | Privacy-sensitive queries | High |
| Brave | Independent index | High |
| Yahoo | General | Low |
| Startpage | Private Google | High |
| Ecosia | Eco-friendly | Medium |
| Qwant | Privacy | High |
| WolframAlpha | Facts, math, calculations | N/A |

---

## Usage Patterns

### Pattern 1: Parallel Broad Search

Execute multiple engines simultaneously for comprehensive coverage:

```
# China policy query - execute in parallel
Engine 1: Baidu + "topic_name" + site:gov.cn
Engine 2: Bing CN + "topic_name" + site:gov.cn
Engine 3: Google + "China policy topic_name"
```

**When to use**: Phase 1 (Broad Collection), complex queries requiring diverse perspectives

### Pattern 2: Sequential Target

Use specific engines for targeted results:

```
# Company research
Phase 1: Baidu (broad) - "Company X"
Phase 2: Baidu + site:cninfo.com.cn + "Company X" (A-share)
Phase 3: Google + site:company-official.com + "investor relations"
```

**When to use**: Phase 3 (Targeted Supplement), known source types

### Pattern 3: Cross-Engine Verification

Verify facts using alternative engines:

```
Primary: Google - "fact claim"
Verify: DuckDuckGo - "fact claim"  
Confirm: WolframAlpha - data verification
```

**When to use**: Phase 4 (Validation), fact-checking critical data

---

## Engine Selection Guide

### By Query Type

| Query Type | Primary | Secondary | Notes |
|-----------|---------|-----------|-------|
| China policy | Baidu | Bing CN | Use site:gov.cn |
| China companies (A-share) | Baidu | Bing CN | site:cninfo.com.cn |
| HK companies | Google HK | Baidu | site:hkexnews.hk |
| US companies | Google | Bing | site:sec.gov |
| Tech/Code | Google | DuckDuckGo | GitHub, StackOverflow |
| Privacy-sensitive | DuckDuckGo | Brave | No tracking |
| Calculations/Facts | WolframAlpha | - | Math, conversions |
| WeChat articles | Sogou WeChat | - | Chinese content |
| General CN news | Baidu | Toutiao | Current events |
| Global news | Google | Bing | Cross-verify |

### By Quality Focus

| Priority | Engine | Rationale |
|----------|--------|-----------|
| Quality focus | Google | Best index, most comprehensive |
| Quality + privacy | DuckDuckGo | Good results, no tracking |
| Alternative index | Brave | Independent from Google |
| CN-specific | Baidu | Best CN government/local |

---

## Time-Based Filtering

Use time filters for recency:

| Filter | Syntax | Use Case |
|--------|--------|----------|
| Past hour | `tbs=qdr:h` | Breaking news |
| Past week | `tbs=qdr:w` | Recent developments |
| Past month | `tbs=qdr:m` | Current trends |
| Past year | `tbs=qdr:y` | Historical data |

Example:
```
topic_name tbs=qdr:m  # Past month results
```

---

## Integration with AISEACT Phases

### Phase 0: Planning
- Select engines based on query type
- Plan parallel vs sequential execution

### Phase 1: Broad Search
- Execute 2-3 engines in parallel
- Combine and deduplicate results

### Phase 2: Assessment
- Identify gaps in coverage
- Note which engines returned best results

### Phase 3: Targeted Search
- Use primary engine with site: operators
- Target specific source types

### Phase 4: Verification
- Use alternative engine for cross-validation
- WolframAlpha for factual data

---

## Engine-Specific Tips

### Baidu
- Best for: Chinese government sites, CN news, local content
- Syntax: `site:gov.cn`, `site:cninfo.com.cn`
- Tip: Add `site:cn` for broader Chinese sources

### Google
- Best for: Tech, academic, international content
- Syntax: `site:github.com`, `filetype:pdf`, `intitle:`
- Tip: Use Google HK for HK/Taiwan content

### DuckDuckGo
- Best for: Privacy-sensitive queries, avoiding personalization
- Syntax: Standard search operators
- Tip: Use `!bang` shortcuts: `!gh` (GitHub), `!so` (StackOverflow)

### WolframAlpha
- Best for: Calculations, factual queries, conversions
- Syntax: Natural language math queries
- Tip: Use for verification of statistics, dates, facts

### Brave Search
- Best for: Independent index, ad-free results
- Syntax: Standard operators
- Tip: Good alternative to Google for unbiased results

---

## Quick Reference

### Installation

```bash
# OpenClaw
openclaw skill install https://clawhub.ai/gpyAngyoujun/multi-search-engine

# LobeHub CLI
npx -y @lobehub/market-cli skills install mushroomfu-openclaw-skills-multi-search-engine
```

### Basic Usage

```
Use multi-search-engine to search [topic]
```

### Multi-Engine Search

```
Use multi-search-engine with Baidu, Google, and DuckDuckGo to search [topic]
```

---

*Combine multi-search-engine's capabilities with AISEACT's methodology for optimal research results.*
