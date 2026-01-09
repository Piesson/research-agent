# Research Agent

A Claude Code-powered research assistant that explains essential concepts systematically.

## Features

- **Platonic Clarification**: Asks clarifying questions before diving into research
- **Hierarchical Analysis**: 5-level framework (Definition → Components → Relationships → Applications → Comparisons)
- **Bilingual Output**: Korean (systematic) + English (casual rhythmic)
- **Auto-Detection**: Automatically detects URLs, concepts, or topics

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

## Structure

```
research-agent/
├── CLAUDE.md                           # Agent behavior definition
├── .claude/
│   ├── commands/research.md            # /research command
│   └── skills/bilingual-output/SKILL.md  # Bilingual output skill
└── README.md
```
