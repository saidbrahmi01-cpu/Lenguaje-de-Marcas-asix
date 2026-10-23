# UD2.1 - CSS Básico

**Actividad:** UD2.1  
**Curso:** 1CFGS - Lenguaje de marcas y sistemas de gestión de la información  
**Fecha:** 2026

---

## 1. Tres formas de incluir CSS

### Requisitos

1. Tres páginas con el mismo contenido: un `<h1>` y dos párrafos.
2. `ej1a_inline.html` con el atributo `style`.
3. `ej1b_style.html` con una etiqueta `<style>` en el `<head>`.
4. `ej1c_externo.html` con un archivo `estilos.css` enlazado con `<link>`.
5. Mismo resultado: `<h1>` azul oscuro y centrado, párrafos en Arial y color gris.
6. Un `README.md` respondiendo a las dos preguntas.

### Estructura de carpetas

```text
ud21_ej1/
├── ej1a_inline.html
├── ej1b_style.html
├── ej1c_externo.html
├── estilos.css
└── README.md
```

### Código `ud21_ej1/ej1a_inline.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>CSS en línea</title>
</head>
<body>
    <h1 style="color: navy; text-align: center;">El café</h1>
    <p style="font-family: Arial, sans-serif; color: #555555;">El café es una de las bebidas más consumidas del mundo. Se prepara a partir de los granos tostados de la planta del cafeto.</p>
    <p style="font-family: Arial, sans-serif; color: #555555;">Existen muchas formas de tomarlo: solo, con leche, cortado o con hielo, según el gusto de cada persona.</p>
</body>
</html>
```

### Código `ud21_ej1/ej1b_style.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>CSS en etiqueta style</title>
    <style>
        h1 {
            color: navy;
            text-align: center;
        }
        p {
            font-family: Arial, sans-serif;
            color: #555555;
        }
    </style>
</head>
<body>
    <h1>El café</h1>
    <p>El café es una de las bebidas más consumidas del mundo. Se prepara a partir de los granos tostados de la planta del cafeto.</p>
    <p>Existen muchas formas de tomarlo: solo, con leche, cortado o con hielo, según el gusto de cada persona.</p>
</body>
</html>
```

### Código `ud21_ej1/ej1c_externo.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>CSS externo</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>
    <h1>El café</h1>
    <p>El café es una de las bebidas más consumidas del mundo. Se prepara a partir de los granos tostados de la planta del cafeto.</p>
    <p>Existen muchas formas de tomarlo: solo, con leche, cortado o con hielo, según el gusto de cada persona.</p>
</body>
</html>
```

### Código `ud21_ej1/estilos.css`

```css
h1 {
    color: navy;
    text-align: center;
}

p {
    font-family: Arial, sans-serif;
    color: #555555;
}
```

### Archivo `ud21_ej1/README.md`

> **¿Cuál de las tres formas es la más cómoda para cambiar el color del título en 10 páginas?**
> La del archivo externo. Se cambia el color una sola vez en `estilos.css` y las 10 páginas se actualizan a la vez. Con `<style>` habría que editar las 10 páginas, y con `style` en línea habría que buscar y editar cada `<h1>` de cada página.
>
> **¿Por qué se desaconseja la primera?**
> El CSS en línea mezcla el contenido con la presentación, obliga a repetir el mismo estilo en cada elemento, no se puede reutilizar, hace el código más largo y difícil de mantener, y como tiene mucha prioridad resulta difícil de sobrescribir después.

### Conclusión

Las tres formas dan el mismo resultado visual, pero el archivo externo separa el contenido del diseño y permite reutilizar el estilo en todo el sitio.

---

## 2. Mis primeras reglas de estilo

### Requisitos

1. Selector universal `*` para la fuente de toda la página.
2. Selectores de tipo para dar color a `<h1>` y `<h2>` y justificar los `<p>`.
3. Al menos una regla con tres o más declaraciones.
4. Cambiar el orden de la regla universal y anotar el resultado en un comentario.

### Estructura de carpetas

```text
ud21_ej2/
├── index.html
└── estilos.css
```

### Código `ud21_ej2/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Tortilla de patatas</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>
    <h1>Tortilla de patatas</h1>
    <h2>Ingredientes</h2>
    <p>Pocos ingredientes, pero la calidad importa.</p>
    <ul>
        <li>Patatas</li>
        <li>Huevos</li>
        <li>Cebolla</li>
    </ul>
    <h2>Elaboración</h2>
    <p>Fríe las patatas, mezcla con el huevo y cuaja la tortilla.</p>
</body>
</html>
```

### Código `ud21_ej2/estilos.css`

```css
/*
   PRUEBA DEL ORDEN DE LA REGLA UNIVERSAL
   He puesto la regla * primero y luego la he movido al final del archivo.
   El resultado NO cambia. El selector universal tiene la menor especificidad
   (0,0,0), así que cualquier selector de tipo (como h2, con 0,0,1) gana
   siempre sobre él, esté antes o después. Por eso h2 sigue en Georgia aunque
   * esté al final. El orden solo importa cuando dos reglas tienen la misma
   especificidad.
*/

