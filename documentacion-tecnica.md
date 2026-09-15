# Documentación técnica — Navegar con Otros
**Versión**: septiembre 2026  
**Archivo de referencia para intervenir el código del sitio**

---

## 1. Estructura general del sitio

| Archivo | Tipo | Color | Estado |
|---------|------|-------|--------|
| `index.html` | Página de inicio | violeta | ✅ completo |
| `sobre-el-proyecto.html` | Página institucional | violeta | ✅ completo |
| `recursos.html` | Página de recursos | — | ⏳ pendiente |
| `tema-1-identidad.html` | Página de tema | verde | ✅ completo |
| `tema-2-privacidad.html` | Página de tema | violeta | ✅ completo |
| `tema-3-desinformacion.html` | Página de tema | coral | ✅ completo |
| `tema-4-convivencia.html` | Página de tema | verde | ✅ completo |
| `tema-5-bienestar.html` | Página de tema | violeta | ✅ completo |
| `tema-6-derechos.html` | Página de tema | coral | ✅ completo |
| `tema-7-creacion.html` | Página de tema | verde | ✅ completo |
| `material-tarjetas-tema-N.html` | Material | color del tema | T1,T3,T4,T5,T6,T7 ✅ · T2 ✅ |
| `material-verdadero-falso-tema-N.html` | Material | color del tema | T1,T3,T5,T6,T7 ✅ · T2,T4 ⏳ |
| `material-ficha-produccion-tema-N.html` | Material | color del tema | T1,T3,T5,T6,T7 ✅ · T2,T4 ⏳ |
| `material-conceptos-tema-N.html` | Material | color del tema | T1,T3,T5,T6,T7 ✅ · T2,T4 ⏳ |
| `estilos.css` | CSS unificado | — | ✅ completo |

**Total**: 30 archivos HTML + 1 CSS

---

## 2. Sistema de colores

El color de cada tema se define con dos variables CSS al comienzo de cada archivo HTML, dentro de un bloque `<style>` de 6 líneas:

```html
<style>
  :root {
    --color-tema: #00897B;        /* color principal */
    --color-tema-claro: #E0F2F1;  /* versión clara para fondos */
  }
</style>
```

| Tema | `--color-tema` | `--color-tema-claro` |
|------|---------------|---------------------|
| T1, T4, T7 (verde) | `#00897B` | `#E0F2F1` |
| T2, T5 (violeta) | `#5E35B1` | `#EDE7F6` |
| T3, T6 (coral) | `#EF5350` | `#FFEBEE` |

Para cambiar el color de un tema: editá esas dos líneas en el archivo de ese tema.  
Para cambiar el color en todos los temas a la vez: editá la variable `--verde`, `--violeta` o `--coral` en `estilos.css`, sección 1 (Variables).

---

## 3. Componentes por tipo de página

### 3.1 Página de tema (`tema-N-nombre.html`)

Orden de elementos de arriba hacia abajo:

| # | Elemento | Etiqueta HTML | Clase CSS |
|---|----------|--------------|-----------|
| 1 | Navegación principal | `<nav>` | `nav` |
| 2 | Barra de temas | `<div>` | `nav-temas` |
| 3 | Cabezal del tema | `<header>` | `tema-header` |
| 4 | Número decorativo | `<div>` | `tema-numero-grande` |
| 5 | Etiqueta "Tema 0N" | `<span>` | `tema-etiqueta` |
| 6 | Título h1 | `<h1>` | — |
| 7 | Bajada | `<p>` | — |
| 8 | Chip de dimensión | `<span>` | `tema-dimension` |
| 9 | Contenedor principal | `<main>` | `contenido` |
| 10 | Acordeón: Marco conceptual | `<div>` | `acordeon-item` |
| 11 | Acordeón: Actividad participativa | `<div>` | `acordeon-item` |
| 12 | Acordeón: Guía docente | `<div>` | `acordeon-item` |
| 13 | Acordeón: Momento crítico | `<div>` | `acordeon-item` |
| 14 | Acordeón: Entradas disciplinares | `<div>` | `acordeon-item` |
| 15 | Navegación entre temas | `<div>` | `nav-entre-temas` |
| 16 | Pie de página | `<footer>` | `footer` |

---

### 3.2 Página de material: Tarjetas (`material-tarjetas-tema-N.html`)

