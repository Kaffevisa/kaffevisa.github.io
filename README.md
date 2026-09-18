# Kaffevisa

En egendesignet, statisk nettside/blogg om kaffe – ren HTML/CSS/JS, ingen
byggeverktøy nødvendig. Fargepaletten er "Cream Coffee".

## Filstruktur

```
kaffevisa-site/
├── index.html              Forsiden med de siste innleggene
├── om.html                 Om-siden
├── posts/                  Enkelt blogginnlegg (én .html-fil per innlegg)
├── css/style.css           Alt av styling og fargepalett
├── js/script.js            Mobilmeny + aktiv nav-lenke
└── assets/favicon.svg      Favicon (kaffekopp)
```

## Slik publiserer du på GitHub Pages

1. **Opprett repoet på GitHub**
   Gå til github.com → New repository → navngi det **nøyaktig**
   `kaffevisa.github.io` (siden du er logget inn som brukeren `kaffevisa`).
   Dette navnet er viktig – det er det som gjør at siden blir din
   hovedside på `https://kaffevisa.github.io`.

2. **Last opp filene**
   Enklest med Git i terminalen, fra denne mappen:

   ```bash
   cd kaffevisa-site
   git init
   git add .
   git commit -m "Første versjon av Kaffevisa"
   git branch -M main
   git remote add origin https://github.com/kaffevisa/kaffevisa.github.io.git
   git push -u origin main
   ```

   (Alternativt: dra og slipp filene inn via GitHub sitt web-grensesnitt
   under "Add file → Upload files", men da må mappestrukturen bevares.)

3. **Skru på GitHub Pages**
   For et repo med navnet `kaffevisa.github.io` blir Pages faktisk skrudd
   på automatisk. Dobbeltsjekk under repoets **Settings → Pages** at:
   - "Source" er satt til **Deploy from a branch**
   - Branch er **main**, mappe **/(root)**

4. **Vent litt, og besøk siden**
   Etter 1–2 minutter er siden live på:
   `https://kaffevisa.github.io`

## Legge til et nytt blogginnlegg

1. Kopiér en av filene i `posts/`, f.eks. `posts/fra-bonne-til-kopp.html`.
2. Endre `<title>`, dato og selve teksten i den nye filen.
3. Legg til et nytt `<article class="post-card">` i `index.html` (kopiér et
   av de eksisterende kortene) som lenker til din nye fil.
4. `git add . && git commit -m "Nytt innlegg" && git push`

## Endre farger eller stil

Alt styres fra toppen av `css/style.css`:

```css
:root {
  --cream:      #ece0d1;
  --tan:        #dbc1ac;
  --caramel:    #967259;
  --coffee:     #634832;
  --espresso:   #38220f;
}
```

Endre disse fem verdiene for å justere hele paletten på ett sted.
