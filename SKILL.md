---
name: aiseact
description: AI Search Enhancement and Cross-verification Tool. ALWAYS USE when performing ANY web search, regardless of who initiated it - whether user explicitly asks, AI autonomously calls MCP/search tools, or model has built-in search capability. Ensures trackable, primary sources and avoids content farms. Triggers on "search", "查找", "验证", "对比", "分析", "为什么", "有什么区别", or ANY search operation.
---

# AISEACT - AI Search Enhancement and Cross-verification Tool

AISEACT (AI-Search-EnhAnCemenT) is an AI search enhancement and cross-verification tool.

**Core Mission**: Solve the problem of "high search capability but low result quality" by enabling AI to find **trackable and verifiable primary sources**, rather than garbage information from content farms.

---

## Core Principles

### Principle 1: Primary Source First

**Information Value Hierarchy**:

| Level | Type | Characteristics | Credibility |
|-------|------|-----------------|-------------|
| L1 | **Primary Source** | Original source, directly from information producer | Highest |
| L2 | **Quasi-Primary Source** | Officially authorized, close to original | High |
| L3 | **Secondary Source** | Analysis/interpretation based on primary sources | Medium |
| L4 | **Tertiary Source** | Multiple rewrites, scraped content | Low (Avoid) |

**Decision Rules**:
- Use official documents instead of analysis articles when possible
- Use raw data instead of media interpretation when possible
- Must trace secondary sources back to their original sources

### Principle 2: Iterative Search

**Prohibited**: Generating answers after a single search.

**Standard Process**:
```
Round 1: Broad search → Collect candidate sources, identify information gaps
    ↓
Analysis: Which are true primary sources? What's missing?
    ↓
Round 2: Targeted search → Fill gaps, find primary sources
    ↓
Analysis: Is information complete? Can we form a logical closure?
    ↓
Round 3 (if needed): Deep verification → Cross-validate key conclusions
```

### Principle 3: Active Filtering

**Identify and Exclude** sources with these characteristics:
- Content farm domains (百家号, 搜狐号, etc.)
- No author attribution, no publication time
- Excessive ads, messy layout
- Sensational headlines, emotional language

### Principle 4: Trackability

Every citation must meet:
- Directly accessible for verification
- Clear labeling of source nature (primary/secondary)
- Complete URL provided

---

## Six-Phase Workflow

### Phase 0: Search Strategy Planning (Critical! Think before searching)

**Complete the following analysis before starting the search**:

**1. Problem Decomposition**
- What is the core information need of the user's question?
- What types of information are needed to answer?
- Which information must come from primary sources?

**2. Source Prediction**
- Where are primary sources for this type of information most likely to be found?
- Which official websites/documents should be checked first?
- What search syntax can quickly locate them?

**3. Search Round Planning**
- Round 1: What keywords to use? What to find?
- Round 2: What information to supplement? How to cross-validate?

### Phase 1: Round 1 Search - Broad Collection

**Objective**: Gather preliminary information, identify reliable sources and key information gaps.

**Key Actions**:
- Use multiple keyword combinations
- **Actively identify and exclude** content farm results
- Record candidate source URLs and preliminary information points

**Exclusion List** (Skip immediately):
- 百家号, 搜狐号, 网易号
- CSDN (non-original authors)
- 简书, 知乎 (non-verified accounts)
- Content farms, content scrapers

### Phase 2: Assessment and Gap Analysis

**Source Credibility Assessment**:
Rate each candidate source (5-star scale), refer to authority-sources.md.

**Information Gap Identification**:
- What key information is still missing?
- What information needs primary source validation?
- What information has contradictions needing clarification?

**Round 2 Search Planning**:
Plan specific targeted search strategies for each gap.

### Phase 3: Round 2 Search - Targeted Supplement

**Objective**: Targeted supplementation of missing information, prioritizing primary sources.

**Core Strategies**:
- Use `site:` syntax to directly locate official sources
- Use `filetype:pdf` to find official documents
- Trace secondary sources back to their original sources

