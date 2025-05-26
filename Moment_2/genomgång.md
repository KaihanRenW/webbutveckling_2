**Vecka 2 – Styling och medier: Studiehandledning**

I vecka 2 fokuserar vi på CSS, responsiv design, effektiva metoder för att skriva stilar, ramverk och integration av multimedia. Efter genomgången ska du:

1. Förstå grundläggande CSS-koncept: selektorer, box-modell, layoutmetoder.  
2. Kunna skapa responsiva layouter med media queries.  
3. Använda CSS-variabler och preprocessorer/post-processors.  
4. Integrera bilder, ljud, video och interaktiv grafik.

---

## 1. CSS-grunder

### 1.1 Selektorer och syntax  
```css
/* Elementselektor */
h2 {
  margin-bottom: 0.5em;
}

/* Klassselektor */
.card {
  padding: 1rem;
}

/* ID-selektor */
#menu {
  list-style: none;
}

/* Kombinationsselektor */
nav ul > li a:hover {
  text-decoration: underline;
}
```

### 1.2 Box-modellen  
- **content** – elementets innehåll  
- **padding** – inre marginal  
- **border** – kantlinje  
- **margin** – yttre marginal  
```css
.box {
  width: 200px;
  padding: 10px;
  border: 2px solid #333;
  margin: 20px;
}
```

---

## 2. Layout: Flexbox & Grid

### 2.1 Flexbox  
```css
.container {
  display: flex;
  justify-content: space-between; /* horisontal fördelning */
  align-items: center;           /* vertikal centrering */
}
```

### 2.2 CSS Grid  
```css
.grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 1rem;
}
```

---

## 3. Responsiv design

### 3.1 Media queries  
```css
/* Basstilar */
body {
  font-size: 16px;
}

/* För skärmar < 600px */
@media (max-width: 600px) {
  body {
    font-size: 14px;
  }
}
```

### 3.2 Fluid layout  
- Använd procentenheter (`%`) och `max-width` istället för fasta pixlar.

---

## 4. Effektivt CSS-skrivande

### 4.1 CSS-variabler (Custom Properties)  
```css
:root {
  --primary-color: #3498db;
  --spacing: 1rem;
}

.button {
  background-color: var(--primary-color);
  padding: var(--spacing);
}
```

### 4.2 Pre-processorer/Post-processors  
- **SASS/SCSS**: nästling, variabler, mixins  
- **PostCSS**: autoprefixer, cssnano  

---

## 5. Ramverk & klassbibliotek

- **Bootstrap 5**: grid, komponenter, verktygsklasser  
- **Tailwind CSS**: utility-first, konfigurering via `tailwind.config.js`  

**Exempel Bootstrap**:
```html
<div class="container">
  <div class="row">
    <div class="col-md-6">Kolumn 1</div>
    <div class="col-md-6">Kolumn 2</div>
  </div>
</div>
```

---

## 6. Multimedia på webben

### 6.1 Bilder  
- Formaten JPEG, PNG, WebP – optimera storlek/quality  
```html
<img src="bild.webp" alt="Beskrivande alt-text" width="400">
```

### 6.2 Ljud & video  
```html
<audio controls>
  <source src="ljud.mp3" type="audio/mpeg">
</audio>
<video controls width="480">
  <source src="video.mp4" type="video/mp4">
</video>
```

### 6.3 Interaktiv grafik  
- `<canvas>` för 2D-ritning  
```html
<canvas id="myCanvas" width="300" height="150"></canvas>
<script>
  const c = document.getElementById('myCanvas');
  const ctx = c.getContext('2d');
  ctx.fillStyle = 'teal';
  ctx.fillRect(10, 10, 100, 50);
</script>
```

---

## 7. Praktisk övning

1. **Uppgift**: Skapa en HTML-sida med:
   - En flexibel header- och navigationslayout med flexbox.  
   - Ett bildgalleri med CSS Grid.  
   - Responsiv typografi via media queries.  
   - Användning av CSS-variabler för färg och mellanrum.  
   - Infoga minst en optimerad bild, ett ljudklipp eller en video.  

2. **Verifiering**:
   - Testa i olika fönsterstorlekar.  
   - Kontrollera att inga horisontella scrollbars uppstår på mindre skärmar.
