<div align="center">

<br />

# Tables

**A fast, native database client for modern developers.**

Connect to PostgreSQL, SQLite, MySQL, MongoDB, and Redis — with an AI agent built right in.

<br />

[![Latest Release](https://img.shields.io/github/v/release/been-there-done-that/tables-releases?label=latest&color=6d28d9&style=flat-square)](https://github.com/been-there-done-that/tables-releases/releases/latest)
[![Platform](https://img.shields.io/badge/platform-macOS%20%7C%20Windows%20%7C%20Linux-6d28d9?style=flat-square)](#download)
[![License](https://img.shields.io/badge/license-MIT-6d28d9?style=flat-square)](#)

<br />

</div>

---

## Download

Head to the [**Releases**](https://github.com/been-there-done-that/tables-releases/releases) page and grab the build for your platform.

| Platform | File |
|---|---|
| macOS (Apple Silicon) | `tables_x.x.x_aarch64.dmg` |
| macOS (Intel) | `tables_x.x.x_x64.dmg` |
| Windows | `tables_x.x.x_x64-setup.exe` |
| Linux | `tables_x.x.x_amd64.AppImage` |

> Releases are signed. macOS builds are notarized.

---

## What is Tables?

Tables is a cross-platform desktop database management app built with **Tauri 2** and **SvelteKit**. Think DataGrip — but lighter, faster, and with an AI agent that understands your schema.

```
Native Rust backend  ·  Monaco SQL editor  ·  Schema explorer  ·  AI assistant
```

### Supported Databases

| | Database | Status |
|---|---|---|
| 🐘 | PostgreSQL | Full — streaming, cursors, query cancellation |
| 🪶 | SQLite | Full |
| 🐬 | MySQL | Supported |
| 🍃 | MongoDB | Supported |
| 🔴 | Redis | Supported |

---

## Features

**SQL Editor**
- Monaco-based editor with SQL syntax highlighting and auto-complete
- Real-time diagnostics via the PostgreSQL C parser (`pg_query`) — syntax errors, unknown tables, dangerous queries
- Per-statement run buttons — execute one query at a time without selecting text
- Format, undo/redo, multi-tab editing

**Schema Explorer**
- Browse databases, schemas, tables, views, functions, sequences, indexes, and foreign keys
- Click any table to preview data instantly with editable grid
- Inline DDL viewer for any object

**AI Agent**
- Conversational agent with live schema awareness
- Tools: `run_query`, `list_tables`, `get_schema`, `explain_query`, file read/write
- Powered by Claude via a lightweight Bun sidecar — no Node.js required

**Performance**
- Rust backend — no Electron overhead
- Virtualized data grid handles millions of rows
- Server-side cursors for large result sets

---

## Source

The source code lives at [`been-there-done-that/tables`](https://github.com/been-there-done-that/tables).
This repository is the release distribution channel only.

---

<div align="center">
<sub>Built with Tauri · SvelteKit · Rust · Bun</sub>
</div>
