
# 📝 Inlämningsuppgift – Bootstrap Grunder (Vecka 4)

## 🎯 Syfte
I denna uppgift ska du få testa på att använda **Bootstrap via CDN** för att skapa en enkel och responsiv webbsida med färdiga komponenter. Du behöver inte installera någonting – bara kopiera och klistra in rätt kod i din HTML!

---

## ✅ Vad du ska göra

### 1. Skapa en HTML-fil

- Öppna din kodeditor (t.ex. VS Code eller Notepad++).
- Skapa en ny fil och spara den som **`uppgift4.html`**.

---

### 2. Lägg till Bootstrap via CDN

Kopiera och klistra in följande kod i din HTML-fil:

```html
<!DOCTYPE html>
<html lang="sv">
<head>
  <meta charset="UTF-8">
  <title>Min Bootstrap-sida</title>

  <!-- ✅ Bootstrap CSS (länka i <head>) -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/css/bootstrap.min.css" rel="stylesheet">
</head>
<body>

  <!-- ✅ Din sida kommer hit -->

  <!-- ✅ Bootstrap JavaScript (lägg före </body>) -->
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.0/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

---

### 3. Bygg upp innehållet i `<body>` enligt följande:

#### 🔹 1. Rubrik

Lägg till en `<h1>`-rubrik i mitten av sidan:

```html
<h1 class="text-center">Välkommen till min Bootstrap-sida</h1>
```

---

#### 🔹 2. Alertbox

Lägg till en varningsruta (alert):

```html
<div class="alert alert-warning text-center" role="alert">
  Detta är en Bootstrap-varning!
</div>
```

---

#### 🔹 3. Knapp i mitten

Lägg till en blå knapp (`btn btn-primary`) som ligger i mitten:

```html
<div class="text-center">
  <button class="btn btn-primary">Tryck här</button>
</div>
```

---

#### 🔹 4. Layout med två kolumner

Lägg till en rad med två kolumner bredvid varandra:

```html
<div class="container mt-4">
  <div class="row">
    <div class="col-6 bg-light p-3 border">Vänster kolumn</div>
    <div class="col-6 bg-light p-3 border">Höger kolumn</div>
  </div>
</div>
```

---

### 4. (Extra – Frivilligt)

Om du vill testa mer:

- Lägg till en ikon från [Bootstrap Icons](https://icons.getbootstrap.com/)
- Lägg till ett formulärfält med etikett

---

## 🧪 Testa

- Öppna filen i webbläsaren (dubbelklicka på filen).
- Kolla så allt syns och ser snyggt ut.
- Testa att ändra storlek på fönstret – innehållet ska anpassa sig (responsivt!).

---

## 📤 Inlämning

- Spara filen som `uppgift4.html`
- Lämna in den enligt instruktioner från din lärare

---

🟢 **Kom ihåg**: Bootstrap fungerar genom klasser (t.ex. `btn`, `container`, `text-center`) som du lägger till i dina HTML-taggar. Du behöver inte skriva någon CSS själv!

Lycka till! 💪
