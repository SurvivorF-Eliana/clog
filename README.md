# Changelog Toolkit

---

## Tools

| Tool | File | Purpose | Added |
|------|------|---------|-------|
| **Changelogs Maker** | `changelogs-maker.html` | Manual entries · dual timestamps (local + client −2h) · path cleaner · export MD/CSV | ⛔ |
| **Changelog Watcher** | `changelog-watcher/watcher.js` | Live filesystem watch · CREATE / MODIFY / DELETE / RENAME · session notes · detailed log | ⛔ |
| **Changelog Reviewer** | `changelog-reviewer.html` | Parse `detailed-changelog.md` · strip noise · folder cards · client summary · export | 👍 |

---

## Quick start

### Reviewer (clean the choclo)

Open `changelog-reviewer.html` in a browser.

1. Paste or **LOAD_FILE** → `detailed-changelog.md`
2. Toggle filters:
   - `STRIP_NOISE` — collapses CodeLockPerms spam, journals, RPT/log mass deletes
   - `DEDUPE` · `NOTES` · `SESSIONS` · `CLIENT_SUMMARY`
3. **EXECUTE**
4. **EXPORT_MD** / **EXPORT_CSV** / **COPY**

---

## Log formats

### Watcher detail (folder-grouped)

```text
📂 `dayzOffline.chernarusplus/db`
   • ✏️ **[MODIFY]** `types.xml`  · 2026-07-26 04:10:01
   • ✨ **[CREATE]** `types.xml.bak`  · 2026-07-26 04:10:02
```

### Maker / client table

| Local TS | Client TS (−2h) | Changed By | File Path | Action | Backup | Before | After | Validation | Rollback | Approval | Notes |
|----------|-----------------|------------|-----------|--------|--------|--------|-------|------------|----------|----------|-------|

---

## Scope reminder

**Allowed (with backup)**
- `mpmissions/.../expansion/market/*.json`
- `expansion/settings/*trader*` / safezone
- `db/types.xml` · `cfgspawnabletypes.xml` (conditional)
- `logos/`

---

## Stack

- HTML / CSS / vanilla JS (maker + reviewer)
- Font: [Host Grotesk](https://fonts.google.com/specimen/Host+Grotesk)

---

## License / confidentiality

Internal tooling for DayZ handoff.
Server configs, credentials, and modlists in related workbooks are confidential under NDA.
