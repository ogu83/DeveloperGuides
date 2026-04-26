# Copilot Instructions
This repository is a curated collection of software engineering reference guides distilled from respected CS and software books. It is a pure-markdown, documentation-only repository — there are no build, test, or lint tools.

## Two Types of Files
Files fall into two distinct categories:

### 1. LLM/Developer-Targeted Reference Guides (authoritative, indexed)
Hand-crafted, well-structured guides listed in README.md. These are the primary deliverables of this repo:
- Comprehensive_Algorithm_Guide_for_LLM.md
- Database_Tuning_Reference.md
- Practical_Debugging_DotNet_Reference.md
- Refactoring_Guide_for_LLM_Agents.md

### 2. Book Transcriptions (raw source material)
PDF-to-markdown conversions of CS textbooks. Many contain OCR artifacts, ----- page-break separators, and unformatted content. These serve as source material for creating new guides, not as polished references:
- Algorithms.md, Algorithms for Programmers.md, Algorithm Analysis and Computational Complexity.md, Graph Theory.md, Graph Theory with Applications.md, Knapsack Problems.md, Introduction to Algorithms.md, Introduction to Algorithms Solutions.md, Problems on Algorithms.md, The Complexity of Boolean Functions.md

## Conventions for Reference Guides
When creating or editing a reference guide, follow the established format used in the existing guides:

File naming: Title_Case_With_Underscores.md for new reference guides.

Document structure:
```markdown
# [Topic] Reference Guide   (or: # [Topic] for LLM Agents)

> A comprehensive reference for [purpose], based on "[Book Title]" by [Author]

---

## Table of Contents

1. [Section Name](#1-section-name)
2. [Section Name](#2-section-name)

---

## 1. Section Name

### Subsection

| Column | Column |
|--------|--------|
| **Term** | Description |

---
```

Key formatting rules:
- Use --- horizontal rules to separate top-level sections
- Use > blockquote at the top to attribute the source book
- Use markdown tables (| col | col |) for comparisons, tools lists, and quick references
- Bold key terms inline with term
- Use numbered TOC entries with lowercase anchor links (e.g., #1-section-name)
- End guides with a "Quick Reference" section summarizing the most actionable content
- Include code blocks (` ``` `) for algorithms, commands, or formal notation

## Adding New Guides
New guides should be:
1. Created in the root directory (not subdirectories)
2. Added to the README.md Guides list with a brief description
3. Based on a named source book (cite it in the opening blockquote)
4. Structured with a numbered TOC and ----separated sections
