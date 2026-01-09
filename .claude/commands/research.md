---
description: Unified research command - auto-detects URLs, concepts, or topics
---

# Research: $ARGUMENTS

## Phase 1: Input Analysis

Analyze the input type:
- **URL pattern** (https://...) → Fetch and analyze the page
- **Question pattern** ("뭐야", "뭔가요", "what is", "explain") → Direct concept explanation
- **Other** → Topic research via web search

## Phase 2: Platonic Clarification

**MANDATORY EVALUATION** - Write this explicitly:

```
질문 필요 여부: [YES/NO]
이유: [brief reason]
```

If YES, ask 1-3 questions:
1. **범위/Scope**: Which aspect? (theory/practice/history/comparison)
2. **깊이/Depth**: Overview or deep-dive?
3. **목적/Purpose**: Any specific use case?

**Wait for user response before proceeding.**

## Phase 3: Information Gathering

Based on input type:

### For URLs:
```
Use WebFetch to retrieve and analyze the content
Extract: Main thesis, key arguments, supporting data
```

### For Concepts:
```
Use existing knowledge + WebSearch if needed
Focus on fundamental understanding
```

### For Topics:
```
Use WebSearch for current information
Query: "[topic] 2025 comprehensive guide"
Gather 3-5 authoritative sources
```

## Phase 4: Hierarchical Analysis

Apply the 5-level framework:

```
Level 1: 정의 - One sentence core definition
Level 2: 구성요소 - 3-5 key components
Level 3: 관계 - How components interact
Level 4: 적용 - Real-world applications
Level 5: 비교 - vs alternatives
```

Identify the vital 20% that explains 80%.

## Phase 5: Bilingual Output

Generate BOTH sections:

### 한국어
- 체계적 계층 구조
- 핵심 먼저
- 전문용어 영어 병기

### English
- Casual, rhythmic flow
- Short sentences mixed with longer explanations
- Analogies for complex concepts

## Phase 6: Visualization (if helpful)

Use ASCII/text diagrams when appropriate:
- Concept hierarchies
- Process flows
- Comparison tables

Example:
```
┌─────────────┐
│  Core Idea  │
└──────┬──────┘
       │
   ┌───┴───┐
   │       │
┌──▼──┐ ┌──▼──┐
│ A   │ │ B   │
└─────┘ └─────┘
```

## Phase 7: Follow-up

Ask:
- "더 깊이 파고 싶은 부분이 있나요?"
- "Notion에 저장할까요?"
