# ☄️ Lopunaikojen Megabileet

Kaveriporukan tapahtumasovellus: vuosi- ja kausiaikajana, järjestämisvuorojono,
alustavat kyselyt (usean ajankohdan äänestys vähimmäisosallistujamäärällä),
osallistumiskuittaukset, kausiesteet, muistot ja arvosanat sekä WhatsApp-jako.

Sovellus on yksi staattinen tiedosto (`index.html`), jossa ei ole riippuvuuksia
eikä build-vaihetta.

## Julkaisu GitHub Pagesissa

1. Luo uusi GitHub-repositorio ja vie tämän kansion sisältö sen `main`-haaraan.
2. Avaa **Settings → Pages**.
3. Valitse **Source: GitHub Actions**. Mukana oleva työnkulku
   (`.github/workflows/pages.yml`) julkaisee sivun automaattisesti jokaisella pushilla.

   Vaihtoehtoisesti voit valita **Source: Deploy from a branch**, haaraksi
   `main` ja kansioksi `/ (root)`. Silloin työnkulkua ei tarvita.
4. Sivu avautuu osoitteeseen `https://<käyttäjä>.github.io/<repo>/`.

## Paikallinen käyttö

Avaa `index.html` selaimessa tai aja esim. `python3 -m http.server`.

## Tietojen tallennus

Tiedot tallentuvat selaimen `localStorage`-muistiin (avain
`lopunaikojen-megabileet-state-v1`). Jokaisella käyttäjällä ja selaimella on siis
oma kopionsa, eikä tieto synkronoidu laitteiden välillä. Jaettu tila vaatisi
taustapalvelun, esimerkiksi Firebasen tai Supabasen.