| # | Elemento | Etiqueta HTML | Clase CSS |
|---|----------|--------------|-----------|
| 1 | Navegación principal | `<nav>` | `nav` |
| 2 | Encabezado del material | `<div>` | `material-header` |
| 3 | Ruta de migas | `<div>` | `material-ruta` |
| 4 | Título h1 | `<h1>` | — |
| 5 | Descripción | `<p>` | — |
| 6 | Badges | `<div>` | `material-badges` |
| 7 | Botón imprimir | `<button>` | `btn-imprimir` |
| 8 | Botón instrucciones | `<button>` | `btn-instrucciones` |
| 9 | Panel instrucciones (oculto) | `<div>` | `instrucciones-panel` |
| 10 | Grilla de tarjetas | `<div>` | `tarjetas-grid` |
| 11 | Tarjeta individual (×8) | `<div>` | `tarjeta` |
| 12 | Modal de tarjeta (×8) | `<div>` | `modal-overlay` |
| 13 | Pie de página | `<footer>` | `footer` |

---

### 3.3 Página de material: Verdadero o Falso (`material-verdadero-falso-tema-N.html`)

| # | Elemento | Etiqueta HTML | Clase CSS |
|---|----------|--------------|-----------|
| 1 | Navegación principal | `<nav>` | `nav` |
| 2 | Encabezado del material | `<div>` | `material-header` |
| 3 | Panel instrucciones fijo | `<div>` | `instrucciones-panel` |
| 4 | Barra de progreso | `<div>` | `progreso-barra` |
| 5 | Texto de progreso | `<div>` | `progreso-texto` |
| 6 | Track de progreso | `<div>` | `progreso-track` |
| 7 | Relleno animado | `<div>` | `progreso-fill` |
| 8 | Contenedor del juego | `<div>` | `juego-contenedor` |
| 9 | Tarjeta de afirmación (×10) | `<div>` | `afirmacion-card` |
| 10 | Panel de respuesta (por tarjeta) | `<div>` | `respuesta-panel` |
| 11 | Resultado final | `<div>` | `resultado-final` |
| 12 | Pie de página | `<footer>` | `footer` |

---

### 3.4 Página de material: Ficha de producción (`material-ficha-produccion-tema-N.html`)

| # | Elemento | Etiqueta HTML | Clase CSS |
|---|----------|--------------|-----------|
| 1 | Navegación principal | `<nav>` | `nav` |
| 2 | Encabezado del material | `<div>` | `material-header` |
| 3 | Estado de guardado | `<div>` | `guardado-estado` |
| 4 | Botón descargar PDF | `<button>` | `btn-pdf` |
| 5 | Botón limpiar | `<button>` | `btn-limpiar` |
| 6 | Aviso CREA | `<div>` | `aviso-crea` |
| 7 | Contenedor de ficha | `<div>` | `ficha-contenedor` |
| 8 | Cabezal de ficha | `<div>` | `ficha-top` |
| 9 | Fila de datos (nombre/año/fecha) | `<div>` | `ficha-datos` |
| 10 | Sección de la ficha (×4–5) | `<div>` | `ficha-seccion` |
| 11 | Textarea de respuesta | `<textarea>` | `ficha-textarea` |
| 12 | Pie de página | `<footer>` | `footer` |

---

### 3.5 Página de material: Conceptos flip (`material-conceptos-tema-N.html`)

| # | Elemento | Etiqueta HTML | Clase CSS |
|---|----------|--------------|-----------|
| 1 | Navegación principal | `<nav>` | `nav` |
| 2 | Encabezado del material | `<div>` | `material-header` |
| 3 | Panel instrucciones fijo | `<div>` | `instrucciones-panel` |
| 4 | Controles (3 botones) | `<div>` | `controles-conceptos` |
| 5 | Grilla de tarjetas | `<div>` | `tarjetas-grid` |
| 6 | Tarjeta flip (×10) | `<div>` | `tarjeta-flip` |
| 7 | Interior animado | `<div>` | `tarjeta-flip-inner` |
| 8 | Cara frontal (término) | `<div>` | `tarjeta-frente` |
| 9 | Cara dorsal (definición) | `<div>` | `tarjeta-dorso` |
| 10 | Pie de página | `<footer>` | `footer` |

---

### 3.6 Página de inicio (`index.html`)

Es la única página sin barra de temas ni cabezal de tema. Tiene seis secciones apiladas verticalmente, cada una como un `<section>`:

