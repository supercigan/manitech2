# DNA — MANITECH Uherské Hradiště

**Typ projektu:** Jednostránkový web komplexního autoservisu (landing page)
**Klient:** MANITECH Uherské Hradiště s.r.o. — autoservis, karosárna, lakovna
**Datum dokončení:** 2026-03-26
**GitHub:** supercigan/manitech2

---

## Vizuální archetype

**Corporate Precision** — Deep charcoal (#0F1117) s electric blue (#3563E9). Žádná amber, žádná červená, žádná zelená. Modrá jako jediný akcent evokuje důvěru a preciznost — sedí k firmě která je smluvním partnerem 10+ pojišťoven a používá prémiovou Spies Hecker technologii. Celkový dojem: velký profesionální servis, ne „garáž za rohem".

---

## Barevná paleta

| Proměnná       | Hex       | Role                                    |
|----------------|-----------|-----------------------------------------|
| `--deep`       | `#0F1117` | Hero, nav scrolled, kontakt, footer     |
| `--deep-mid`   | `#131722` | Pojišťovny sekce                        |
| `--deep-soft`  | `#1A1F2E` | Sluzby karty pozadí                     |
| `--blue`       | `#3563E9` | Primární akcent — vše: CTA, labels, bordery |
| `--blue-d`     | `#2A50D0` | Hover stav blue                         |
| `--blue-l`     | `#EEF2FF` | Světlé blue plochy, ikony bg            |
| `--blue-ll`    | `#F5F7FF` | Extra světlé blue pozadí                |
| `--light`      | `#F7F8FB` | Světlé sekce (detail, tým)              |
| `--mid`        | `#ECEEF4` | Střední prvky                           |
| `--white`      | `#FFFFFF` | Čistá bílá (o nás sekce)                |
| `--text-dark`  | `#0F1117` | Hlavní text                             |
| `--text-mid`   | `#4B5563` | Sekundární text                         |
| `--text-light` | `#9CA3AF` | Potlačený text                          |
| `--border`     | `#E5E7EF` | Bordery na světlém                      |

**Charakter palety:** Jediný akcent = electric blue. Žádný sekundární teplý tón. Modrá = důvěra + preciznost.

---

## Typografie

| Řez     | Font      | Použití                                       |
|---------|-----------|-----------------------------------------------|
| Nadpisy | Syne      | H1–H4, nav logo, section labels, tlačítka     |
| Tělo    | Outfit    | Odstavce, popisky, formulář, tagy             |

- H1: `clamp(2.6rem, 5.5vw, 4.8rem)`, weight 800, italic `<em>` pro třetí řádek
- H2: `clamp(2rem, 4vw, 3rem)`, weight 700
- H3: `clamp(1.15rem, 2vw, 1.4rem)`, weight 700
- Section label: **pill badge** — `padding: 5px 14px`, `border-radius: 100px`, `rgba(53,99,233,0.1)` bg, `border: 1px solid rgba(53,99,233,0.25)`, 0.7rem, letter-spacing 0.2em, uppercase
- **Nav logo text: 1.65rem / 800** — osvědčená proporce
- Tlačítka: Outfit 0.95rem weight 600, border-radius 8px

---

## Layout a struktura sekcí

```
1. NAV           — Fixed průhledný → deep při scrollu, hamburger na mobilu
2. HERO          — Dark deep, radial glow (blue 18% bottom-left + 7% top-right),
                   dot grid (40px, opacity 0.6), diagonal clip-path panel (42% width),
                   badge "Fungujeme od roku 2000" s pulsujícím tečkovým indikátorem,
                   H1 s italic em na 3. řádku, 2 CTA (blue primary + ghost),
                   hero-info-bar (adresa/tel/hodiny), hodiny karta vpravo
3. TRUST STRIP   — 3px blue border-top, bílé pozadí, 4 karty: 25+ let / 10+ pojišťoven /
                   Spies Hecker (hvězda) / 800 44 66 88
4. SLUZBY        — Dark deep, 2×2 grid, 4 karty: Autoservis / Pneuservis /
                   Autolakovna / Karosárna+Pojistné. Hover: bottom border scaleX(0→1)
5. DETAIL        — Light, 4×2 grid, 8 karet konkrétních služeb s ikonami
6. POJIŠŤOVNY    — Dark deep-mid, split intro (text + "Jak to funguje" karta),
                   10 partnerů v 5×2 gridu (text badges)
7. TÝM           — White, 3 karty, iniciálové avatary (PP/PV/PT) v blue kroužku
8. O NÁS         — Light, split: text+features vlevo / map card vpravo
9. KONTAKT       — Dark deep, split: info panel vlevo / formulář vpravo
10. FOOTER       — #0A0C12, 3 sloupce: logo+popis | nav | kontakt
```

---

## Klíčové UI vzory

- **Section label (pill badge):** `display:inline-flex`, `border-radius:100px`, modrý border + bg — ODLIŠNÉ od všech ostatních DNA (které mají left-border linku)
- **Hero radial glow:** `radial-gradient(ellipse 70% 60% at 15% 110%, rgba(53,99,233,0.18))` — žádné canvas, žádný ghost text
- **Hero dot grid:** `background-image: radial-gradient(rgba(53,99,233,0.12) 1px, transparent 1px)`, `background-size: 40px 40px`
- **Hero diagonal panel:** `clip-path: polygon(15% 0, 100% 0, 100% 100%, 0% 100%)`, 42% width, subtle blue gradient
- **Hero badge:** pill s pulsujícím tečkovým indikátorem (CSS animation `pulse`)
- **Sluzba karta hover:** `bottom border scaleX(0→1)` animate — bottom sliding underline
- **Team avatary:** iniciály (PP/PV/PT) v 80px blue bordered kroužku — ne SVG postava
- **Pojišťovny grid:** čistý text v hover-activatable cells — bez log (loga nejsou k dispozici)
- **Fade-up animace:** IntersectionObserver, delay třídy d1–d6 (0.1–0.6s)
- **Watermark:** `position:fixed`, 5×7 grid (35 opakování), `rotate(-30deg)`, `opacity: rgba(0,0,0,0.09)`, text "Demoverze – Tomáš Smolík"
- **Tlačítka:** `border-radius: 8px`, primary s `box-shadow: 0 4px 20px rgba(53,99,233,0.35)`

---

## Technický stack

- Čistý HTML/CSS/JS — jeden soubor `index.html`
- Google Fonts (Syne + Outfit)
- Formulář: lokální simulace (bez odesílání) — Formspree lze přidat
- Deploy: GitHub → supercigan/manitech2 → Vercel

---

## Co se osvědčilo

- **Electric blue jako jediný akcent** — v kontextu DNA portfolia zcela unikátní (jiné mají amber, červenou, zelenou, bronz)
- **Pill badge jako section label** — svěží alternativa k left-border linii, moderní SaaS look
- **Radial glow hero** — čistší než canvas animace nebo ghost text, načítá se okamžitě
- **Trust strip s 3px blue border-top** — silné vizuální napojení na hero a rychlé reason-why
- **Pojišťovny jako samostatná sekce** — silný selling point firmy, zaslouží vlastní prostor
- **Iniciálové avatary** — lepší než generická SVG postava, osobnější než placeholder ikona
- **Watermark 5×7 grid** — rovnoměrné pokrytí stránky, profesionálnější než jedno velké diagonální

## Co se nepovedlo / co příště udělat jinak

- Výměna čelního skla ikona byla opravována vícekrát — SVG přední okno auta je těžce rozpoznatelné v 20px, příště použít jednodušší tvar
- Brzdové centrum a Podvozkové centrum mají slabé ikony (list/bars) — nepůsobí automotive
- Screenshoty z _screenshots/ nepatří do gitu — přidat do .gitignore
