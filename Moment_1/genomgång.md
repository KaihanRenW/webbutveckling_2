**Vecka 1 – Genomgång och studiehandledning**

Denna studiehandledning täcker veckans centrala innehåll: webbens roll, grundläggande terminologi och HTML:s struktur och semantiska element. Målet är att du efter genomgången:

1. Förstår hur webben fungerar (klient-server, HTTP/HTTPS, statisk vs dynamisk).
2. Känner till grundläggande begrepp inom webbutveckling.
3. Kan skapa en semantisk HTML-sida med korrekt dokumentstruktur.

---

## 1. Webbens betydelse och funktion

### 1.1 Klient–server-modellen  
- **Klient** = webbläsare (Chrome, Firefox, Safari etc.) som skickar begäran (request).  
- **Server** = dator/miljö (t.ex. Apache, Nginx eller Node.js) som hanterar begäran och skickar svar (response).  
- Interaktion sker alltid över HTTP eller HTTPS (krypterad).  

```text
[Klient] ---(HTTP GET /index.html)---> [Server]
[Server] ---(HTTP 200 OK + HTML)---> [Klient]
```

### 1.2 HTTP-protokollet  
- **Metoder**:  
  - `GET` – hämta resurser  
  - `POST` – skicka formulärdata  
  - `PUT`, `DELETE`, `PATCH` – CRUD-operationer i API:er  
- **Statuskoder**:  
  - `2xx` – framgång (200 OK, 201 Created)  
  - `3xx` – omdirigering (301 Moved Permanently)  
  - `4xx` – klientfel (404 Not Found, 400 Bad Request)  
  - `5xx` – serverfel (500 Internal Server Error)  

### 1.3 Statisk vs dynamisk  
- **Statisk webbplats**: filer (.html, .css, .js) levereras oförändrade.  
- **Dynamisk webbapplikation**: genererar innehåll vid varje förfrågan (t.ex. PHP, Node.js, Python).  

---

## 2. Terminologi inom webbutveckling

| Begrepp         | Förklaring                                                  |
|-----------------|-------------------------------------------------------------|
| **URL**         | Uniform Resource Locator – adress till en resurs på webben. |
| **DOM**         | Document Object Model – HTML-dokumentet som ett objektträd. |
| **API**         | Application Programming Interface – sätt att kommunicera program. |
| **CMS**         | Content Management System – t.ex. WordPress, Drupal.        |
| **SSL/TLS**     | Krypterar HTTP till HTTPS.                                  |
| **Frontend**    | Klientsidan (HTML/CSS/JS).                                  |
| **Backend**     | Serversidan (databas, autentisering, logik).                |
| **Fullstack**   | Både frontend och backend.                                  |

---

## 3. Struktur på webbsidor med HTML

### 3.1 Grundläggande dokumentstruktur  
Varje HTML-dokument bör ha denna minsta mall:

```html
<!DOCTYPE html>
<html lang="sv">
  <head>
    <meta charset="utf-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Min första webbsida</title>
    <link rel="stylesheet" href="styles.css">
  </head>
  <body>
    <!-- Innehåll här -->
  </body>
</html>
```

- `<!DOCTYPE html>` talar om att dokumentet är HTML5.  
- `<html lang="sv">` anger språk (viktig för tillgänglighet).  
- `<meta charset>` ställer in teckenkodning.  
- `<meta viewport>` gör sidan responsiv på mobiler.

### 3.2 Semantiska element  
Semantiska taggar förbättrar läsbarhet, SEO och tillgänglighet.

| Tagg       | Användning                                     |
|------------|------------------------------------------------|
| `<header>` | Sidhuvud, innehåller ofta logotyp och meny     |
| `<nav>`    | Navigationsmeny                                |
| `<main>`   | Huvudinnehåll (får endast finnas en per sida)  |
| `<section>`| Tematiskt avsnitt (ex. bloggavsnitt)           |
| `<article>`| Självständigt innehåll (ex. blogginlägg)       |
| `<aside>`  | Sidoinformation (kommentarer, länkar)          |
| `<footer>` | Sidfot med upphovsrätt, kontaktinfo etc.       |

**Exempel:**  
```html
<body>
  <header>
    <h1>Välkommen till Webbkursen</h1>
  </header>
  <nav>
    <ul>
      <li><a href="#home">Hem</a></li>
      <li><a href="#om">Om kursen</a></li>
    </ul>
  </nav>
  <main>
    <section id="om">
      <h2>Om kursen</h2>
      <p>Här lär du dig grunderna i HTML.</p>
    </section>
    <article>
      <h3>Vecka 1: HTML</h3>
      <p>...</p>
    </article>
    <aside>
      <h4>Tips</h4>
      <p>Använd W3C Validator!</p>
    </aside>
  </main>
  <footer>
    <p>&copy; 2025 Webbutveckling AB</p>
  </footer>
</body>
```

---

## 4. Praktisk övning

### Uppgift: Skapa en enkel semantisk HTML-sida

1. **Setup**: Skapa två filer i en mapp: `index.html` och `styles.css`.  
2. **Dokumentmall**: Klistra in mallen från avsnitt 3.1 i `index.html`.  
3. **Semantiska sektioner**:  
   - Lägg till `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<aside>`, `<footer>`.  
   - Ge varje avsnitt en rubrik (`<h1>`–`<h4>`).  
4. **Metadata**:  
   - Ange språk med `lang="sv"`.  
   - Ställ in `<meta charset>` och `<meta viewport>` korrekt.  
5. **Kontrollera**:  
   - Öppna i webbläsare och se att strukturen är som förväntat.  
   - Validera med [W3C HTML-validator](https://validator.w3.org/).  

**Reflektion:** Vad händer om du tar bort `<!DOCTYPE html>`?  
**Bonus:** Lägg till en extern Google Font i `<head>` och applicera den via CSS.  