| # | Elemento | Etiqueta HTML | Clase CSS | Contenido |
|---|----------|--------------|-----------|-----------|
| 1 | Navegación principal | `<nav>` | `nav` | Logo + 3 links |
| 2 | Hero | `<section>` | `hero` | Etiqueta · h1 · bajada · 2 botones |
| 3 | Dimensiones | `<section>` | `dimensiones` | Título · subtítulo · 3 tarjetas de dimensión |
| 4 | Temas | `<section>` | `temas` + `id="temas"` | Título · subtítulo · 7 tarjetas de tema |
| 5 | Para quién | `<section>` | `para-quien` | Título · subtítulo · 3 tarjetas de perfil |
| 6 | CTA final | `<section>` | `cta-final` | Título · bajada · botón |
| 7 | Pie de página | `<footer>` | `footer` | Créditos + link a Sobre el proyecto |

**Estructura del Hero:**

```html
<section class="hero">
  <span class="hero-etiqueta">Recurso web para docentes · Educación Media · Uruguay</span>
  <h1>Ciudadanía digital en el aula</h1>
  <p>Descripción breve...</p>
  <div class="hero-botones">
    <a href="#temas" class="btn-principal">Ver los temas</a>
    <a href="sobre-el-proyecto.html" class="btn-secundario">¿Qué es este recurso?</a>
  </div>
</section>
```

**Tarjetas de dimensión** (sección Dimensiones):

```html
<div class="dimensiones-grid">
  <div class="dimension-card comprension">
    <h3>Comprensión del entorno digital</h3>
    <p>Descripción...</p>
  </div>
  <div class="dimension-card convivencia">...</div>
  <div class="dimension-card creacion">...</div>
</div>
```

Las tres variantes de color usan las clases `comprension` (verde), `convivencia` (violeta) y `creacion` (coral), definidas en `estilos.css` sección 16.

**Tarjetas de tema** (sección Temas):

```html
<div class="temas-grid">
  <a href="tema-1-identidad.html" class="tema-card">
    <div class="tema-numero">01</div>
    <h3>Identidad y huella digital</h3>
    <p>Descripción breve...</p>
  </a>
  <!-- ×7 -->
</div>
```

Cada `tema-card` es un enlace `<a>` que lleva directamente a la página del tema. El número grande (`tema-numero`) se muestra en verde claro como elemento decorativo.

**Tarjetas de perfil** (sección Para quién):

```html
<div class="perfiles-grid">
  <div class="perfil-card">
    <div class="perfil-icono">👩‍🏫</div>
    <h3>Cualquier docente de Media</h3>
    <p>Descripción...</p>
  </div>
  <!-- ×3 -->
</div>
```

**CTA final:**

```html
<section class="cta-final">
  <h2>Llevá la ciudadanía digital al aula</h2>
  <p>Descripción...</p>
  <a href="#temas" class="btn-blanco">Explorar los temas</a>
</section>
```

El `btn-blanco` es exclusivo del CTA final: fondo blanco con texto violeta, para contraste sobre el fondo violeta de la sección.

**Nota sobre el ancla `#temas`**: el `<section class="temas">` tiene `id="temas"`. Los dos botones del hero y el botón del CTA final apuntan a `#temas`, lo que hace que el navegador baje directamente a esa sección al hacer clic.

---

## 4. Componentes compartidos en detalle

### 4.1 Navegación principal

Aparece en todas las páginas. Sticky (queda fija al hacer scroll).

```html
<nav>
  <a href="index.html" class="nav-logo">Navegar <span>con Otros</span></a>
  <ul class="nav-links">
    <li><a href="index.html#temas">Temas</a></li>
    <li><a href="recursos.html">Recursos</a></li>
    <li><a href="sobre-el-proyecto.html">Sobre el proyecto</a></li>
  </ul>
</nav>
```

Para agregar un ítem al menú: agregá un `<li><a href="...">Texto</a></li>` dentro de `<ul class="nav-links">`.

---

### 4.2 Barra de temas

Solo en las páginas de tema. El tema activo lleva la clase `activo`.

```html
<div class="nav-temas">
  <a href="tema-1-identidad.html" class="activo">01 · Identidad</a>
  <a href="tema-2-privacidad.html">02 · Privacidad</a>
  <!-- ... -->
</div>
```

Para marcar el tema activo: la clase `activo` se pone en el `<a>` del tema cuya página estás viendo.

---

### 4.3 Cabezal de tema

