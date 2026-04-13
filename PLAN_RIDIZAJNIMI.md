# Planifikim per Update te Webfaqes se Futbollit

## 1) Qellimi i projektit
Ky update ka fokus ne:
- Ridizajnim vizual te webfaqes.
- Harmonizim te identitetit me logon dhe ngjyrat e saj.
- Integrim te faqes se Facebook-ut ne website.
- Publikim demo ne Netlify.

## 2) Objektivat kryesore
- Te ruhet permbajtja ekzistuese e webfaqes (te dhenat aktuale).
- Te permiresohet pamja dhe eksperienca ne desktop dhe mobile.
- Te rritet besueshmeria vizuale permes nje sistemi te qarte ngjyrash dhe tipografie.
- Te shtohet seksion aktiv social me embed te Facebook-ut.
- Te vendoset nje version demo online per testim dhe feedback.

## 3) Scope (cka perfshihet)
### Ne scope
- Analize e permbajtjes ekzistuese nga faqet:
  - `index.html`
  - `team.html`
  - `ndeshjet.html`
  - `galeria.html`
- Ridizajnim i UI bazuar ne identitetin vizual te klubit.
- Refaktorim i `assets/css/main.css` (ngjyra, spacing, tipografi, komponente).
- Integrim i widget-it te Facebook (Page Plugin) ne nje seksion te pershtatshem.
- Deploy demo ne Netlify.


## 4) Kerkesat funksionale
1. Webfaqja te ruaje informacionin aktual (tekste, foto, ndeshje, ekip).
2. Te kete stil te rifreskuar sipas logos dhe ngjyrave te saj.
3. Te kete embed te faqes se Facebook-ut:
   - URL: `https://www.facebook.com/profile.php?id=61579096839380`
4. Dizajni te jete responsive (mobile, tablet, desktop).
5. Te publikohet demo URL ne Netlify.

## 5) Kerkesat jo-funksionale
- Performanca: ngarkim i shpejte i faqeve (optimizim i imazheve dhe CSS/JS).
- Konsistence vizuale ne te gjitha faqet.
- Mirembajtje e lehte (strukture e paster e CSS dhe seksioneve HTML).
- Kompatibilitet me shfletues modern (Chrome, Edge, Firefox, Safari).

## 6) Strategjia e ridizajnimit (Logo + Ngjyra)
### Hapi 1: Auditim vizual
- Nxjerrje e paletes primare nga logo (1 ngjyre kryesore, 1 sekondare, 1 accent).
- Kontroll i kontrastit per aksesueshmeri.

### Hapi 2: Definim Design Tokens
Ne `:root` te `assets/css/main.css`:
- `--color-primary`
- `--color-secondary`
- `--color-accent`
- `--color-bg`
- `--color-surface`
- `--color-text`
- `--radius-*`, `--shadow-*`, `--spacing-*`

### Hapi 3: Aplikim ne komponente
- Header / Navbar
- Hero section
- Butona dhe link-e
- Karta (team, ndeshje, galeri)
- Footer

## 7) Integrimi i Facebook ne website
### Opsioni i rekomanduar: Facebook Page Plugin
Do vendoset ne:
- `index.html` (seksion "Lajmet e fundit" ose para footer-it),
ose
- faqe e dedikuar sociale.

Elementet kryesore:
- SDK e Facebook-ut ne fund ose fillim te `body`.
- `div.fb-page` me URL e profilit.

Shenim: Nese URL e profilit nuk gjeneron korrekt Page Plugin (varesisht llojit te faqes), do perdoret alternativisht:
- buton/link direkt me CTA te qarte,
- ose iframe/social feed alternative qe lejohet nga politika e Facebook-ut.

## 8) Plan pune me faza
## Faza 1 - Analize dhe planifikim (0.5 dite)
- Inventar i permbajtjes aktuale.
- Konfirmim i ngjyrave te logos.
- Vendim per pozicionin e Facebook embed.

Deliverable:
- Mini-brief dizajni + lista e ndryshimeve per secilen faqe.

## Faza 2 - Ridizajnim UI (1-2 dite)
- Refaktorim i stileve globale ne `main.css`.
- Perditesim i strukturave kryesore HTML ne faqet ekzistuese.
- Testim responsive.

Deliverable:
- Version i ri vizual ne local/staging.

## Faza 3 - Integrim Facebook + QA (0.5-1 dite)
- Integrim i widget-it Facebook.
- Testim i renderimit dhe performance.
- QA final (linke, layout, mobile).

Deliverable:
- Build final gati per deploy.

## Faza 4 - Deploy ne Netlify (0.5 dite)
- Krijim site ne Netlify.
- Lidhje me repo ose deploy manual i folderit.
- Vendosje e demo URL.

Deliverable:
- Link demo publik ne Netlify.

## 9) Checklist implementimi
- [ ] Te gjitha faqet ekzistuese jane ruajtur me permbajtje te njejte.
- [ ] Paleta e ngjyrave eshte unifikuar sipas logos.
- [ ] Header, butona, karta dhe footer kane stil te ri konsistent.
- [ ] Facebook embed funksionon ne desktop dhe mobile.
- [ ] Nuk ka gabime kritike ne layout.
- [ ] Demo eshte online ne Netlify.

## 10) Rreziqe dhe zgjidhje
- Rrezik: Facebook plugin mund te kete kufizime per disa URL profili.
  - Zgjidhje: fallback me link/CTA zyrtar ose alternative feed.
- Rrezik: Kontrast i dobet i ngjyrave pas ridizajnimit.
  - Zgjidhje: testim i kontrastit dhe korrigjim i token-eve.
- Rrezik: Prishje e layout-it ne mobile.
  - Zgjidhje: testime ne breakpoint-et kryesore dhe rregullime CSS.

## 11) Kriteret e pranimit
Projekti konsiderohet i perfunduar kur:
1. Dizajni i ri reflekton qarte identitetin e logos dhe ngjyrave.
2. Perdoruesi mund te shikoje seksionin e Facebook-ut ne website.
3. Te dhenat ekzistuese ne faqe jane ruajtur.
4. Demo URL ne Netlify eshte funksionale dhe e aksesueshme publikisht.

## 12) Hapat e rekomanduar per Netlify (praktik)
1. Krijo repository (nese nuk ekziston) dhe ngarko kodin.
2. Ne Netlify: "Add new site" -> "Import an existing project".
3. Zgjidh repo-n.
4. Build command: bosh (site statik) ose sipas nevojes.
5. Publish directory: rrënja e projektit (ku ndodhet `index.html`) ose folderi perkates.
6. Deploy site dhe verifiko faqet kryesore.
7. Nese duhet, vendos custom domain me vone.

---

## Output final i kesaj faze
- Dokument planifikimi i qarte per ekipin.
- Gati per kalim ne fazen e implementimit teknik.