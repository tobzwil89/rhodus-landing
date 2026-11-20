# rhodus-landing – öffentliche Testseite von Rhodus

Nur die fertig gebaute Startseite mit Warteliste, ausgeliefert über GitHub Pages auf **https://rhodus.tobiaszwilling.me**.
Quelle ist `~/Desktop/Claude/rhodus-test/web/` (React/Vite). Hier wird nichts von Hand geändert.

## Neu veröffentlichen

1. In `rhodus-test`: `sh web/ausliefern.sh` (baut und kopiert nach `docs/`, `CNAME` und `.nojekyll` bleiben stehen).
2. Hier: `git add docs && git commit -m "Seite neu gebaut" && git push`. Tobias pusht selbst.

## Aufbau

- `docs/` = Inhalt der Seite (GitHub Pages: Branch `main`, Ordner `/docs`), `docs/CNAME` = `rhodus.tobiaszwilling.me`.
- DNS bei Namecheap: CNAME `rhodus` → `tobzwil89.github.io`.
- Warteliste: Formular sendet direkt an Kit (`web/src/anmelden.ts`, `KIT_FORMULAR`), Double-Opt-in über Kit.
- Impressum und Datenschutz: `docs/impressum.html` (Quelle `web/public/impressum.html`).
- `noindex`: Google soll die Seite nicht anzeigen (Entscheidung Tobias 20.11.2026).

## Stand

- 20.11.2026: angelegt. Inhalt wie die lokale Testseite (Entscheidung Tobias: „Alles wie Testseite“, also auch inoffizielle
  Kennzahlen, Promi-Fotos, Börsenlogos; Risiken in `rhodus-test/web/VOR_LIVEGANG.md`). Preisseite und Gratis/Pro entfallen,
  stattdessen Warteliste.
- [x] Kit-Formular „Rhodus Warteliste“ (ID 10219810) eingetragen.
- [x] Repository tobzwil89/rhodus-landing, DNS bei Namecheap (geprüft 20.11.: zeigt auf GitHub).
- [ ] Pages-Quelle auf Ordner `/docs` stellen (stand auf `/`, Seite lag deshalb unter `/docs/`), danach HTTPS erzwingen.
