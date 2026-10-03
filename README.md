# Sample-Website-Projects-and-Bootcamps

**A project report on a collection of completed web development projects and bootcamp exercises.**

![Last Updated](https://img.shields.io/badge/last%20updated-October%202026-informational)
![License](https://img.shields.io/badge/license-MIT-green)

---

## 1. Executive Summary

This repository documents three web projects built to practise and demonstrate front-end development:

| # | Project | Completion | Outcome |
|---|---------|-----------|---------|
| 1 | Money Way Finance App | 100% | Original budget app audited, bugs fixed, and rebuilt as a premium finance website |
| 2 | Upsurge Consulting Site | 100% | Site rebuilt from an incomplete WordPress backup as a modern consulting website |
| 3 | Emmanuel Williams Portfolio | 75% | Personal portfolio in progress; live deployment needs verification |

The two completed projects follow the same pattern: start from an existing or partially broken codebase, identify the faults, and deliver a cleaner, faster, more polished result using plain HTML, CSS and JavaScript.

---

## 2. Project 1: Money Way Finance App

### Background
Money Way is a personal finance brand with the tagline *"Monitor your money on the go"*. The source material was a JavaScript budget tracker (a Budgety-style CRUD app) and a WordPress/Elementor marketing site, supplied as page exports and a database dump.

### Objectives
- Fix defects in the budget calculator
- Combine the marketing pages and the calculator into one coherent site
- Raise the visual quality to a premium standard

### Findings: defects in the original app
| Issue | Impact |
|-------|--------|
| Expense percentages hardcoded (`45%` header, `21%` on items, shown on income too) | Misleading figures |
| Amounts unformatted, no thousands separators | Hard to read |
| Click handler on the whole list container | Errors when clicking outside the delete button |
| Descriptions inserted with `innerHTML` | Script-injection risk |
| No Enter-key support, `alert()` for validation | Poor usability |
| Delete button visible only on hover | Unusable on touch devices |
| Fixed 1000px layout | Broken on phones and tablets |
| Insecure `http://` icon font, invalid duplicate `type` attribute, stray button, `icome__title` typo | Blocked resources and markup errors |
| No data persistence | Entries lost on refresh |

### Solution
- Rebuilt as a single responsive page with a working calculator
- Percentages calculated from real income; ₦ currency formatting; correct negative balances
- Plain-text rendering of user input, inline validation, Enter-key support, per-item delete
- Data saved to the browser's localStorage, plus a "Clear all" control
- Sections for services, why choose us, testimonials, about and a quote request form
- Light and dark themes, scroll animations, mobile-first layout

### Limitations
- Data is stored per device only; there is no account or server
- The contact form opens the visitor's email client rather than sending directly
- Original illustrations and the hero photo existed only inside PDF exports, so icons were used instead
- Contact details in the source pages were template placeholders and need confirming

**Stack:** HTML, CSS, JavaScript

---

## 3. Project 2: Upsurge Consulting Site

### Background
Upsurge EC is a consulting business whose website existed as an All-in-One WP Migration backup (`.wpress`, about 405 MB).

### Findings: state of the backup
- The archive was **truncated**: it ended partway through the WooCommerce plugin files with no end-of-archive marker
- It contained **no `database.sql`**, so all page content, menus and settings were unrecoverable
- Four entries had corrupted size fields; the other 20,313 files were recovered
- The only logged fatal error came from the Smart Slider 3 plugin
- The site was still in a "launching soon" state and carried unused theme demo content and a heavy plugin stack (Elementor, WooCommerce, Jetpack and others)

A faithful restore was therefore not possible.

### Solution
A new single-page site built from the recovered brand assets (UIC logo and team photos):
- Hero, services, process, team and contact sections
- Sticky navigation, scroll animations, responsive layout, light and dark themes
- No plugins or database, which removes the original failure points and improves load speed

### Limitations
- Services, statistics, tagline and contact email are **placeholder copy**; the original business content was lost with the database
- Three of four team members are labelled generically because their names were not recoverable
- The contact form uses an email link rather than a server

**Stack:** HTML, CSS, JavaScript

---

## 4. Project 3: Emmanuel Williams Portfolio

**Status:** about 75% complete.
**Intended live URL:** https://eewilliams.netlify.app/

### Deployment check
When this report was updated (4 October 2026), the URL above returned an **HTTP 404**. Possible causes include a paused or deleted Netlify site, a changed subdomain, or a missing `index.html` in the published folder. This should be resolved before the project is presented.

### Report details (to be completed)
- **Purpose and audience:** _add_
- **Pages and features built so far:** _add_
- **Technologies used:** _add_
- **Remaining work to reach 100%:** _add_

---

## 5. Technology Stack

HTML5 · CSS3 · JavaScript · React · Node.js · Git

Projects 1 and 2 use plain HTML, CSS and JavaScript only. React and Node.js are part of the wider repository stack; update this line once Project 3's stack is confirmed.

## 6. Method and Lessons Learned

1. **Audit before building.** Reading the original code and logs first exposed the real faults (hardcoded values, unsafe rendering, a truncated backup).
2. **Keep it simple.** Replacing a plugin-heavy WordPress stack with plain, self-contained pages reduced both complexity and risk.
3. **Verify backups.** An archive that cannot be fully restored is not a backup; always confirm the database is included.
4. **Never trust placeholder data.** Template phone numbers and sample copy must be replaced before launch.

## 7. Recommendations and Next Steps

- Fix or redeploy the Netlify site and finish Project 3
- Replace placeholder content on the Upsurge site with real business details
- Connect both contact forms to a form service (for example Netlify Forms)
- Add screenshots and live demo links to this README
- Take a fresh, verified backup of any live WordPress site, including its database

## 8. Getting Started

```bash
git clone https://github.com/<your-username>/Sample-Website-Projects-and-Bootcamps.git
cd Sample-Website-Projects-and-Bootcamps
npx serve <project-folder>
```

Each static project also opens directly by double-clicking its `index.html`.

## 9. License

Released under the [MIT License](LICENSE).

## 10. Author

**Emmanuel Williams**