**Typical Targeted Search Patterns**:
```
# Company official information
target_entity + site:official_website_domain
target_entity + announcement/report site:disclosure_platform

# Government official information
policy_topic + site:gov.cn
policy_topic + site:relevant_ministry_domain

# Technology official information
technology_name + official documentation
technology_name + site:github.com
```

### Phase 4: Primary Source Validation

**Completeness Check**:
- [ ] Does core data come from official documents?
- [ ] Does technical information come from official documents?
- [ ] If secondary information exists, has it been traced to original sources?

**Cross-Validation**:
- Does key information have 2-3 independent source supports?
- Are there contradictions between sources? How to handle?

### Phase 5: Logical Closure Check

**Answer Completeness**:
- [ ] Are all aspects of the user's question covered?
- [ ] Are conclusions supported by sufficient primary information?
- [ ] Is the information chain complete and traceable?

**Garbage Information Removal**:
- [ ] Are there remaining low-quality sources?
- [ ] Have analysis articles been replaced with primary sources?

### Phase 6: Answer Generation

**Citation Format**:

```markdown
## [Answer Title]

According to [Official Source Name] disclosure[1], [key information]...

Additionally, [Another Official Source] shows[2]...

### Comparison/Analysis
[Analysis based on primary sources]

---
**Sources**:
[1] [Source Name]: [Full URL] - [Primary/Secondary]
[2] [Source Name]: [Full URL] - [Primary/Secondary]
```

**Transparency Labeling**:
- Clearly label primary sources (official website, official documents)
- Secondary sources need explanation and trace to original sources when possible
- Explain uncertainties

---

## Search Strategy Quick Reference

### Search Syntax to Avoid Low-Quality Sources

| Target | Search Syntax | Use Case |
|--------|---------------|----------|
| Government websites | `site:gov.cn` | Policies and regulations |
| Company announcements | `site:cninfo.com.cn` | A-share listed companies |
| Hong Kong announcements | `site:hkexnews.hk` | Hong Kong listed companies |
| US announcements | `site:sec.gov` | US listed companies |
| GitHub | `site:github.com` | Technical projects |
| Official documents | `filetype:pdf` | Whitepapers, annual reports |

### Primary Source Priority by Scenario

**Company Research Scenario**:
1. Company official website (products, technology, investor relations)
2. Prospectus/Annual reports (disclosure platforms)
3. Official technical documentation/GitHub
4. Official press conferences/announcements

**Technical Questions Scenario**:
1. Official documentation (first choice)
2. GitHub official repositories
3. Standard documents/RFC
4. Academic papers

**Policy and Regulations Scenario**:
1. Government official websites (gov.cn/gov)
2. Official legal databases
3. Official interpretation documents

---

## Reference Documents

| Document | Purpose |
|----------|---------|
| [references/unreliable-sources.md](references/unreliable-sources.md) | Content farm blacklist |
| [references/authority-sources.md](references/authority-sources.md) | Authoritative source recommendations (by scenario) |
| [references/workflow.md](references/workflow.md) | Detailed workflow and checklists |
| [references/search-strategies.md](references/search-strategies.md) | Specific search strategies and techniques |
| [references/case-studies.md](references/case-studies.md) | Reference cases (not templates) |

---

## Key Reminders

1. **Don't answer after one search**: Must conduct multi-round iteration
2. **Don't rely on analysis articles**: Prioritize finding primary sources
3. **Don't cite garbage sources**: Actively avoid content farms
4. **Ensure traceability**: Every information point must have source labeling
5. **Form logical closure**: Answers must have sufficient information support

---

## Quick Self-Check List

Before generating answers, confirm:

- [ ] Have at least two rounds of search been conducted?
- [ ] Does key information come from primary sources?
- [ ] Have 百家号, 搜狐号, and other garbage sources been excluded?
- [ ] Does every key conclusion have source labeling?
- [ ] Are source URLs complete and accessible?
- [ ] Are primary and secondary information distinguished?
- [ ] Are uncertainties explained?

---

*AISEACT provides reusable methodology, evolving AI search from "information搬运" to "authoritative research".*
