# Unified Search Syntax Reference

This document combines AISEACT priority operators with multi-search-engine capabilities.

---

## AISEACT Priority Operators

These operators help locate authoritative primary sources.

### Government & Official

| Syntax | Target | Example |
|--------|--------|---------|
| `site:gov.cn` | Chinese government sites | `policy_name site:gov.cn` |
| `site:gov` | International government | `regulation_name site:gov` |
| `site:gov.uk` | UK government | `topic_name site:gov.uk` |

### Company Disclosures

| Syntax | Target | Example |
|--------|--------|---------|
| `site:cninfo.com.cn` | China A-share disclosures | `company_name annual_report site:cninfo.com.cn` |
| `site:hkexnews.hk` | HK stock disclosures | `company_name prospectus site:hkexnews.hk` |
| `site:sec.gov` | US SEC filings | `company_name 10-K site:sec.gov` |

### Academic & Technical

| Syntax | Target | Example |
|--------|--------|---------|
| `site:edu.cn` | Chinese universities | `topic_name site:edu.cn` |
| `site:edu` | International universities | `topic_name site:edu` |
| `site:github.com` | GitHub repositories | `project_name site:github.com` |

---

## multi-search-engine Operators

### File Type Limitation

| Syntax | Target | Example |
|--------|--------|---------|
| `filetype:pdf` | PDF documents | `topic_name filetype:pdf` |
| `filetype:doc` | Word documents | `topic_name filetype:doc` |
| `filetype:ppt` | PowerPoint | `topic_name filetype:ppt` |

### Text Matching

| Syntax | Function | Example |
|--------|----------|---------|
| `"exact phrase"` | Exact match | `"artificial intelligence"` |
| `-exclude` | Exclude term | `topic -advertisement` |
| `OR` | Boolean OR | `AI OR machine_learning` |
| `()` | Grouping | `(AI OR ML) site:github.com` |

### Advanced

| Syntax | Function | Example |
|--------|----------|---------|
| `intitle:` | Title contains | `intitle:tutorial python` |
| `inurl:` | URL contains | `inurl:blog python` |
| `intext:` | Body contains | `intext:implementation python` |

---

## Time Filters

### multi-search-engine Time Parameters

| Filter | Syntax | Use Case |
|--------|--------|----------|
| Past hour | `tbs=qdr:h` | Breaking news |
| Past day | `tbs=qdr:d` | Today's events |
| Past week | `tbs=qdr:w` | Recent developments |
| Past month | `tbs=qdr:m` | Current trends |
| Past year | `tbs=qdr:y` | Historical data |

### Examples

```
# Past month results
topic_name tbs=qdr:m

# Past year for historical research
event_name tbs=qdr:y
```

---

## Engine-Specific Syntax

### DuckDuckGo Bangs

| Bang | Target | Example |
|------|--------|---------|
| `!gh` | GitHub | `!gh react hooks` |
| `!so` | StackOverflow | `!so python async` |
| `!w` | Wikipedia | `!w machine learning` |
| `!aws` | AWS Docs | `!aws s3` |
| `!g` | Google | `!g python tutorial` |

### WolframAlpha

Direct queries for factual data:
```
# Mathematical
integral of x^2
population of China

# Conversions
100 USD to EUR
miles to kilometers 50

# Facts
Apple Inc revenue
Tesla market cap
```

---

## Combined Patterns

### Company Research

```
# A-share company
company_name 招股说明书 site:cninfo.com.cn filetype:pdf

# HK company
company_name prospectus site:hkexnews.hk

# US company
company_name "10-K" filetype:pdf
```

### Technical Documentation

```
# Official docs
framework_name documentation site:docs.example.com

# GitHub
library_name site:github.com README

# Papers
technology_name survey filetype:pdf
```

### Policy Research

```
# Chinese policy
policy_name site:gov.cn

# International
policy_name "white paper" site:gov
```

---

## Quick Reference Card

| Task | Syntax |
|------|--------|
| Government source | `site:gov.cn` |
| Company filing | `site:cninfo.com.cn` |
| Academic paper | `filetype:pdf` |
| GitHub code | `site:github.com` |
| Exact phrase | `"search term"` |
| Exclude term | `-exclude` |
| Recent news | `tbs=qdr:m` |
| Privacy search | Use DuckDuckGo |

---

*Use this reference to construct precise searches that return authoritative results.*
