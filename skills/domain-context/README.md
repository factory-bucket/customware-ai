# domain-context

**Progressive Domain Crystallization (PDC)** — a skill for building and maintaining a living domain knowledge base for any custom business application.

## What It Does

Enables any AI assistant to accumulate understanding of internal terminology, entities, relationships, and business rules over time through a human-AI collaborative protocol.

The AI reads a structured `DOMAIN.md` file at the start of every session, uses domain terminology exactly as defined, flags gaps inline during work, and proposes structured updates for human review at session end.

## Key Features

- **Living knowledge base** — grows incrementally across sessions, never auto-modified
- **Progressive disclosure** — three-tier system (Core / Working Context / Archive) that scales from a single 60-line file to a multi-file domain model
- **Human-in-the-loop governance** — AI proposes updates, humans review and apply
- **Template-driven** — blank DOMAIN.md template with tier annotations, ready to initialize
- **Anti-pattern awareness** — documented failure modes for both AI and human participants

## Installation

```bash
npx skills add customware-ai/skills --skill domain-context
```

## File Structure

```
domain-context/
├── SKILL.md                         ← Main skill instructions
├── assets/
│   └── templates/
│       └── DOMAIN.md                ← Blank template to initialize a new domain
└── references/
    ├── seed-questions.md            ← Questions to bootstrap a new domain
    ├── entity-template.md           ← Template for individual entity files
    └── anti-patterns.md             ← Common mistakes to avoid
```

## License

MIT

