# Pre-Entrega 2 - Soda Stereo

## Descripción del Proyecto

Sitio web oficial de Soda Stereo desarrollado como segunda pre-entrega del curso. El sitio incluye información sobre la banda, discografía, integrantes y un formulario de contacto.

## Estructura del Proyecto

```
Entrega2_Garcia/
├── index.html              # Página principal (en raíz)
├── css/
│   └── styles.css          # Archivo de estilos principal
├── pages/
│   ├── banda.html          # Página de integrantes
│   ├── discografia.html    # Página de discografía
│   └── contacto.html       # Página de contacto
└── img/                    # Carpeta de imágenes
    ├── logo_soda.png
    ├── soda_destacada.jpg
    ├── noticia_1.png
    ├── noticia_2.jpg
    ├── noticia_3.png
    ├── cerati_perfil.jpg
    ├── zeta_perfil.jpeg
    ├── charly_perfil.jpg
    └── [tapas de álbumes]
```

## Implementación de Consignas

### ✅ HTML - Estructura Semántica

**Requisito:** Mínimo 3 HTML con estructura semántica completa (header, main, footer).

**Implementación:**
- ✅ **4 páginas HTML creadas:**
  - `index.html` - Página principal
  - `pages/banda.html` - Información de integrantes
  - `pages/discografia.html` - Discografía completa
  - `pages/contacto.html` - Formulario de contacto

- ✅ **Estructura semántica en todas las páginas:**
  - `<header>` - Contiene logo y navegación (líneas 18-36 en index.html)
  - `<main>` - Contiene el contenido principal (líneas 39-76 en index.html)
  - `<footer>` - Contiene copyright y redes sociales (líneas 79-86 en index.html)

- ✅ **H1 en cada HTML:**
  - `index.html`: `<h1>Soda Stereo</h1>` (línea 41)
  - `pages/banda.html`: `<h1>Integrantes</h1>` (línea 42)
  - `pages/discografia.html`: `<h1>Discografía Completa</h1>` (línea 42)
  - `pages/contacto.html`: `<h1>Contacto</h1>` (línea 42)

- ✅ **Menú de navegación completo:**
  - Implementado en todas las páginas con enlaces a: Inicio, Discografía, Banda, Contacto
  - Ubicado en `<nav>` dentro del `<header>` (líneas 22-35 en index.html)

- ✅ **Comentarios en HTML:**
  - Comentarios descriptivos en cada sección
  - Ejemplo: `<!-- Header con navegación -->`, `<!-- Sección H2: Últimas Noticias -->`

- ✅ **Atributos alt completos:**
  - Todas las imágenes tienen atributo `alt` descriptivo
  - Ejemplo: `alt="Soda Stereo Ecos - Nueva función en Movistar Arena"`

### ✅ CSS - Estilos y Box Model

**Requisito:** Aplicar estilos básicos a todos los HTML. BOX MODEL (propiedades en cada HTML). FLEX/GRID/MQ (usado como mínimo en 1 HTML). 1 HTML estructurado para mobile y desktop.

**Implementación:**
- ✅ **Archivo CSS:** `css/styles.css`

- ✅ **Box Model aplicado en todos los elementos:**
  - **Width:** Definido en todos los elementos principales
    - Ejemplo: `header { width: 100%; }` (línea 24)
    - Ejemplo: `.noticia-card { width: calc(33.333% - 20px); }` (línea 188)
  
  - **Padding:** Aplicado consistentemente
    - Ejemplo: `header { padding: 20px; }` (línea 25)
    - Ejemplo: `.noticia-card { padding: 20px; }` (línea 189)
  
  - **Margin:** Definido para espaciado
    - Ejemplo: `main { margin: 30px auto; }` (línea 107)
    - Ejemplo: `h1 { margin: 0 0 30px 0; }` (línea 116)
  
  - **Border:** Aplicado en elementos visuales
    - Ejemplo: `header { border-bottom: 2px solid #1a252f; }` (línea 29)
    - Ejemplo: `.disco-card { border: 2px solid #bdc3c7; }` (línea 256)

- ✅ **Flexbox implementado:**
  - **Ubicación:** `index.html` - Sección de noticias
  - **Archivo CSS:** Líneas 176-185
  - **Código:**
    ```css
    .noticias-container {
        display: flex;
        flex-direction: row;
        flex-wrap: wrap;
        justify-content: space-between;
        align-items: flex-start;
    }
    ```

- ✅ **Grid implementado:**
  - **Ubicación:** `pages/discografia.html` - Grid de álbumes
  - **Archivo CSS:** Líneas 241-249
  - **Código:**
    ```css
    .discos-container {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
        gap: 20px;
    }
    ```

- ✅ **Media Queries implementadas:**
  - **Ubicación:** `css/styles.css` - Líneas 502-568
  - **Breakpoints:**
    - Mobile: `@media screen and (max-width: 768px)` (línea 504)
    - Tablet: `@media screen and (min-width: 769px) and (max-width: 1023px)` (línea 556)
  
  - **Responsive en index.html:**
    - `.noticias-container` cambia a `flex-direction: column` en móvil (línea 516)
    - `.noticia-card` se ajusta a `width: 90%` en móvil (línea 520)

