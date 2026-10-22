# UD1.4 - Enlaces

**Actividad:** UD1.4  
**Curso:** 1CFGS - Lenguaje de marcas y sistemas de gestión de la información  
**Fecha:** 2026

---

## 1. Enlaces externos

### Requisitos

1. Al menos 4 enlaces externos reales.
2. Cada enlace con un rótulo descriptivo.
3. Al menos un enlace con `target="_blank"`.
4. Enlaces organizados en una lista `<ul>` con `<li>`.

### Estructura de carpetas

```text
14_1/
└── index.html
```

### Código `14_1/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Enlaces de interés para el desarrollo web</title>
</head>
<body>
    <h1>Enlaces de interés para el desarrollo web</h1>

    <p>Recopilación de recursos útiles para aprender y practicar desarrollo web.</p>

    <ul>
        <li><a href="https://developer.mozilla.org/es/" target="_blank">MDN Web Docs: documentación oficial de HTML, CSS y JavaScript</a></li>
        <li><a href="https://www.w3schools.com/">W3Schools: tutoriales y ejemplos para practicar</a></li>
        <li><a href="https://validator.w3.org/">Validador de W3C: comprueba que tu HTML es correcto</a></li>
        <li><a href="https://github.com/">GitHub: plataforma para alojar y compartir proyectos</a></li>
    </ul>
</body>
</html>
```

### Conclusión

La etiqueta `<a>` con el atributo `href` crea el enlace. Un rótulo descriptivo explica a dónde lleva el enlace, y `target="_blank"` hace que se abra en una pestaña nueva.

---

## 2. Navegación entre dos páginas

### Requisitos

1. `index.html` con un párrafo de bienvenida y un enlace "Sobre mí".
2. `sobre-mi.html` con una presentación y un enlace "Volver al inicio".
3. Ambos enlaces con rutas relativas.
4. Comprobar la navegación con Live Server.

### Estructura de carpetas

```text
14_2/
├── index.html
└── sobre-mi.html
```

### Código `14_2/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Inicio</title>
</head>
<body>
    <h1>Bienvenido a mi web</h1>

    <p>Hola, me alegra que hayas llegado hasta aquí. Esta es la página de inicio de mi
    pequeño sitio web.</p>

    <p><a href="sobre-mi.html">Sobre mí</a></p>
</body>
</html>
```

### Código `14_2/sobre-mi.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Sobre mí</title>
</head>
<body>
    <h1>Sobre mí</h1>

    <p>Me llamo Tu Nombre y estudio un Ciclo Formativo de Grado Superior. Me gusta la
    informática, aprender cosas nuevas y trabajar en proyectos en equipo.</p>

    <p><a href="index.html">Volver al inicio</a></p>
</body>
</html>
```

### Conclusión

Una ruta relativa como `sobre-mi.html` indica la posición del archivo respecto a la página actual. Funciona en cualquier ordenador mientras los archivos estén en la misma carpeta.

---

## 3. Tabla de contenidos con anclas

### Requisitos

1. Bloque "Índice" al principio con enlaces `href="#idSeccion"`.
2. Cada sección con un `<h2>` y su `id` correspondiente.
3. Al final de cada sección, un enlace "↑ Volver al índice".
4. Al menos 4 secciones con 2 párrafos reales cada una.

### Estructura de carpetas

```text
14_3/
└── index.html
```

### Código `14_3/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Guía de Git para principiantes</title>
</head>
<body>
    <h1 id="inicio">Guía de Git para principiantes</h1>

    <nav id="indice">
        <h2>Índice</h2>
        <ul>
            <li><a href="#que-es">¿Qué es Git?</a></li>
            <li><a href="#instalacion">Instalación</a></li>
            <li><a href="#comandos">Comandos básicos</a></li>
            <li><a href="#github">Subir proyectos a GitHub</a></li>
        </ul>
    </nav>

    <h2 id="que-es">¿Qué es Git?</h2>
    <p>Git es un sistema de control de versiones que guarda el historial de cambios de un
    proyecto. Gracias a él se puede volver a una versión anterior si algo sale mal.</p>
    <p>También permite que varias personas trabajen a la vez sobre el mismo proyecto sin
    pisarse el trabajo, algo fundamental en cualquier equipo de desarrollo.</p>
    <p><a href="#indice">↑ Volver al índice</a></p>

    <h2 id="instalacion">Instalación</h2>
    <p>Git se descarga desde su página oficial, git-scm.com, y está disponible para Windows,
    macOS y Linux. El instalador se puede dejar con las opciones por defecto.</p>
    <p>Para comprobar que se ha instalado bien, se abre una terminal y se escribe
    <code>git --version</code>. Si aparece un número de versión, ya está listo.</p>
    <p><a href="#indice">↑ Volver al índice</a></p>

    <h2 id="comandos">Comandos básicos</h2>
    <p>Con <code>git init</code> se crea un repositorio nuevo en la carpeta actual. Después,
    <code>git add .</code> prepara los archivos modificados para guardarlos.</p>
    <p>Para guardar los cambios en el historial se usa <code>git commit -m "mensaje"</code>.
    Conviene escribir mensajes claros que expliquen qué se ha cambiado.</p>
    <p><a href="#indice">↑ Volver al índice</a></p>

    <h2 id="github">Subir proyectos a GitHub</h2>
    <p>GitHub es una plataforma que aloja repositorios Git en internet. Primero se crea un
    repositorio vacío en la web y se copia su dirección.</p>
    <p>Después se conecta el proyecto con <code>git remote add origin dirección</code> y se
    suben los cambios con <code>git push -u origin main</code>.</p>
    <p><a href="#indice">↑ Volver al índice</a> | <a href="#inicio">Ir arriba del todo</a></p>
