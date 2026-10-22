# UD2.3 - Imágenes

**Actividad:** UD2.3  
**Curso:** 1CFGS - Lenguaje de marcas y sistemas de gestión de la información  
**Fecha:** 2026

---

## 1. Tu primera imagen

### Requisitos

1. Imagen guardada en la carpeta `img/` del proyecto.
2. Insertada con `<img>` y ruta relativa.
3. Atributo `alt` con una descripción real.
4. Ancho de 400 píxeles con `width`.
5. Un párrafo debajo explicando qué se ve.

### Estructura de carpetas

```text
13_1/
├── index.html
└── img/
    └── playa.jpg
```

### Código `13_1/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Mi primera imagen</title>
</head>
<body>
    <h1>Mi primera imagen</h1>

    <img src="img/playa.jpg" alt="Playa de arena blanca con el mar azul y una palmera al fondo" width="400">

    <p>En la fotografía se ve una playa de arena blanca con aguas tranquilas de color azul.
    A la derecha hay una palmera y al fondo se distingue el horizonte con un cielo despejado.</p>
</body>
</html>
```

### Conclusión

La etiqueta `<img>` necesita siempre `src` (ruta de la imagen) y `alt` (texto alternativo). Una ruta relativa como `img/playa.jpg` funciona mientras la carpeta del proyecto se mantenga unida.

---

## 2. Galería de imágenes

### Requisitos

1. Las 4 imágenes dentro de un mismo `<div>`.
2. Cada imagen con su `alt`.
3. Ancho de cada imagen al 40% con `width="40%"`.
4. Un `<h2>` con el título de la galería.

### Estructura de carpetas

```text
13_2/
├── index.html
└── img/
    ├── foto1.jpg
    ├── foto2.jpg
    ├── foto3.jpg
    └── foto4.jpg
```

### Código `13_2/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Galería de imágenes</title>
</head>
<body>
    <h1>Mi ciudad</h1>

    <h2>Galería de Valencia</h2>

    <div>
        <img src="img/foto1.jpg" alt="Ciudad de las Artes y las Ciencias de Valencia al atardecer" width="40%">
        <img src="img/foto2.jpg" alt="Playa de la Malvarrosa con gente paseando por la arena" width="40%">
        <img src="img/foto3.jpg" alt="Plaza del Ayuntamiento de Valencia con su fuente y edificios históricos" width="40%">
        <img src="img/foto4.jpg" alt="Plato de paella valenciana con arroz, pollo y verduras" width="40%">
    </div>
</body>
</html>
```

### Conclusión

Al estar las imágenes dentro de un `<div>`, el porcentaje del ancho se calcula respecto al contenedor y no respecto a toda la página.

> Nota: en HTML5 el atributo `width` solo admite números enteros, por lo que `width="40%"` lo marca el validador de W3C. El ejercicio lo pide así para practicar el porcentaje; la alternativa válida es `style="width: 40%;"`.

---

## 3. Texto envolvente alrededor de una imagen

### Requisitos

1. Imagen con `float: left` o `float: right` mediante `style`.
2. Al menos 3 párrafos que se acomoden alrededor.
3. Un elemento con `style="clear: both;"` después del bloque de texto.
4. Un `<h1>` con el titular antes del bloque de imagen y texto.

### Estructura de carpetas

```text
13_3/
├── index.html
└── img/
    └── noticia.jpg
```

### Código `13_3/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Noticia</title>
</head>
<body>
    <h1>Inauguran un nuevo parque urbano en el centro de la ciudad</h1>

    <img src="img/noticia.jpg" alt="Vista del nuevo parque urbano con zonas verdes y un camino central" width="300" style="float: left; margin: 0 15px 10px 0;">

    <p>Lorem ipsum dolor sit amet, consectetur adipiscing elit. Sed do eiusmod tempor incididunt
    ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco
    laboris nisi ut aliquip ex ea commodo consequat.</p>

    <p>Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat
    nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt in culpa qui officia
    deserunt mollit anim id est laborum.</p>

    <p>Sed ut perspiciatis unde omnis iste natus error sit voluptatem accusantium doloremque
    laudantium, totam rem aperiam, eaque ipsa quae ab illo inventore veritatis et quasi
    architecto beatae vitae dicta sunt explicabo.</p>

    <div style="clear: both;"></div>

    <p>Este párrafo aparece debajo del bloque de imagen y texto, sin verse afectado por el float.</p>
</body>
</html>
```

### Conclusión

Un elemento con `float` sale del flujo normal de la página. Con `clear: both` se limpia el flotado y el contenido posterior se coloca donde corresponde.

---

## 4. Reto: tarjeta de producto

### Requisitos

1. Imagen principal local con ruta relativa.
2. Segunda imagen con URL absoluta, como sello, y un comentario indicando cuál es local y cuál remota.
3. Tamaño de ambas imágenes con `width` y `height`.
4. Borde en la imagen principal con `border` mediante `style`.
5. Nombre del producto (`<h2>`), precio con `<del>` y `<strong>`, y descripción (`<p>`).
6. Textos `alt` descriptivos por si alguna imagen no carga.

### Estructura de carpetas

```text
13_4/
├── index.html
└── img/
    └── zapatillas.jpg
```

### Código `13_4/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Tarjeta de producto</title>
</head>
<body>
    <!--
        Imagen principal: LOCAL (img/zapatillas.jpg).
        Conviene guardarla en el proyecto porque es la foto clave del producto:
        carga más rápido, no depende de otra web y nadie puede borrarla.

        Sello de oferta: REMOTA (URL absoluta).
        Es un elemento secundario que puede cambiar con frecuencia (rebajas, novedades),
        así que se puede actualizar sin tocar el proyecto. El riesgo es que si la otra
        web la borra o cambia la URL, la imagen deja de verse.
    -->
    <h1>Tienda de deporte</h1>

    <img src="img/zapatillas.jpg"
         alt="Zapatillas de running azules con suela blanca y cordones naranjas"
         width="300" height="300"
         style="border: 3px solid #2c3e50;">

    <img src="https://placehold.co/80x80?text=Oferta"
         alt="Sello rojo con la palabra Oferta que indica que el producto está rebajado"
         width="80" height="80">

    <h2>Zapatillas Runner Pro</h2>

    <p>Precio antes: <del>89,99 €</del><br>
    Precio ahora: <strong>59,99 €</strong></p>

    <p>Zapatillas ligeras y transpirables, con suela amortiguada pensada para correr
    largas distancias con comodidad.</p>
</body>
</html>
```

### Conclusión

Las rutas relativas son ideales para los archivos del propio proyecto, y las URL absolutas para recursos alojados en otras webs. Un buen `alt` permite entender qué falta por ver si la imagen no carga. El borde se aplica con `style="border: ..."` porque el atributo `border` de HTML está obsoleto.

---
