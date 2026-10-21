# The Indian Money Book

> **Everything About Personal Finance, Money, Law, and Freedom.**
> *Written for India, built for 2026.*

A complete, practical guide to personal finance for Indian readers, from your
first salary to your final retirement — covering legal savings, grey-zone tax
planning, the illegal traps you must avoid, and the family money conversations
no one tells you to have. The text is written in a plain, spoken style that is
safe for **text-to-speech** from start to finish.

---

## The book at a glance

- **Forty chapters** across **seven parts**
- **About ninety thousand words**
- **~193 pages** as a typeset PDF
- Fully text-to-speech ready (no tables, no unexplained jargon)
- Grounded in Indian reality: rupee figures, Indian banks, Indian tax rules,
  Indian cities, Indian family dynamics

### The seven parts

| Part | Chapters | Focus |
| ---- | -------- | ----- |
| One   | 1 – 5   | Foundations: myths, budget, emergency fund, credit score, psychology of money |
| Two   | 6 – 12  | Earning & borrowing: salary, side income, every loan type, marriage money, the money-instrument map |
| Three | 13 – 20 | Investing: mutual funds, index funds, stocks, bonds, PPF/EPF/NPS, real estate, gold, crypto |
| Four  | 21 – 24 | Tax: the two regimes, legal deductions, capital gains, filing the return |
| Five  | 25 – 31 | Protect & retire: health & life insurance, estate planning, parents, retirement, social security |
| Six   | 32 – 36 | Law & the grey zone: scams, legal-but-edgy strategies, the illegal zone, legal documents, family money |
| Seven | 37 – 40 | The 2026 landscape, a 90-day action plan, a 5-year roadmap, the lifelong money mindset |

The book closes with a **verified-data appendix** — the sourced numbers (tax
slabs, interest rates, scheme rules, legal positions) that back the figures in
the chapters, with confidence tags.

---

## Files

| File        | What it is |
| ----------- | ---------- |
| `book.md`   | The complete source of truth — one large, TTS-safe markdown document (all 40 chapters + appendix). |
| `book.pdf`  | A typeset, print-ready A4 version with a cover, chapter page breaks, and running page numbers. |

## Regenerating the PDF

The PDF is produced from `book.md` with a small Node + Playwright build that
splits the book into part/chapter sections, typesets them (serif body, cover,
per-chapter page breaks), and renders a Chromium PDF with a real page-number
footer.

The build tooling lives under `.agnes/` (ignored by git, not part of the book):

```
.agnes/work/finance-book/
├── book-header.md        # front matter + table of contents
├── part-01.md … part-07.md
├── research.md           # verified 2025-26 / 2026 numbers
├── assemble.js           # rebuilds book.md from the clean sources
├── pdf/
│   ├── build-book.js     # markdown -> HTML -> PDF
│   └── book.html / book.pdf
```

To rebuild after editing `book.md`:

```bash
cd .agnes/work/finance-book/pdf
npm install marked@15 playwright@1.62.1   # once
node build-book.js "C:/g/araf/book.md"
```

## License

The book is a personal work. Code and the typeset document are released under
the terms in `LICENSE`.

---

> **Disclaimer.** This book is educational, not legal, tax, or investment
> advice for your specific situation. Rates, slabs, and rules quoted reflect
> the financial year 2025–26 / the calendar year 2026 and change with every
> budget and court judgment. Confirm current official figures and consult a
> qualified chartered accountant, licensed advisor, or lawyer before acting.
> Nothing in this book is an instruction to break the law; the grey-zone and
> illegal-zone chapters exist so you can recognise the lines and stay on the
> right side of them.
