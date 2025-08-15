# WITLOF 2025 — Lanceren via GitHub Pages (met eigen domein)

Dit pakket is klaar voor **GitHub Pages** met domein **witlof-2025.nl** en mailto ingesteld.
Jouw GitHub-gebruikersnaam: **stemkenslofbv244-netizen**

---

## Stap-voor-stap: live via GitHub Pages

### 1) Nieuwe repository maken
1. Ga naar https://github.com/ en log in.
2. Klik rechtsboven **+ → New repository**.
3. **Repository name:** `witlof2025`
4. **Public** aanzetten → **Create repository**.

### 2) ZIP uitpakken en uploaden
1. Pak deze ZIP lokaal uit.
2. In je nieuwe repo klik je **Add file → Upload files**.
3. Sleep **alle bestanden** uit de uitgepakte map (niet de ZIP zelf):
   ```
   index.html
   assets/
   social-preview.png
   CNAME
   README.md
   ```
4. Klik **Commit changes**.

### 3) GitHub Pages inschakelen
1. Ga naar **Settings → Pages** (linkermenu).
2. **Source:** *Deploy from a branch*
3. **Branch:** `main` • **Folder:** `/ (root)`
4. Klik **Save**. Binnen kort verschijnt er onderaan een bevestiging met de Pages-URL.

### 4) Eigen domein instellen in Pages
1. Op dezelfde **Pages**-pagina: **Custom domain** → vul in:
   ```
   witlof-2025.nl
   ```
2. **Save**.

> Het bestand **CNAME** staat al in de root met `witlof-2025.nl`, dus GitHub weet welk domein bij deze site hoort.

### 5) DNS instellen bij je domeinprovider
Maak onderstaande records bij je domeinprovider.

**A-records (apex / root domein)**  
Voor `witlof-2025.nl` (host: `@`) → voeg deze vier IP’s toe:
```
185.199.108.153
185.199.109.153
185.199.110.153
185.199.111.153
```

**CNAME (www-subdomein)**  
Zodat **www.witlof-2025.nl** ook werkt:
```
www  →  stemkenslofbv244-netizen.github.io.
```

> Punt achter `github.io.` mag, sommige providers eisen dit. Laat TTL op standaard staan.

### 6) HTTPS aanzetten
- Terug in **Settings → Pages**: vink **Enforce HTTPS** aan zodra het beschikbaar is.
- DNS kan 10 minuten tot 24 uur nodig hebben. Wacht tot GitHub het certificaat klaar heeft.

---

## Wat staat er in dit pakket?
- `index.html` — tweetalig (NL/EN), geel-groen, animaties, positieve intro (gezondheid & gemak), Netlify-ready form, mailknop naar **ed.stemkens@home.nl**.
- `assets/` — favicon en apple-touch-icon.
- `social-preview.png` — afbeelding voor link previews.
- `CNAME` — gevuld met `witlof-2025.nl`.
- `README.md` — dit document met jouw username.

## Testen
- Na deploy zonder domein: je site staat tijdelijk op `https://stemkenslofbv244-netizen.github.io/witlof2025/` (totdat je custom domain actief is).
- Met domein: `https://witlof-2025.nl/`

Veel succes! 🍋🥬
