# Alexandrian Library

A personal library of knowledge: notes, explanations, checklists and worked examples across many fields, organized by the classical division of the sciences.

## Table of Contents

- [About](#about)
- [Purpose](#purpose)
- [Scope](#scope)
- [Knowledge domains](#knowledge-domains)
- [Full table of contents](#full-table-of-contents)
- [How to use this repository](#how-to-use-this-repository)
- [Reading the library](#reading-the-library)
- [Repository layout](#repository-layout)
- [Sources and migration](#sources-and-migration)
- [Contributing and working with AI agents](#contributing-and-working-with-ai-agents)
- [Status](#status)

## About

This repository collects what I learn, from mathematics and biology to finance, psychology, computer science and career skills. Each note explains one idea in plain English, with an example and a link to the sources. The notes are written so that they are still useful when I come back after a year, and so that someone new to the topic can follow them from top to bottom.

This is a personal knowledge base, not a tutorial site or a product. The goal is depth and correctness.

## Purpose

The repository exists to:

- build a durable reference that I can search, extend and trust,
- force real understanding by requiring every concept to be explained precisely, with examples and analogies,
- keep one consistent standard for how knowledge is written down, so the collection stays coherent as it grows,
- provide a source of truth that both people and AI assistants can work with under the same rules.

## Scope

**In scope**

- Concepts, mechanisms and the reasoning behind them, in any field listed below.
- Worked examples, exercises, comparisons, checklists and decision guides.
- Summaries of papers, books, documentation and talks, always in my own words and with a link to the source.

**Out of scope**

- Credentials, tokens, private keys, personal data or anything obtained from a real breach.
- Working malware, weaponized exploits or step by step guides aimed at real, unauthorized targets.
- Text copied wholesale from books, courses or articles.
- Personalized medical, legal or financial advice. Notes in those fields are educational.

## Knowledge domains

The top level follows the classical division of knowledge: formal, natural and social sciences, the humanities, applied sciences and the arts. Personal development has its own domain because it draws on all of them. Each domain has a `README.md` that lists its fields, and each field has a `README.md` that lists its planned topics. All domains are planned and have no notes yet.

| Domain | What it covers |
| --- | --- |
| [Formal sciences](formal-sciences/README.md) | Mathematics, logic, statistics and probability, theoretical computer science, decision and systems theory. |
| [Natural sciences](natural-sciences/README.md) | Physics, chemistry, biology, earth sciences, astronomy. |
| [Social sciences](social-sciences/README.md) | Psychology, economics, sociology, political science, law, anthropology, education, communication and media. |
| [Humanities](humanities/README.md) | Philosophy, history, linguistics and languages, literature, religion and mythology, archaeology. |
| [Applied sciences](applied-sciences/README.md) | Medicine and health, computer science (including cybersecurity), engineering, business and management, finance and investing. |
| [Arts](arts/README.md) | Visual arts, music, performing arts, design and architecture, photography. |
| [Personal development](personal-development/README.md) | Personal growth, skills (soft and hard) and career. |

Where a topic fits two domains, it has one home note and the other domain links to it. For example, the theory of algorithms lives under formal sciences, and programming practice lives under computer science.

## Full table of contents

[ToC.md](ToC.md) lists every file in the repository as an indented tree, with planned topics shown without links. Use it to see the whole structure at once. Use the domain and field READMEs for the recommended reading order.

## How to use this repository

- To learn a topic, open the domain, then the field, and read the notes in the order the field `README.md` gives.
- To look something up, start from [ToC.md](ToC.md) or search with `grep -rn "term" --include="*.md" .`.
- To find open gaps, run `grep -rn "^TODO:" --include="*.md" .`.

## Reading the library

This repository is set up for [Librarian OS](https://japonics.io), a reader for Markdown knowledge repositories. [librarian-os.json](librarian-os.json) names the project and lists the entry points (the seven domain directories). Librarian OS renders the notes in the browser with adjustable font size and font family, light, dark and sepia themes, search, a graph of the relations between notes and practice questions.

```bash
# in the librarian-os directory
npm install
npm run dev -- --repo /absolute/path/to/this/repository
```

The relations come from the sidecar files described in [GUIDELINE.md](GUIDELINE.md#35-sidecar-metadata): every `note.md` has a `note.md.json` next to it. The tools that keep them valid run from Librarian OS: `npm run check`, `npm run scaffold` and `npm run toc`, each with this repository's path as the argument.

## Repository layout

```text
ToC.md                  # full tree of every file
GUIDELINE.md            # rules for structure, note format and style
_sources/               # original exports that notes are migrated from
librarian-os.json       # configuration for Librarian OS (project name, entry points, rules)
_assets/<domain>/       # images, diagram sources and other files used by notes
<domain>/
    README.md           # fields in the domain
    <field>/
        README.md       # planned topics and notes in reading order
        <topic>.md      # a single note
        <topic>.md.json # its sidecar: node header and relations
```

The full rules for structure and naming are in [GUIDELINE.md](GUIDELINE.md#3-repository-structure-and-naming).

## Sources and migration

The directory [_sources](_sources) holds the original exports (HTML) that my earlier notes came from. They are written partly in Polish. Their content is translated into English and moved into the domain tree. [ToC.md](ToC.md) names the target field for each export. The exports are kept until the migration of a file is reviewed.

## Contributing and working with AI agents

All notes follow [GUIDELINE.md](GUIDELINE.md). It applies to people and to AI agents alike. Agent-specific entry points are [AGENTS.md](AGENTS.md) and [CLAUDE.md](CLAUDE.md). Both point to the GUIDELINE and do not repeat its rules.

## Status

The structure is in place and the notes are being migrated. Every area marked `(planned)` in [ToC.md](ToC.md) has a `README.md` and no notes.