```html
<header class="tema-header">
  <div class="tema-header-inner">
    <div class="tema-numero-grande">01</div>   <!-- número decorativo, opacidad baja -->
    <span class="tema-etiqueta">Tema 01</span>
    <h1>Identidad y huella digital</h1>
    <p>Descripción breve del tema...</p>
    <span class="tema-dimension">Dimensión: Comprensión del entorno digital</span>
  </div>
</header>
```

El color del cabezal viene de `--color-tema` y `--color-tema-claro` definidos en el `<style>` de cada página.

---

### 4.4 Acordeón

Es el componente central de las páginas de tema. Cada bloque de acordeón tiene esta estructura:

```html
<div class="acordeon-item">

  <!-- BOTÓN que abre/cierra -->
  <button class="acordeon-btn" onclick="toggleAcordeon(this)">
    <div class="acordeon-btn-izq">
      <div class="acordeon-icono" style="background:#E0F2F1;">🧭</div>
      <div>
        <div class="acordeon-titulo">Marco conceptual</div>
        <div class="acordeon-subtitulo">Qué es el tema y por qué importa</div>
      </div>
    </div>
    <span class="acordeon-flecha">▾</span>
  </button>

  <!-- CONTENIDO (se muestra/oculta) -->
  <div class="acordeon-contenido">
    <!-- Texto, cajas, listas, etc. -->
  </div>

</div>
```

**Para que un acordeón empiece abierto**: agrega la clase `abierto` al botón y la clase `visible` al contenido:

```html
<button class="acordeon-btn abierto" ...>
<div class="acordeon-contenido visible">
```

**JavaScript que lo controla** (al final de cada página de tema):

```javascript
function toggleAcordeon(btn) {
  const contenido = btn.nextElementSibling;
  const estaAbierto = btn.classList.contains('abierto');
  btn.classList.toggle('abierto', !estaAbierto);
  contenido.classList.toggle('visible', !estaAbierto);
}
```

---

### 4.5 Tabs de nivel (Ciclo básico / Bachillerato)

Dentro de la Guía docente. Permite alternar entre dos paneles de contenido.

```html
<!-- Botones de pestaña -->
<div class="tabs-nivel">
  <button class="tab-nivel activo" onclick="cambiarNivel(this, 'basico')">Ciclo básico</button>
  <button class="tab-nivel" onclick="cambiarNivel(this, 'bachillerato')">Bachillerato</button>
</div>

<!-- Paneles de contenido -->
<div class="panel-nivel visible" id="panel-basico">
  <!-- Contenido para ciclo básico -->
</div>

<div class="panel-nivel" id="panel-bachillerato">
  <!-- Contenido para bachillerato -->
</div>
```

**JavaScript**:

```javascript
function cambiarNivel(tab, nivel) {
  const tabs = tab.parentElement.querySelectorAll('.tab-nivel');
  const paneles = tab.closest('.acordeon-contenido').querySelectorAll('.panel-nivel');
  tabs.forEach(t => t.classList.remove('activo'));
  paneles.forEach(p => p.classList.remove('visible'));
  tab.classList.add('activo');
  document.getElementById('panel-' + nivel).classList.add('visible');
}
```

---

### 4.6 Cajas de contenido

Son bloques con fondo de color que destacan información dentro del acordeón. Cada tipo tiene su propia clase:

| Tipo | Clase | Fondo | Borde | Uso |
|------|-------|-------|-------|-----|
| Actividad | `caja-actividad` | verde claro | verde | Descripción de la dinámica de aula |
| Nivel | `caja-nivel` | violeta claro | violeta | Orientaciones CB / bachillerato |
| Crítica | `caja-critica` | coral claro | coral | Momento crítico con preguntas |
| IA | `caja-ia` | morado claro | morado | Integración de IA en el tema |
| Ley (T6) | `caja-ley` | coral claro | coral | Descripción de leyes uruguayas |

Ejemplo de caja-actividad:

```html
<div class="caja-actividad">
  <div class="caja-actividad-titulo">📋 "Nombre de la actividad"</div>
  <p><strong>Duración estimada</strong>: 50 minutos</p>
  <p>Descripción...</p>
</div>
```

---

### 4.7 Entradas disciplinares

Dos columnas: Informática y Educación para la Ciudadanía.

```html
<div class="entradas-grid">

  <div class="entrada-card informatica">
    <h4>💻 Desde Informática</h4>
    <p>Contenido específico...</p>
    <p><strong>Pregunta guía</strong>: ¿...?</p>
  </div>

  <div class="entrada-card ciudadania">
    <h4>⚖️ Desde Ed. para la Ciudadanía</h4>
    <p>Contenido específico...</p>
    <p><strong>Pregunta guía</strong>: ¿...?</p>
  </div>

</div>
```

