# ⬡ GOLD Investment Kalkulator

Ein vollständiger Browser-Kalkulator für das physische Gold-Investment-Modell mit monatlichen Auszahlungen, Treuebonus, Affiliate-System und interaktivem Zielrechner.

**→ [Live-Demo öffnen](https://svenn8n-a11y.github.io/gold-investment-kalkulator/)**

---

## Das Geschäftsmodell

| Parameter | Wert |
|-----------|------|
| Monatliche Auszahlung | 2 % des Kaufpreises (fixiert bei Kauf) |
| Laufzeit pro Position | 36 Monate (1 Zyklus) |
| Treuebonus nach 36 Monaten | 30 % des Kaufpreises (in EUR) |
| Gold-Lieferung nach 36 Monaten | Physisches Gold (Gramm zum Kaufkurs) |
| Affiliate-Provision | 1 % / Monat des Klienten-Kaufpreises (36 Monate) |
| Cash-ROI (garantiert) | **102 %** pro Zyklus (36 × 2 % + 30 % Bonus) |
| Gesamt-ROI inkl. Goldwertsteigerung | **≈ 108 %** bei ~2 % Gold/Jahr |

---

## Features

### 💰 Investitionen
- **Einmalinvestitionen** – beliebig viele, zu beliebigen Startzeitpunkten
- **Monatlicher Sparplan** – jede Rate startet einen eigenen 36-Monats-Zyklus
- **Monatliche Payout-Reinvestition** – automatische Wiederanlage jeder Auszahlung
- **Zyklus-Reinvestition** – am Ende jedes 36-Monats-Zyklus wird das gesamte Liquid-Kapital reinvestiert
- **Einmalige Entnahmen** – beliebige Auszahlungen zu geplanten Zeitpunkten

### 👥 Affiliates
- Mehrere Klienten anlegen
- Pro Klient mehrere Investitionspositionen mit unterschiedlichen Startterminen
- Automatische Berechnung der 1%-Provision für 36 Monate je Position

### 📊 Dashboard
- 8 KPI-Kacheln (investiertes Kapital, Cash-ROI, Gesamt-ROI, Erträge, Goldakkumulation, Gesamtvermögen)
- **4 interaktive Charts** (Chart.js):
  - Gesamtvermögen über Zeit (Kapital + Gold)
  - Monatliche Einnahmen nach Quelle (gestapeltes Balkendiagramm)
  - Goldakkumulation in Gramm + EUR-Wert
  - Einnahmen-Aufschlüsselung als Donut-Chart

### 📅 Zeitverlauf
- Vollständige Monatstabelle über alle Zyklen
- Bonus-Monate und Zyklusgrenzen farblich hervorgehoben
- Alle Spalten: Payouts, Boni, Affiliate, Entnahmen, Reinvestition, Goldlieferung, Salden

### 🎯 Zielrechner
- Zielbetrag + Zielgröße (Liquidität / Gesamtvermögen / monatliche Einnahmen) frei wählbar
- **Kombinations-Rechner**: Einmaleinlage + Ratenzahlung + Affiliates gleichzeitig konfigurierbar
- Zielerreichungsmonat (mit/ohne Reinvestition)
- Optimierungsberechnung: Was brauche ich für den Zielbetrag in X Monaten?
  - Nur Einmaleinlage
  - Nur monatliche Rate
  - Nur Affiliates (à 1.000 / 5.000 / 10.000 €)

### ⚙️ Einstellungen
- **Live-Goldpreis** (via metals.live API + EUR/USD-Kurs)
- **Goldpreis-Projektionsregler** (0–15 % p. a.)
- **Zyklen-Regler** (1–5 Zyklen = 36–180 Monate)

---

## ROI-Erklärung

```
Cash-ROI (garantiert, unabhängig vom Goldpreis):
  36 Monate × 2 %/Monat = 72 %
  + 30 % Treuebonus      = 30 %
  ─────────────────────────────
  Gesamt Cash-ROI        = 102 %

Gesamt-ROI inkl. Gold (bei 2 % Goldpreissteigerung/Jahr):
  Cash-ROI               = 102 %
  + Goldwertzuwachs 3J   ≈   6 %  (1,02³ − 1)
  ─────────────────────────────
  Gesamt-ROI             ≈ 108 %
```

---

## Technologie

| | |
|---|---|
| **Frontend** | Vanilla HTML / CSS / JavaScript |
| **Charts** | [Chart.js 4.4](https://www.chartjs.org/) (CDN) |
| **Goldpreis API** | [metals.live](https://metals.live) + [frankfurter.app](https://www.frankfurter.app) |
| **Deployment** | GitHub Pages (Single-File, kein Build-Schritt) |

---

## Lokale Nutzung

Einfach `index.html` im Browser öffnen – keine Installation, kein Server nötig.

```bash
git clone https://github.com/svenn8n-a11y/gold-investment-kalkulator.git
cd gold-investment-kalkulator
open index.html   # macOS
# oder: start index.html (Windows)
```

---

## Lizenz

MIT – frei nutzbar und anpassbar.
