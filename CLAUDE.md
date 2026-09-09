# Festival Planner

## Project Goal

Wir entwickeln einen minimalistischen Festival-Planer für Festivalbesucher.
"Wo ist was wann?"
## Tech Stack

* FastAPI
* SQLAlchemy
* SQLite
* HTML
* JavaScript

## Functional Requirements

Die MVP-Anforderungen (Muss / optional / Benutzeraktionen / Scope-Abgrenzung) sind in
[`doc/requirements.md`](doc/requirements.md) definiert.

Kurzfassung: Ein eintägiges Festival, Programm als chronologische Liste, Filter nach Bühne,
Anzeige „läuft jetzt / kommt als Nächstes". Daten per Seed, kein Login. Bewusst so klein
wie möglich, aber im Datenmodell auf Mehrtägigkeit vorbereitet.

## Architecture

TODO

## Domain Model

Vollständig in [`doc/domain-model.md`](doc/domain-model.md).

Kurzfassung: Genau eine Entität `ProgramItem` mit `id`, `title`, `stage` (String),
`starts_at`, `ends_at` (volle Zeitstempel). Nur diese Tabelle wird persistiert.
„Läuft jetzt / kommt als Nächstes", Sortierung und Bühnenliste werden zur Laufzeit
berechnet bzw. abgeleitet. Keine Festival-, Stage- oder User-Entität im MVP.

## Development Rules

* Keep the application small and focused.
* Do not add unnecessary frameworks or dependencies.
* Analyze requirements before implementing changes.
* Keep the existing project structure and coding style consistent.
* Write simple, readable code.
* Add tests for important business logic.
* Document important decisions and non-obvious code.
* Review existing code before making larger changes.

## Working with Claude

* Analyze the existing project before making changes.
* Prefer small, incremental changes.
* Explain larger structural changes before implementing them.
* Do not introduce new dependencies without a clear reason.
* Do not implement functionality that is not part of the agreed requirements.
* Ask for clarification when requirements are ambiguous.
* Update this file when important project decisions change.

## Project Commands

### Install dependencies

```bash
pip install -r requirements.txt
```

### Start backend

TODO

### Run tests

TODO

## Teaching Material

Files in `teaching/` are intended for participants only.

Do not read, analyze, summarize, or use files from this directory unless the user explicitly asks for it.

For you teaching/ is write only. When ever you think you have interesting information for teaching you can add it to teaching/