# MANITECH UH — Project Summary

**Datum zahájení:** 2026-03-26
**Datum dokončení:** 2026-03-26
**Klient:** MANITECH Uherské Hradiště s.r.o.
**Původní web:** https://manitech-uh.cz/
**GitHub:** https://github.com/supercigan/manitech2

---

## Co je hotovo

- [x] Přečteny DNA soubory všech 5 předchozích projektů
- [x] Screenshoty a analýza původního webu manitech-uh.cz
- [x] Zvolena unikátní vizuální identita
- [x] Vytvořen index.html — kompletní jednostránkový web
- [x] Opraveny špatné ikony (Spies Hecker, Autolakovna, Diagnostika, Pneuservis, Sklo, Odtah)
- [x] Opraveny výšky karet (sluzby grid, tým grid)
- [x] Opraveny avatary týmu (iniciály PP/PV/PT)
- [x] Přidán footer logo icon
- [x] Upraven spacing sekcí
- [x] Přidán watermark (5×7 grid, "Demoverze – Tomáš Smolík", -30°, opacity 9%)
- [x] GitHub push — repo: supercigan/manitech2

---

## Co se řeší

- [ ] DNA soubor — hotovo viz níže

---

## Důležitá rozhodnutí

### Vizuální identita
- **Fonty:** Syne (nadpisy) + Outfit (tělo) — žádný z předchozích projektů je nepoužil
- **Paleta:** Electric blue #3563E9 na deep charcoal #0F1117 — jediný projekt s modrou jako primárním akcentem
- **Section label:** modrý pill badge (inline, border-radius 100px) — jiné projekty používají left-border linie
- **Hero dekorace:** CSS radial glow effect + dot grid + diagonal clip-path panel
- **Watermark:** 5×7 grid opakování (35×), rotate -30°, opacity 9%

### Informace z původního webu (reálné údaje)
- **Adresa:** Moravníky 1392, 686 01 Uherské Hradiště (areál UHS JAKOS, Maratice)
- **Telefon:** +420 800 44 66 88 (bezplatná linka)
- **Email:** servis@manitech-uh.cz / nehody@manitech-uh.cz
- **Hodiny:** Po–Pá 7:00–16:00, So+Ne zavřeno
- **Funguje od:** roku 2000
- **Specialice:** Škoda, VW, Seat, Audi
- **Tým:** Přemysl Plachý (pojistné události, 774 131 455), Přemysl Vavřina (vedoucí servisu, 778 443 700), Pavel Tomešek (přijímací technik, 777 166 773)
- **Pojišťovny:** Česká pojišťovna, CPP, Allianz, Generali, Slavia, ČSOB, Kooperativa, Triglav, AXA, Servisní pojišťovna

### Sekce webu
1. NAV — fixed transparent → dark scroll, hamburger
2. HERO — dark + blue radial glow, diagonal deco, badge "od roku 2000", hodiny karta vpravo
3. TRUST STRIP — 4 karty (Od roku 2000, 10+ pojišťoven, Spies Hecker, Bezplatná linka)
4. SLUZBY — 4 hlavní karty (Autoservis, Lakovna, Karosárna, Pojistné události)
5. DETAIL AUTOSERVISU — grid 8 konkrétních služeb
6. POJIŠŤOVNY — 10 partnerů v gridu
7. TÝM — 3 karty s iniciálami a kontakty
8. O NÁS — split layout, lokace + text
9. KONTAKT — form + info na tmavém pozadí
10. FOOTER — 3 sloupce + logo icon

---

## Příští kroky

- Předat klientovi, smazat watermark
- Nastavit Formspree pro kontaktní formulář