---

### 4.8 Encabezado de material

Aparece en todas las páginas de materiales (tarjetas, VF, ficha, conceptos).

```html
<div class="material-header">
  <div class="material-header-inner">

    <div class="material-meta">
      <div class="material-ruta">
        <a href="index.html">Inicio</a> → 
        <a href="tema-1-identidad.html">Tema 01</a> → 
        Tarjetas de casos
      </div>
      <h1>Tarjetas de casos</h1>
      <p>Descripción breve...</p>
      <div class="material-badges">
        <span class="badge badge-verde">Identidad</span>
        <span class="badge badge-violeta">CB y bachillerato</span>
        <span class="badge badge-coral">Actividad grupal</span>
      </div>
    </div>

    <div class="material-acciones">
      <button onclick="window.print()">🖨️ Imprimir / PDF</button>
      <!-- otros botones según el tipo de material -->
    </div>

  </div>
</div>
```

**Badges disponibles**: `badge-verde`, `badge-violeta`, `badge-coral`, `badge-amarillo`.

---

### 4.9 Tarjeta con modal (Tarjetas de casos)

Cada tarjeta es clickeable y abre un modal con el caso completo.

```html
<!-- TARJETA -->
<div class="tarjeta" onclick="abrirModal('m1')">
  <div class="tarjeta-header">
    <span class="tarjeta-numero">Tarjeta 01</span>
    <span class="tarjeta-tipo">Tipo</span>
  </div>
  <div class="tarjeta-cuerpo">
    <div class="tarjeta-situacion">Título del caso</div>
    <p class="tarjeta-descripcion">Descripción breve...</p>
    <div class="tarjeta-pregunta">¿Pregunta disparadora?</div>
  </div>
  <div class="tarjeta-pie">👥 Grupal · 💬 Debate</div>
</div>

<!-- MODAL -->
<div class="modal-overlay" id="m1" onclick="cerrarModal('m1')">
  <div class="modal" onclick="event.stopPropagation()">
    <div class="modal-header">
      <div><!-- título y subtítulo --></div>
      <button onclick="cerrarModal('m1')">✕</button>
    </div>
    <div class="modal-body">
      <p>Descripción completa del caso...</p>
      <div class="modal-preguntas">
        <p>Preguntas para debatir</p>
        <ul>
          <li>Pregunta 1</li>
          <li>Pregunta 2</li>
        </ul>
      </div>
      <button class="modal-cerrar" onclick="cerrarModal('m1')">Cerrar</button>
    </div>
  </div>
</div>
```

**JavaScript**:

```javascript
function abrirModal(id) {
  document.getElementById(id).classList.add('visible');
  document.body.style.overflow = 'hidden';
}
function cerrarModal(id) {
  document.getElementById(id).classList.remove('visible');
  document.body.style.overflow = '';
}
// Cierre con tecla Escape:
document.addEventListener('keydown', e => {
  if (e.key === 'Escape') {
    document.querySelectorAll('.modal-overlay.visible')
      .forEach(m => m.classList.remove('visible'));
    document.body.style.overflow = '';
  }
});
```

---

### 4.10 Guardado automático (Ficha de producción)

La ficha guarda el contenido en `localStorage` del navegador cada vez que el usuario escribe, con un retardo de 800ms para no guardar en cada tecla.

```javascript
const CLAVE_STORAGE = 'ficha-t1';  // distinta en cada tema
const CAMPOS = ['campo-nombre', 'campo-año', 'campo-fecha', /* ... */];
let timerGuardado;

function guardarAutomatico() {
  actualizarEstado('guardando', '⏳ Guardando...');
  const datos = {};
  CAMPOS.forEach(id => {
    const el = document.getElementById(id);
    if (el) datos[id] = el.value;
  });
  localStorage.setItem(CLAVE_STORAGE, JSON.stringify(datos));
  setTimeout(() => actualizarEstado('guardado', '✓ Guardado'), 500);
  setTimeout(() => actualizarEstado('', '💾 Guardado automático'), 2500);
}

// Escuchar cambios en todos los campos:
CAMPOS.forEach(id => {
  const el = document.getElementById(id);
  if (el) el.addEventListener('input', () => {
    clearTimeout(timerGuardado);
    timerGuardado = setTimeout(guardarAutomatico, 800);
  });
});
```

