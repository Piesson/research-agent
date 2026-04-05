# Research Agent

A Claude Code-powered research assistant that explains essential concepts systematically.

## Features

- **Platonic Clarification**: Asks clarifying questions before diving into research
- **Hierarchical Analysis**: 5-level framework (Definition → Components → Relationships → Applications → Comparisons)
- **Bilingual Output**: Korean (systematic) + English (casual rhythmic)
- **Auto-Detection**: Automatically detects URLs, concepts, or topics
- **PDF Book Reading**: PDF → TXT 변환 후 챕터별 순차 요약 (토큰 제한 우회)

## Usage

```bash
cd ~/Desktop/research-agent
claude
```

Then use the `/research` command:

```
/research 블록체인
/research https://example.com/article
/research attention mechanism이 뭐야?
```

## PDF Book Reading

Large PDF files exceed token limits. Use this workflow:

```bash
# 1. Convert PDF to TXT
pdftotext "book.pdf" "book.txt"

# 2. Read chapter by chapter
# (Claude will use offset/limit to read portions)

# 3. Save to Notion
node ~/Desktop/notion-log-agent/index.js book "Book Title - Chapter X" "Summary..."
```

## Structure

```
research-agent/
├── CLAUDE.md                           # Agent behavior definition
├── .claude/
│   ├── commands/research.md            # /research command
│   └── skills/bilingual-output/SKILL.md  # Bilingual output skill
└── README.md
```

## Recent Changes

### 2026-01-19
- `eric-bahn-personal-profile.csv`: Updated

- `eric-bahn-personal-profile.csv`: Updated

- `ai-language-learning.csv`: Updated

- `eric-bahn-investments.csv`: Updated

- `hustle-fund-2025-2026.csv`: Updated

- `hustle-fund-portfolio.csv`: Updated



