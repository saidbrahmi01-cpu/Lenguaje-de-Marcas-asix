# UD1.2 - Formato de texto

**Actividad:** UD1.2  
**Curso:** 1CFGS - Lenguaje de marcas y sistemas de gestión de la información  
**Fecha:** 2026

---

## 1. Estructura con títulos y párrafos

### Requisitos

1. Un `<h1>` con el título general de la página.
2. Al menos tres secciones, cada una con su propio `<h2>`.
3. Cada sección contiene al menos un párrafo `<p>` de 3 líneas como mínimo.
4. Una de las secciones incluye un `<h3>` para crear una subsección.

### Código `ud12_ej1.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Sevilla - Guía de la ciudad</title>
</head>
<body>
    <h1>Sevilla, ciudad del sur de España</h1>

    <h2>Historia</h2>
    <p>Sevilla fue fundada hace más de dos mil años y ha sido un enclave fundamental en la
    historia de la península ibérica. Pasó por manos de romanos, musulmanes y castellanos, y
    todas estas culturas han dejado su huella en sus calles y monumentos.</p>
    <p>Durante los siglos XVI y XVII fue el puerto principal del comercio con América, lo que
    la convirtió en una de las ciudades más ricas y pobladas de Europa.</p>

    <h2>Gastronomía</h2>
    <p>La cocina sevillana se basa en productos del mercado y en recetas tradicionales que se
    han transmitido de generación en generación. El aceite de oliva, el jamón y el pescado frito
    son protagonistas habituales de cualquier comida.</p>

    <h3>Tapas típicas</h3>
    <p>Ir de tapas es casi una tradición social. Entre las más populares están las espinacas con
    garbanzos, el salmorejo y las croquetas caseras, que se suelen tomar acompañadas de una caña
    en cualquier bar del centro.</p>

    <h2>Lugares de interés</h2>
    <p>La Giralda, la Catedral y el Real Alcázar forman un conjunto monumental declarado
    Patrimonio de la Humanidad. A pocos pasos se encuentra el Barrio de Santa Cruz, con sus
    callejuelas estrechas y sus patios llenos de flores.</p>
</body>
</html>
```

### Conclusión

Los encabezados `<h1>` a `<h6>` organizan el documento de forma jerárquica: un único `<h1>` como título general, `<h2>` para las secciones y `<h3>` para las subsecciones.

---

## 2. Formato de texto enriquecido

### Requisitos

1. "Envío gratuito en pedidos superiores a 50 euros" con `<strong>`.
2. La cita de Aristóteles dentro de un `<blockquote>`.
3. "descatalogado" con `<em>`.
4. "XR200" con `<mark>` (se usa tal como aparece en el texto base).
5. Precio anterior con `<del>` y precio actual con `<ins>`.
6. Un salto de línea `<br>` y una línea horizontal `<hr>` para separar los precios.

### Código `ud12_ej2.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Tienda online</title>
</head>
<body>
    <h1>Bienvenido a nuestra tienda online</h1>

    <p><strong>Envío gratuito en pedidos superiores a 50 euros.</strong></p>

    <blockquote>
        "La calidad no es un acto, es un hábito" - Aristóteles.
    </blockquote>

    <p>Advertencia: el producto ha sido <em>descatalogado</em> y sustituido por el modelo
    <mark>XR200</mark>.</p>

    <hr>

    <p>Precio anterior: <del>39,99 euros</del>.<br>
    Precio actual: <ins>29,99 euros</ins>.</p>