### ✅ Bootstrap - Menú Hamburguesa

**Requisito:** Opción b - En cada HTML un componente de Bootstrap (menú hamburguesa en cada HTML).

**Implementación:**
- ✅ **Componente Bootstrap en todas las páginas:**
  - **Ubicación:** Dentro de `<nav>` en cada HTML
  - **Archivo:** Todas las páginas (index.html línea 24-26, pages/banda.html línea 24-26, etc.)
  
  - **Código implementado:**
    ```html
    <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav">
        <span class="navbar-toggler-icon"></span>
    </button>
    <div class="collapse navbar-collapse" id="navbarNav">
        <!-- Menú de navegación -->
    </div>
    ```

- ✅ **Bootstrap CSS y JS:**
  - CSS: CDN Bootstrap 5.3.2 (línea 11 en index.html)
  - JS: CDN Bootstrap Bundle (línea 89 en index.html)

### ✅ Organización de Archivos

**Requisito:** CSS en `css/styles.css`. Páginas secundarias en carpeta `pages/`.

**Implementación:**
- ✅ **CSS:** `css/styles.css` - Archivo único con todos los estilos
- ✅ **Páginas en carpeta pages/:**
  - `pages/banda.html`
  - `pages/discografia.html`
  - `pages/contacto.html`
- ✅ **Index.html:** Ubicado en la raíz del proyecto
- ✅ **Rutas correctas:**
  - Desde `index.html`: `css/styles.css`, `img/...`, `pages/...`
  - Desde `pages/*.html`: `../css/styles.css`, `../img/...`, `../index.html`

## Páginas del Sitio

### 1. index.html
- **Ubicación:** Raíz del proyecto
- **Características:**
  - Usa **Flexbox** para el grid de noticias
  - Tiene **Media Queries** para responsive (mobile y desktop)
  - Imagen hero destacada
  - Sección de últimas noticias con 3 cards

### 2. pages/banda.html
- **Ubicación:** `pages/banda.html`
- **Características:**
  - Información de los 3 integrantes
  - Sección de dato histórico/cita destacada
  - Box Model aplicado en todos los elementos

### 3. pages/discografia.html
- **Ubicación:** `pages/discografia.html`
- **Características:**
  - Usa **Grid** para el layout de álbumes (3 columnas)
  - 6 álbumes con portadas e información
  - Box Model aplicado en todos los elementos

### 4. pages/contacto.html
- **Ubicación:** `pages/contacto.html`
- **Características:**
  - Formulario de contacto completo
  - Box Model aplicado en todos los elementos

## Dónde se Aplica Cada Tecnología

### Box Model
- **Aplicado en:** Todos los HTML
- **Archivo CSS:** Todo el archivo `css/styles.css`
- **Ejemplos específicos:**
  - Header: líneas 23-29
  - Main: líneas 104-110
  - Footer: líneas 465-473
  - Cards: líneas 187-194 (noticias), 251-258 (discos), 305-311 (integrantes)

### Flexbox
- **Aplicado en:** `index.html` - Sección de noticias
- **Archivo CSS:** Líneas 176-185
- **Clase:** `.noticias-container`

### Grid
- **Aplicado en:** `pages/discografia.html` - Grid de álbumes
- **Archivo CSS:** Líneas 241-249
- **Clase:** `.discos-container`

### Media Queries
- **Aplicado en:** `index.html` principalmente (responsive design)
- **Archivo CSS:** Líneas 502-568
- **Breakpoints:**
  - Mobile (≤768px): líneas 504-553
  - Tablet (769px-1023px): líneas 556-568

### Bootstrap
- **Aplicado en:** Todas las páginas HTML
- **Componente:** Menú hamburguesa (navbar-toggler)
- **Ubicación HTML:** Líneas 24-26 en cada página

## Estructura Semántica

Todas las páginas incluyen:
- `<header>` - Logo y navegación
- `<main>` - Contenido principal
- `<footer>` - Copyright y redes sociales
- `<section>` - Secciones temáticas
- `<article>` - Contenido independiente (noticias, discos, integrantes)
- `<nav>` - Navegación

## Enlaces y Rutas

### Desde index.html:
- CSS: `css/styles.css`
- Imágenes: `img/logo_soda.png`, `img/soda_destacada.jpg`, etc.
- Páginas: `pages/discografia.html`, `pages/banda.html`, `pages/contacto.html`

### Desde pages/*.html:
- CSS: `../css/styles.css`
- Imágenes: `../img/logo_soda.png`, `../img/cerati_perfil.jpg`, etc.
- Index: `../index.html`
- Otras páginas: `discografia.html`, `banda.html`, `contacto.html` (relativas dentro de pages/)

## Autor

García Mauro - Enero 2025

## Notas

- El sitio mantiene la estructura y diseño del proyecto original
- Todas las consignas han sido implementadas correctamente
- El código está comentado y organizado
- Responsive design implementado para mobile y desktop

