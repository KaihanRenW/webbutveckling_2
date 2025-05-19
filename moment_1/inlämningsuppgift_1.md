**Inlämningsuppgift, Moment 1: Semantisk HTML-sida**

---

### Syfte  
Att visa att du förstår webbens grundläggande struktur, terminologi och hur du bygger en semantisk HTML-sida med korrekt dokumentstruktur och metataggar.

---

### Uppgiftsbeskrivning  
Skapa en enkel webb­sida `index.html` enligt nedan specifikation. Sidan ska visa en fiktiv presentation av dig själv eller ett ämne du gillar (t.ex. en hobby, ett favoritspel eller en fiktiv kurs).

---

### Kravspecifikation

1. **Dokumentstruktur & metadata**  
   - Använd **HTML5**-mall med `<!DOCTYPE html>`, `<html lang="sv">`, `<head>` och `<body>`.  
   - Sätt `<meta charset="utf-8">` och `<meta name="viewport" content="width=device-width, initial-scale=1.0">`.  
   - Ge sidan en beskrivande `<title>`.

2. **Semantiska element**  
   Sida skall innehålla minst dessa taggar, i korrekt hierarki:
   - `<header>` med en huvudrubrik (`<h1>`)  
   - `<nav>` med en enkel meny (minst två länkar, t.ex. “Hem” och “Om mig”)  
   - `<main>` som omsluter huvudinnehållet  
     - Inuti `<main>`:  
       - En `<section>` med underrubrik (`<h2>`) och ett stycke text.  
       - Ett `<article>` med underrubrik (`<h3>`) och minst ett stycke text.  
       - Ett `<aside>` med kompletterande information eller “tips”.  
   - `<footer>` med upphovsrätt eller kontaktinfo.

3. **Länkar och listor**  
   - Minst en lista (`<ul>` eller `<ol>`) inom något av sektionselementen.  
   - Minst en intern länk (anchor) till en sektion på samma sida.

4. **Validering**  
   - Koden ska validera utan fel i [W3C HTML-validatorn](https://validator.w3.org/).

5. **Extra (bonus)**  
   – Lägg in en extern Google Font i `<head>` och använd den på minst en rubrik.  
   – Inkludera en `<meta name="description">` med en kort text om sidan för SEO.

---

### Inlämning  
- **Filer:**  
  - `index.html`  
  - (valfritt) `styles.css` om du använder extern CSS  
- Push:a till din remote repo och dela länken för repo i CR.
