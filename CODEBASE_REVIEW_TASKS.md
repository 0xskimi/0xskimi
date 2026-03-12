# Codebase review: proposed tasks

## 1) Typo fix task
**Issue found:** The sentence "Building a crypto + fiat wallet that makes money simple." is less natural/clear than intended product messaging.

**Task:** Update the README copy to "Building a crypto + fiat wallet that makes managing money simple." to fix wording/typo-level clarity.

**Why:** Improves readability and avoids awkward phrasing in the repository's primary description.

**Done when:** README contains the updated sentence and no grammar checker flags the line.

---

## 2) Bug fix task
**Issue found:** The Twitter/X profile URL uses `https://www.x.com/0xskimi/`. `www.x.com` can produce inconsistent behavior depending on clients and link unfurlers.

**Task:** Replace the URL with canonical `https://x.com/0xskimi`.

**Why:** Reduces risk of broken links in markdown renderers and improves portability for static-site/link validators.

**Done when:** README link resolves to the same profile in browser and via a markdown link checker.

---

## 3) Documentation discrepancy task
**Issue found:** README says "Currently building Incore" but does not explain whether this repo is source code for Incore, a profile repo, or a placeholder.

**Task:** Add a short "About this repository" section clarifying scope (e.g., personal profile/landing README vs product code repo).

**Why:** Aligns reader expectations and removes ambiguity about missing source code.

**Done when:** README includes a section explicitly stating repo purpose and where product code lives (if elsewhere).

---

## 4) Test improvement task
**Issue found:** No automated checks exist for README integrity.

**Task:** Add a lightweight CI check for markdown quality and links (e.g., markdownlint + markdown-link-check or lychee) that runs on pull requests.

**Why:** Prevents regressions in public-facing content and catches future typos/broken links automatically.

**Done when:** CI job runs on PRs and fails on markdown/style/link errors.