* {
    font-family: Arial, sans-serif;
}

h1 {
    color: darkred;
    text-align: center;
    text-decoration: underline;
}

h2 {
    color: seagreen;
    font-family: Georgia, serif;
}

p {
    text-align: justify;
}
```

### Conclusión

Los selectores de tipo se aplican a todas las etiquetas de ese nombre. El selector universal `*` sirve para fijar valores generales, y los selectores más específicos los sobrescriben.

---

## 3. Descendientes y clases

### Requisitos

1. `<em>` del `<h1>` en naranja sin cambiar el `<em>` del `<li>`.
2. Fondo gris claro solo para los `<p>` dentro de `<li>`.
3. Borde izquierdo solo para los `<p>` dentro de `.comentarios`.
4. Regla `p.especial` que afecte a los dos párrafos con esa clase.
5. Un `<span class="especial">` y la regla `.especial` para que le afecte.

### Estructura de carpetas

```text
ud21_ej3/
├── index.html
└── estilos.css
```

### Código `ud21_ej3/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Novedades de la semana</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>
    <div class="articulo">
        <h1>Novedades de la <em>semana</em></h1>
        <p>Resumen de lo más importante. <span class="especial">Leer más</span></p>
        <ul>
            <li><p>Nuevo <em>framework</em> de JavaScript.</p></li>
            <li><p>Actualización de seguridad en Windows.</p></li>
        </ul>
    </div>
    <div class="comentarios">
        <p>Comentario de Ana: ¡muy interesante!</p>
        <p class="especial">Respuesta de la redacción: gracias.</p>
    </div>
    <p class="especial">Nota final del autor.</p>
</body>
</html>
```

### Código `ud21_ej3/estilos.css`

```css
/* 1. El em dentro del h1 (no afecta al em del li) */
h1 em {
    color: orange;
}

/* 2. Solo los p que están dentro de un li */
li p {
    background-color: #eeeeee;
}

/* 3. Solo los p dentro de .comentarios */
.comentarios p {
    border-left: 4px solid #2c3e50;
    padding-left: 10px;
}

/* 4. Solo los p con clase especial (el span NO se ve afectado) */
p.especial {
    color: crimson;
    font-style: italic;
}

/* 5. Cualquier elemento con clase especial, incluido el span */
.especial {
    font-weight: bold;
    text-decoration: underline;
}
```

### Conclusión

El selector de descendientes (`h1 em`, `li p`) elige elementos según dónde están dentro del HTML. `p.especial` solo afecta a párrafos con esa clase, mientras que `.especial` afecta a cualquier etiqueta que la tenga, por eso hace falta para el `<span>`.

---

## 4. Identificadores y atributos

### Parte A - Selector de id

### Requisitos

1. `<h1 id="corp">` estilizado con selector de id.
2. Duplicar el `id` en un `<h2>`, validar y copiar el error en el README.
3. Corregir convirtiendo el id repetido en clase y explicar por qué se desaconseja el selector de id.

### Estructura de carpetas

```text
ud21_ej4/
├── index.html
├── estilos.css
└── README.md
```

### Código con el error (id duplicado)

```html
<h1 id="corp">Mi página</h1>
<h2 id="corp">Subtítulo</h2>
```

### Archivo `ud21_ej4/README.md`

> **Mensaje del validador de W3C al duplicar el id:**
> `Error: Duplicate ID corp.`
> (el validador añade además una línea indicando dónde estaba la primera aparición del id; copia aquí el mensaje exacto que te salga a ti).
>
> **Corrección:** el `<h1>` conserva `id="corp"` y el `<h2>` pasa a tener `class="corp"`.
>
> **¿Por qué se desaconseja usar selectores de id para estilizar?**
> Porque un `id` debe ser único en toda la página y por tanto no se puede reutilizar en otros elementos. Además tiene una especificidad muy alta, lo que obliga a escribir reglas aún más específicas para sobrescribirlo y hace el CSS difícil de mantener. Las clases se pueden reutilizar tantas veces como haga falta.

### Parte B - Selector de atributo

### Requisitos

1. Lista de enlaces, algunos con `target="_blank"`.
2. Selector de atributo para dar color solo a los enlaces con `target`.
3. Párrafos con y sin `class` y selector de atributo para estilizar solo los que tienen `class`.

### Código `ud21_ej4/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Identificadores y atributos</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>
    <h1 id="corp">Mi página</h1>
    <h2 class="corp">Subtítulo</h2>

    <h2>Enlaces</h2>
    <ul>
        <li><a href="https://developer.mozilla.org/es/" target="_blank">MDN Web Docs</a></li>
        <li><a href="https://www.w3schools.com/">W3Schools</a></li>
        <li><a href="https://github.com/" target="_blank">GitHub</a></li>
        <li><a href="https://validator.w3.org/">Validador de W3C</a></li>
    </ul>

    <h2>Párrafos</h2>
    <p>Este párrafo no tiene clase.</p>
    <p class="nota">Este párrafo tiene la clase nota.</p>
    <p>Este otro tampoco tiene clase.</p>
    <p class="aviso">Este párrafo tiene la clase aviso.</p>
