<div align="center">

<br />

# Tables

**A fast, native database client for modern developers.**

Connect to PostgreSQL, SQLite, MySQL, MongoDB, and Redis — with an AI agent built right in.

<br />

[![Latest Release](https://img.shields.io/github/v/release/been-there-done-that/tables-releases?label=latest&color=6d28d9&style=flat-square)](https://github.com/been-there-done-that/tables-releases/releases/latest)
[![Platform](https://img.shields.io/badge/platform-macOS%20%7C%20Windows%20%7C%20Linux-6d28d9?style=flat-square)](#%EF%B8%8F-download)
[![License](https://img.shields.io/badge/license-MIT-6d28d9?style=flat-square)](#)

<br />

</div>

---

## ⬇️ Download

Go to the [**Releases**](https://github.com/been-there-done-that/tables-releases/releases/latest) page and download the file for your operating system.

| Operating System | File to download |
|---|---|
| macOS — Apple Silicon (M1/M2/M3/M4) | `tables_0.0.3_aarch64.dmg` |
| macOS — Intel | `tables_0.0.3_x64.dmg` |
| Windows | `tables_0.0.3_x64-setup.exe` |
| Linux | `tables_0.0.3_amd64.AppImage` |

> **Not sure which Mac you have?** Click the Apple menu → **About This Mac**. If it says "Apple M1" or later, download `aarch64`. If it says Intel, download `x64`.

---

## 🚀 Install & Launch

### macOS
1. Download the `.dmg` file
2. Double-click it to open
3. Drag **Tables** into your **Applications** folder
4. Open **Applications** and double-click **Tables**

> **"Tables can't be opened because Apple cannot check it for malicious software"?**  
> Right-click the app → **Open** → click **Open** again. This only happens once.

### Windows
1. Download the `-setup.exe` file
2. Double-click it and follow the installer
3. Tables will appear in your Start Menu when done

> Windows may show a SmartScreen warning — click **More info → Run anyway**.

### Linux (AppImage)
1. Download the `.AppImage` file
2. Make it executable and run:
   ```bash
   chmod +x tables_0.0.3_amd64.AppImage
   ./tables_0.0.3_amd64.AppImage
   ```

---

## 🗄️ Try It — Connect a SQLite Database in 3 Steps

No database? No problem. Download our sample file and you'll have data to explore in under a minute.

### Step 1 — Download the sample database

**[⬇ Download sample.db](https://github.com/been-there-done-that/tables-releases/raw/main/sample.db)**

It contains three tables — `customers`, `products`, `orders` — and a pre-built `order_summary` view, all pre-loaded with data.

### Step 2 — Connect it in Tables

1. Launch **Tables**
2. Click **Connect** in the top toolbar
3. Select **SQLite** as the database type
4. Click the folder icon and navigate to `sample.db`
5. Click **Connect**

That's it. You're in.

### Step 3 — Start exploring

The schema explorer on the left lists all tables. Click any one to preview its data instantly.

Open the **Query** tab and try some SQL:

```sql
-- All orders with customer and product names
SELECT * FROM order_summary;
```

```sql
-- Top spending customers
SELECT customer, SUM(total) AS total_spent
FROM order_summary
GROUP BY customer
ORDER BY total_spent DESC;
```

```sql
-- Products running low on stock
SELECT name, category, stock
FROM products
WHERE stock < 100
ORDER BY stock ASC;
```

---

## 🔌 Connect PostgreSQL / MySQL / MongoDB / Redis

1. Click **Connect** in the top toolbar
2. Select your database type from the list
3. Fill in your connection details and click **Save**

Default ports for reference:

| Database | Default port |
|---|---|
| PostgreSQL | `5432` |
| MySQL | `3306` |
| MongoDB | `27017` |
| Redis | `6379` |
| SQLite | *(file path — no port needed)* |

---

## ✨ What's inside

**SQL Editor** — Monaco-based editor with syntax highlighting, auto-complete, real-time error detection, per-statement run buttons, format, and multi-tab editing.

**Schema Explorer** — Browse every database object: tables, views, functions, sequences, indexes, foreign keys. Click any table for a live data preview. Click any object to see its DDL.

**AI Agent** — Ask questions about your data in plain English. The agent reads your live schema, runs queries, and writes SQL for you. Powered by Claude.

**Supported databases** — PostgreSQL · SQLite · MySQL · MongoDB · Redis

---

## 💬 Feedback & Issues

Found a bug or have a request? Open an issue in the [source repository →](https://github.com/been-there-done-that/tables/issues)

---

<div align="center">
<sub>Built with Tauri · SvelteKit · Rust · Bun</sub>
</div>
