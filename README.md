# InvoiceAI — Email to ERP Importer

> A live AI-powered app that reads invoice emails and extracts structured data for ERP import — no manual entry required.

Built as a product management portfolio project to demonstrate AI-augmented workflows in finance/accounts payable.

---

## What it does

1. **Select or paste** an invoice email (any format, any vendor template)
2. **AI extracts** invoice number, vendor, dates, line items, tax, totals, currency, payment method
3. **Export** as CSV or JSON — or simulate a push to your ERP system

Works with invoices in any layout, currency, or language.

---

## Live demo

👉 [View live on GitHub Pages](https://YOUR-USERNAME.github.io/invoice-ai-erp/)

---

## Deploy in 3 steps (GitHub Pages)

### 1. Create a new repository

Go to [github.com/new](https://github.com/new), name it `invoice-ai-erp`, set it to **Public**, click **Create repository**.

### 2. Upload the file

- Click **Add file → Upload files**
- Drag in `index.html`
- Commit directly to `main`

### 3. Enable GitHub Pages

- Go to **Settings → Pages**
- Under **Source**, select `main` branch and `/ (root)`
- Click **Save**

Your live URL will appear within ~60 seconds:
```
https://YOUR-USERNAME.github.io/invoice-ai-erp/
```

---

## How it works

The app calls the [Anthropic Claude API](https://docs.anthropic.com/) directly from the browser. Claude parses the raw email text and returns a structured JSON object with all invoice fields.

```
Raw email text
     ↓
Claude AI (claude-sonnet-4-6)
     ↓
Structured JSON: invoice_number, vendor, dates, line_items, tax, total
     ↓
Display + Export (CSV / JSON / ERP push)
```

---

## Features

- ✅ 3 sample invoice emails (USD, EGP, freelance formats)
- ✅ Custom email paste field — try your own invoices
- ✅ AI confidence score per extraction
- ✅ Flag system for missing fields (e.g. no VAT, unclear dates)
- ✅ Export to CSV or JSON
- ✅ Simulated ERP push with activity log
- ✅ Dark mode support
- ✅ Mobile responsive

---

## Tech stack

| Layer | Technology |
|-------|-----------|
| Frontend | Vanilla HTML/CSS/JS (single file, no build step) |
| AI | Claude Sonnet 4.6 via Anthropic API |
| Icons | Tabler Icons |
| Hosting | GitHub Pages |

---

## PM context

This project demonstrates:

- **Problem framing** — AP teams manually re-key invoice data into ERPs (SAP, Oracle, QuickBooks). This is slow, error-prone, and a clear automation opportunity.
- **Solution design** — AI extraction as a thin layer between email and ERP, preserving human review via confidence scores and flags before import.
- **Measurable value** — Time saved = (avg. invoice entry time) × (monthly invoice volume). Typical AP team saves 2–4 hrs/day.
- **Technical feasibility** — Demonstrated live, not hypothetical.

---

## License

MIT