</body>
</html>
```

### Código `ud21_ej4/estilos.css`

```css
/* Selector de id (solo un elemento) */
#corp {
    color: darkred;
}

/* Selector de clase (reutilizable) */
.corp {
    color: darkred;
}

/* Selector de atributo: enlaces que tienen el atributo target */
a[target] {
    color: darkorange;
    font-weight: bold;
}

/* Selector de atributo: párrafos que tienen el atributo class */
p[class] {
    background-color: #fff3cd;
    padding: 5px;
}
```

### Conclusión

Los selectores de atributo (`a[target]`, `p[class]`) eligen elementos según los atributos que tienen. Los `id` no se pueden repetir, por eso para estilos conviene usar clases.

---

## 5. Reto: colisiones y refactorización

### Parte A - Detective de colisiones

### Estructura de carpetas

```text
ud21_ej5/
├── index.html
├── estilos.css
├── README.md
├── cv.html
└── cv.css
```

### Código `ud21_ej5/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Colisiones CSS</title>
    <link rel="stylesheet" href="estilos.css">
</head>
<body>
    <h1 id="titulo" class="grande">Hola CSS</h1>
    <p class="aviso">Texto 1</p>
    <p class="aviso" id="importante">Texto 2</p>
    <div><p>Texto 3</p></div>
</body>
</html>
```

### Código `ud21_ej5/estilos.css`

```css
p { color: blue; }
p { color: green; }
.aviso { color: red; }
div p { color: orange; }
p.aviso { color: purple; }
#importante { color: black; }
h1 { color: gray; }
.grande { color: teal; }
#titulo { color: brown; }
```

### Archivo `ud21_ej5/README.md`

> **Predicciones y resultados** (especificidad escrita como id, clase, etiqueta):

| Elemento | Reglas que le afectan | Color final | Motivo |
|---|---|---|---|
| `<h1>` | `h1` (0,0,1), `.grande` (0,1,0), `#titulo` (1,0,0) | **brown** | El selector de id es el más específico. |
| Texto 1 | `p` (0,0,1) dos veces, `.aviso` (0,1,0), `p.aviso` (0,1,1) | **purple** | `p.aviso` suma etiqueta y clase y supera a `.aviso`. |
| Texto 2 | las mismas que Texto 1 y además `#importante` (1,0,0) | **black** | El id gana a todas las demás reglas. |
| Texto 3 | `p` (0,0,1) dos veces, `div p` (0,0,2) | **orange** | `div p` suma dos etiquetas y supera a `p`, aunque `p { color: green; }` aparezca después. |

> **Comprobación con el inspector (F12):** completa esta parte con el resultado que veas en tu navegador. Si alguna predicción no coincide con la tabla, corrígela aquí y explica el motivo. Recuerda que entre dos reglas con la misma especificidad gana la última, como pasa con `p { color: blue; }` y `p { color: green; }`.

### Parte B - Refactorización

Se refactoriza el currículum de la UD1.2 (`ud12_ej4`): se eliminan todos los atributos `style` y se pasan a `cv.css`.

### Código `ud21_ej5/cv.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Currículum - Tu Nombre</title>
    <link rel="stylesheet" href="cv.css">
</head>
<body>
    <h1>Tu Nombre Apellidos</h1>

    <h2>Perfil</h2>
    <p>Estudiante motivado con interés en el <strong>desarrollo de aplicaciones</strong> y en
    las <em>tecnologías web</em>. Me gusta aprender cosas nuevas y trabajar en equipo.</p>

    <h2>Formación</h2>
    <p>Ciclo Formativo de Grado Superior en <strong><em>Desarrollo de Aplicaciones
    Multiplataforma</em></strong>, actualmente en primer curso.</p>

    <h2>Habilidades</h2>
    <ul>
        <li class="habilidad">HTML5</li>
        <li class="habilidad">Trabajo en equipo</li>
        <li class="habilidad">Control de versiones con Git</li>
    </ul>

    <h2>Contacto</h2>
    <address>
        Correo: <a href="mailto:tunombre@ejemplo.es">tunombre@ejemplo.es</a><br>
        Teléfono: 600 000 000
    </address>
</body>
</html>
```

### Código `ud21_ej5/cv.css`

```css
/* ===== ENCABEZADOS ===== */
/* Agrupación de selectores separados por comas: comparten estilo */
h1, h2 {
    color: #2c3e50;
}

/* Agrupación de declaraciones para un mismo elemento */
h1 {
    color: white;
    background-color: #2c3e50;
    font-size: 36px;
}

h2 {
    font-size: 24px;
}

/* ===== LISTA DE HABILIDADES ===== */
/* Selector de clase */
.habilidad {
    color: #1a5276;
    background-color: #eaf2f8;
    font-size: 18px;
}
```

### Conclusión

Cuando dos reglas chocan gana la más específica, y si tienen la misma especificidad gana la última. Mover los estilos de los atributos `style` a un archivo CSS separa el contenido del diseño y permite agrupar selectores y reutilizar clases.

---