El estado visual se muestra en el elemento `.guardado-estado`:

```javascript
function actualizarEstado(clase, texto) {
  const el = document.getElementById('estado-guardado');
  el.className = 'guardado-estado' + (clase ? ' ' + clase : '');
  el.textContent = texto;
}
```

---

### 4.11 Descarga de PDF (Ficha de producción)

Usa la librería `html2pdf.js` cargada desde CDN. El proceso clona el formulario, reemplaza los inputs y textareas por divs con el texto ingresado, y genera el PDF.

```javascript
function descargarPDF() {
  const original = document.getElementById('ficha-contenido');
  const clon = original.cloneNode(true);

  // Reemplazar inputs por spans con el valor
  clon.querySelectorAll('input[type="text"]').forEach(el => {
    const span = document.createElement('span');
    span.textContent = el.value || '___';
    span.style.cssText = 'border-bottom:1px solid #ccc; display:inline-block; min-width:80px;';
    el.parentNode.replaceChild(span, el);
  });

  // Reemplazar textareas por divs con el valor
  clon.querySelectorAll('textarea').forEach(el => {
    const div = document.createElement('div');
    div.textContent = el.value || ' ';
    div.style.cssText = 'border:1px solid #ccc; border-radius:6px; padding:0.5rem; min-height:50px; white-space:pre-wrap;';
    el.parentNode.replaceChild(div, el);
  });

  html2pdf().set({
    margin: [10, 10, 10, 10],
    filename: 'ficha-identidad.pdf',
    image: { type: 'jpeg', quality: 0.95 },
    html2canvas: { scale: 2, useCORS: true },
    jsPDF: { unit: 'mm', format: 'a4', orientation: 'portrait' }
  }).from(clon).save();
}
```

---

### 4.12 Tarjeta flip (Conceptos)

El efecto de giro 3D se logra solo con CSS. El JavaScript solo agrega y quita la clase `girada`.

```html
<div class="tarjeta-flip" onclick="this.classList.toggle('girada')">
  <div class="tarjeta-flip-inner">

    <div class="tarjeta-frente">
      <div class="tarjeta-termino">Término</div>
      <div class="tarjeta-pista">Hacé clic para ver la definición</div>
    </div>

    <div class="tarjeta-dorso">
      <div class="tarjeta-definicion">Definición del término...</div>
      <div class="tarjeta-dorso-termino">Término</div>
    </div>

  </div>
</div>
```

El CSS que hace el giro (en `estilos.css`):

```css
.tarjeta-flip { perspective: 1000px; }
.tarjeta-flip-inner { transition: transform 0.5s; transform-style: preserve-3d; }
.tarjeta-flip.girada .tarjeta-flip-inner { transform: rotateY(180deg); }
.tarjeta-frente, .tarjeta-dorso { backface-visibility: hidden; }
.tarjeta-dorso { transform: rotateY(180deg); }
```

---

## 5. Cómo hacer cambios frecuentes

| Quiero cambiar... | Dónde |
|-------------------|-------|
| El color de un tema | `<style>` de ese archivo HTML (2 variables) |
| Un color en todo el sitio | `estilos.css`, sección 1 (Variables) |
| La tipografía | `estilos.css`, variables `--font-titulo` y `--font-texto` |
| El texto de una tarjeta de caso | En el HTML del material correspondiente, buscar el modal por id (m1, m2...) |
| Una afirmación del VF | En el array `afs` al final del HTML del VF correspondiente |
| Un concepto flip | En el array `conceptos` al final del HTML de conceptos |
| Las preguntas de una ficha | En las etiquetas `<label>` y `<p class="ficha-pregunta">` |
| Agregar un ítem al menú nav | En todos los HTML, en `<ul class="nav-links">` |
| Agregar un video (Mirada experta) | Agregar un bloque `<div class="acordeon-item">` nuevo en la página de tema |

---

## 6. Dependencias externas

| Librería | Versión | URL | Uso |
|----------|---------|-----|-----|
| Google Fonts (Nunito + Open Sans) | — | fonts.googleapis.com | Tipografías |
| html2pdf.js | 0.10.1 | cdnjs.cloudflare.com | Descarga PDF en fichas |

No hay otras dependencias. El sitio no usa frameworks, no tiene base de datos, y no requiere servidor.

---

*Documentación generada en septiembre 2026.*