</body>
</html>
```

### Conclusión

Cada etiqueta aporta un significado: `<strong>` indica importancia, `<em>` énfasis, `<mark>` texto resaltado, `<del>` contenido eliminado e `<ins>` contenido añadido.

---

## 3. Ficha técnica con etiquetas semánticas

### Requisitos

1. `<abbr>` con el atributo `title`.
2. `<code>` para una línea de código o comando.
3. `<kbd>` para una combinación de teclas.
4. `<dfn>` en la primera definición de un término técnico.
5. `<time datetime="aaaa-mm-dd">` para una fecha relevante.
6. `<address>` con datos de contacto ficticios.
7. Al menos un uso de `<sub>` o `<sup>`.

### Código `ud12_ej3.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Ficha técnica: Git</title>
</head>
<body>
    <h1>Ficha técnica: Git</h1>

    <h2>Descripción</h2>
    <p>Git es un sistema de control de versiones (<abbr title="Version Control System">VCS</abbr>)
    distribuido. Un <dfn>repositorio</dfn> es la carpeta donde Git almacena el historial de
    cambios de un proyecto.<sup>1</sup></p>

    <h2>Fecha de lanzamiento</h2>
    <p>Git fue creado por Linus Torvalds y se publicó el
    <time datetime="2005-04-07">7 de abril de 2005</time>.</p>

    <h2>Comandos básicos</h2>
    <p>Para guardar los cambios en el historial se usa el comando
    <code>git commit -m "mensaje"</code>.</p>

    <h2>Atajos en VSCode</h2>
    <p>Para guardar un archivo antes de hacer el commit, pulsa
    <kbd>Ctrl</kbd> + <kbd>S</kbd>.</p>

    <h2>Notas</h2>
    <p><sup>1</sup> Cada copia del repositorio contiene el historial completo del proyecto.</p>

    <h2>Autor de la ficha</h2>
    <address>
        Ana García López<br>
        Correo: <a href="mailto:ana.garcia@ejemplo.es">ana.garcia@ejemplo.es</a><br>
        Teléfono: 600 123 456
    </address>
</body>
</html>
```

### Conclusión

Estas etiquetas no sirven solo para cambiar el aspecto del texto, sino para dar significado: `<code>` es para código, `<kbd>` para teclas, `<abbr>` para siglas, `<dfn>` para definiciones y `<time>` para fechas legibles por máquinas.

---

## 4. Reto: mini currículum con estilos inline

### Requisitos

1. `<h1>` con el nombre y `<h2>` para cada sección.
2. `<strong>` y `<em>` para destacar información.
3. Una lista para las habilidades.
4. `<address>` para los datos de contacto.
5. Atributo `style` en al menos tres elementos con `color`, `background-color` y `font-size`.
6. Etiquetas anidadas cerradas en el orden correcto.

### Código `ud12_ej4.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Currículum - Tu Nombre</title>
</head>
<body>
    <h1 style="color: white; background-color: #2c3e50; font-size: 36px;">Tu Nombre Apellidos</h1>

    <h2 style="color: #2c3e50; font-size: 24px;">Perfil</h2>
    <p>Estudiante motivado con interés en el <strong>desarrollo de aplicaciones</strong> y en
    las <em>tecnologías web</em>. Me gusta aprender cosas nuevas y trabajar en equipo.</p>

    <h2 style="color: #2c3e50; font-size: 24px;">Formación</h2>
    <p>Ciclo Formativo de Grado Superior en <strong><em>Desarrollo de Aplicaciones
    Multiplataforma</em></strong>, actualmente en primer curso.</p>

    <h2 style="color: #2c3e50; font-size: 24px;">Habilidades</h2>
    <ul>
        <li style="color: #1a5276; background-color: #eaf2f8; font-size: 18px;">HTML5</li>
        <li style="color: #1a5276; background-color: #eaf2f8; font-size: 18px;">Trabajo en equipo</li>
        <li style="color: #1a5276; background-color: #eaf2f8; font-size: 18px;">Control de versiones con Git</li>
    </ul>

    <h2 style="color: #2c3e50; font-size: 24px;">Contacto</h2>
    <address>
        Correo: <a href="mailto:tunombre@ejemplo.es">tunombre@ejemplo.es</a><br>
        Teléfono: 600 000 000
    </address>
</body>
</html>
```

### Conclusión

El atributo `style` permite aplicar estilos directamente a un elemento. Las etiquetas anidadas se cierran en orden inverso al de apertura: en `<strong><em>texto</em></strong>` se cierra primero `</em>` y después `</strong>`.

---