</body>
</html>
```

### Conclusión

Un enlace con `href="#id"` salta al elemento de la misma página que tenga ese `id`. Los `id` deben ser únicos dentro del documento.

---

## 4. Reto: mini sitio personal de 3 páginas

### Requisitos

1. Tres páginas: `index.html`, `proyectos.html` y `contacto.html`.
2. El mismo menú de navegación en la parte superior de las tres.
3. La página activa marcada con `<strong>` y sin enlace.
4. En `contacto.html`, un enlace `mailto:`.
5. En `proyectos.html`, un enlace de descarga con `download`.
6. En cada página, un enlace "Volver arriba" con un ancla interna.

### Estructura de carpetas

```text
14_4/
├── index.html
├── proyectos.html
├── contacto.html
└── cv.pdf
```

### Código `14_4/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Inicio - Mi sitio personal</title>
</head>
<body>
    <nav id="arriba">
        <ul>
            <li><strong>Inicio</strong></li>
            <li><a href="proyectos.html">Proyectos</a></li>
            <li><a href="contacto.html">Contacto</a></li>
        </ul>
    </nav>

    <h1>Hola, soy Tu Nombre</h1>
    <p>Bienvenido a mi sitio personal. Soy estudiante de desarrollo de aplicaciones y aquí
    puedes ver los proyectos en los que he trabajado y cómo contactar conmigo.</p>

    <p><a href="#arriba">Volver arriba</a></p>
</body>
</html>
```

### Código `14_4/proyectos.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Proyectos - Mi sitio personal</title>
</head>
<body>
    <nav id="arriba">
        <ul>
            <li><a href="index.html">Inicio</a></li>
            <li><strong>Proyectos</strong></li>
            <li><a href="contacto.html">Contacto</a></li>
        </ul>
    </nav>

    <h1>Mis proyectos</h1>

    <h2>Web de recetas</h2>
    <p>Página con recetas de cocina organizadas por categorías, creada con HTML.</p>

    <h2>Agenda de contactos</h2>
    <p>Pequeña aplicación para guardar nombres y teléfonos.</p>

    <h2>Portfolio personal</h2>
    <p>Este mismo sitio web, hecho de forma progresiva a lo largo del curso.</p>

    <p><a href="cv.pdf" download>Descargar CV</a></p>

    <p><a href="#arriba">Volver arriba</a></p>
</body>
</html>
```

### Código `14_4/contacto.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Contacto - Mi sitio personal</title>
</head>
<body>
    <nav id="arriba">
        <ul>
            <li><a href="index.html">Inicio</a></li>
            <li><a href="proyectos.html">Proyectos</a></li>
            <li><strong>Contacto</strong></li>
        </ul>
    </nav>

    <h1>Contacto</h1>
    <p>Si quieres ponerte en contacto conmigo, escríbeme un correo:</p>

    <p><a href="mailto:tunombre@ejemplo.com">Enviar un correo a tunombre@ejemplo.com</a></p>

    <p><a href="#arriba">Volver arriba</a></p>
</body>
</html>
```

### Conclusión

El menú repetido en todas las páginas permite navegar por el sitio y `<strong>` indica la página activa. El protocolo `mailto:` abre el programa de correo y el atributo `download` fuerza la descarga del archivo en lugar de abrirlo en el navegador.

---
