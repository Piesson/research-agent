---
name: bilingual-output
description: Ensures all research outputs include both Korean (systematic) and English (casual rhythmic) explanations
---

# Bilingual Output Skill

This skill activates for ALL research-related outputs to ensure consistent bilingual formatting.

## Output Structure

Every explanation MUST include:

### 1. 한국어 섹션 (Korean Section)

**Style: 체계적 (Systematic)**

- Use clear hierarchy with headers
- Order: Core concept → Details → Examples
- Number/bullet points for logical flow
- Technical terms with English in parentheses: 머신러닝(Machine Learning)

**Template:**
```markdown
### 한국어

#### 핵심 정의
[1-2문장 핵심]

#### 주요 구성요소
1. **[요소 1]**: 설명
2. **[요소 2]**: 설명
3. **[요소 3]**: 설명

#### 작동 원리
[단계별 설명]

#### 실제 적용
- [예시 1]
- [예시 2]
```

### 2. English Section

**Style: Casual Rhythmic**

- Short punchy sentences. Then longer ones for flow.
- Use "you" and "we" freely
- Analogies are your friend: "Think of it like..."
- Conversational but accurate

**Template:**
```markdown
### English

**The gist?** [One-liner definition]

Here's the deal. [Core concept in casual terms]

**Key pieces:**
- **[Component 1]** - [casual explanation]
- **[Component 2]** - [casual explanation]

**How it actually works:**
[Step-by-step in conversational tone]

**Real talk:** [Practical implications, honest assessment]
```

## Activation Triggers

This skill activates when:
- `/research` command is used
- User asks for explanation of a concept
- Research output is being generated

## Quality Check

Before completing output, verify:
- [ ] Korean section exists with systematic structure
- [ ] English section exists with casual tone
- [ ] Both cover the same core content
- [ ] Technical accuracy maintained in both languages

## Tone Examples

**Korean (formal but clear):**
> 트랜스포머는 어텐션 메커니즘(Attention Mechanism)을 기반으로 하는 딥러닝 아키텍처입니다. 기존 RNN과 달리 병렬 처리가 가능하여 학습 속도가 빠릅니다.

**English (casual but precise):**
> Transformers? They're the architecture behind ChatGPT and pretty much every modern AI. The secret sauce is "attention" - letting the model look at all words at once instead of one by one. Way faster than the old approach.
