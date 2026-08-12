<div align="right">

**Srpski** · [English](README.en.md)

</div>

# Luka Cvoro — Portfolio

Lični sajt i CV. Oracle APEX & PL/SQL developer iz Beograda.

**Uživo:** [lukacvoro.netlify.app](https://portfoliolukacvoro.netlify.app/) · **LinkedIn:** [luka-cvoro](https://www.linkedin.com/in/luka-cvoro-3b2194197/) · **Mejl:** [lukac95@gmail.com](mailto:lukac95@gmail.com)

---

## Šta je ovo

Jednostranični portfolio bez ijednog framework-a — čist HTML, CSS i JavaScript u jednom fajlu. Nema build koraka, nema `node_modules`, nema zavisnosti. Otvoriš `index.html` i radi.

Ideja je bila da sajt ne samo *opisuje* šta radim, nego to i **pokaže**: pošto radim sa bazama, filtriranje tehnologija ispisuje pravi SQL upit, a slanje forme prikazuje `INSERT` koji bi je upisao.

## Šta ume

| | |
|---|---|
| **Dvojezičnost** | Ceo sajt na srpskom i engleskom — jedan klik, bez ponovnog učitavanja. Prevode se i tekstovi, i datumi, i primeri koda, i poruke o greškama. |
| **Živa SQL konzola** | Filteri iznad liste tehnologija ispisuju stvarni `SELECT ... WHERE ... ORDER BY` sa brojem redova, koji se menja dok biraš. |
| **GitHub projekti** | Repozitorijumi se povlače uživo sa GitHub API-ja. Novi projekat se pojavi sam, bez izmene koda i bez novog deploya. |
| **Vremenska linija** | Iskustvo i obrazovanje sa tačkicama po pozicijama, aktivne uloge označene. |
| **Formulari** | Kontakt i zahtev za ponudu, sa validacijom po polju i slanjem preko Netlify Forms — bez backenda. |
| **Kalendar** | Sopstveni date picker, jer nativni `input[type=date]` ne poštuje jezik sajta. Format `dd.mm.gggg.` ili `dd/mm/yyyy`. |

## Tehnologije

`HTML5` · `CSS3` (Grid, Flexbox, custom properties) · `JavaScript` (ES6+, bez biblioteka) · `GitHub REST API` · `Netlify Forms`

Bez jQuery-ja, bez React-a, bez Tailwind-a. Namerno — za sajt ove veličine sve to bi bilo više tereta nego koristi.

## Struktura

```
.
├── index.html      # ceo sajt: struktura, stilovi, logika, prevodi
├── luka.jpg        # fotografija (400×400)
├── og.png          # slika za pregled linka (1200×630)
├── README.md       # ova datoteka
└── README.en.md    # engleska verzija
```

## Pokretanje

```bash
git clone https://github.com/Cvoki/portfolio.git
cd portfolio
```

Otvori `index.html` u pregledaču — to je sve.

Za lokalni server (potreban ako testiraš slanje forme):

```bash
python3 -m http.server 8000
# pa otvori http://localhost:8000
```

> **Napomena:** slanje formulara radi samo na objavljenom sajtu, jer se oslanja na Netlify Forms.

## Objavljivanje

Sajt je na Netlify-u, povezan sa ovim repozitorijumom — svaki `push` na `main` pokreće novi deploy.

Za forme je potrebno u Netlify panelu jednom uključiti **Forms → Enable form detection** i zatim ponovo deployovati. Obaveštenja se podešavaju pod *Notifications → Form submission notifications*.

## Izmene sadržaja

Sve što se menja nalazi se u `<script>` bloku na dnu `index.html`, u nekoliko nizova:

| Šta menjaš | Gde |
|---|---|
| Prevodi svih tekstova | `const T = { sr: {...}, en: {...} }` |
| Radno iskustvo | `const XP = [...]` |
| Obrazovanje | `const EDU = [...]` |
| Jezici | `const JEZICI = [...]` |
| Tehnologije i nivoi | `const TEH = [...]` |
| Primeri koda | `const PRIMERI = {...}` |

Svako polje sa tekstom ima oblik `{sr: "...", en: "..."}` — dodaš oba i prevod radi sam.

## Licenca

Kod je slobodan za korišćenje i učenje. Sadržaj (biografija, fotografija, tekstovi) nije — to je moje.

---

<sub>Ako te zanima saradnja ili imaš pitanje — <a href="mailto:lukac95@gmail.com">javi se</a>.</sub>
