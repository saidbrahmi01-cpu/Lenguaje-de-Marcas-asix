# UD0_ACT1 - Lenguaje de marcas

**Actividad:** UD0_ACT1  
**Curso:** 1CFGS - Lenguaje de marcas y sistemas de gestión de la información  
**Fecha:** 2026

---

## 1. Observación de `textos.txt` y `textos.html`

### Contenido de `textos.txt`

```text
<h1>Texto grande</h1>
<h3>Texto pequeño</h3>
```

Al abrir `textos.txt` con un navegador, el contenido se muestra como texto porque el archivo tiene extensión `.txt`.

### Contenido de `textos.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Textos</title>
</head>
<body>
    <h1>Texto grande</h1>
    <h3>Texto pequeño</h3>
</body>
</html>
```

Al cambiar la extensión a `.html` y abrir el archivo en el navegador, el navegador interpreta las etiquetas HTML y muestra:

- `<h1>` como un título grande.
- `<h3>` como un título más pequeño.

### Conclusión

La extensión del archivo indica al programa cómo interpretar su contenido. En un archivo `.txt`, las etiquetas se consideran texto normal. En un archivo `.html`, las etiquetas HTML se interpretan y permiten dar estructura y significado al documento.

---

## 2. Estructura SGML de módulos de DAM

### Vocabulario

- `dam`
- `modulo`
- `titulo`
- `contenido`
- `unidad`

### Reglas

1. `dam` contiene varios `modulo`.
2. Cada `modulo` tiene un `titulo` y un `contenido`.
3. `contenido` contiene varias `unidad`.
4. Todas las `unidad` están dentro de un `contenido`.
5. Las `unidad` son texto simple.
6. Detrás de una `unidad` solo puede ir otra `unidad` o el fin de `contenido`.
7. Detrás de un `modulo` solo puede ir otro `modulo` o el fin de `dam`.

### Código `DAM.sgml`

```sgml
<dam>

    <modulo>
        <titulo>Lenguaje de Marcas</titulo>
        <contenido>
            <unidad>Introduccion a los lenguajes de marcas</unidad>
            <unidad>HTML</unidad>
            <unidad>CSS</unidad>
        </contenido>
    </modulo>

    <modulo>
        <titulo>Programacion</titulo>
        <contenido>
            <unidad>Fundamentos de programacion</unidad>
            <unidad>Algoritmos</unidad>
            <unidad>Programacion orientada a objetos</unidad>
        </contenido>
    </modulo>

    <modulo>
        <titulo>Sistemas Informaticos</titulo>
        <contenido>
            <unidad>Hardware</unidad>
            <unidad>Sistemas operativos</unidad>
            <unidad>Administracion de sistemas</unidad>
        </contenido>
    </modulo>

</dam>
```

---

## 3. Documento SGML: Países del mundo

### Vocabulario

- `paises`
- `pais`
- `nombre`
- `capital`
- `continente`
- `idioma`
- `poblacion`

### Reglas

1. `paises` contiene uno o varios `pais`.
2. Cada `pais` contiene `nombre`, `capital`, `continente` e `idioma`.
3. `poblacion` es opcional.
4. Los elementos de cada `pais` aparecen en el orden establecido.

### Código `paises.sgml`

```sgml
<paises>

    <pais>
        <nombre>España</nombre>
        <capital>Madrid</capital>
        <continente>Europa</continente>
        <idioma>Español</idioma>
        <poblacion>aproximadamente 49 millones</poblacion>
    </pais>

    <pais>
        <nombre>Francia</nombre>
        <capital>Paris</capital>
        <continente>Europa</continente>
        <idioma>Francés</idioma>
        <poblacion>aproximadamente 69 millones</poblacion>
    </pais>

    <pais>
        <nombre>Marruecos</nombre>
        <capital>Rabat</capital>
        <continente>África</continente>
        <idioma>Árabe y amazigh</idioma>
        <poblacion>aproximadamente 37 millones</poblacion>
    </pais>

    <pais>
        <nombre>Japón</nombre>
        <capital>Tokio</capital>
        <continente>Asia</continente>
        <idioma>Japonés</idioma>
        <poblacion>aproximadamente 123 millones</poblacion>
    </pais>

    <pais>
        <nombre>Brasil</nombre>
        <capital>Brasilia</capital>
        <continente>América del Sur</continente>
        <idioma>Portugués</idioma>
        <poblacion>aproximadamente 213 millones</poblacion>
    </pais>

</paises>
```

---

## 4. Información de libros estructurada con Markdown

### Vocabulario

- **Título**
- **Formato**
- **ISBN**
- **Autor**
- **Páginas**
- **Editorial**
- **Año**
- **Idioma**
- **Descripción**

### Reglas

1. Cada libro tiene un título.
2. El formato puede ser en papel o ebook.
3. Cada libro tiene un ISBN.
4. Cada libro tiene un autor.
5. El número de páginas se indica cuando está disponible.
6. Cada libro tiene una editorial.
7. El año se indica cuando aparece en la información disponible.
8. El idioma se indica cuando está disponible.
9. La descripción se añade cuando está disponible.

### 📚 FALCO

- **Formato:** En papel
- **ISBN:** 9788420419688
- **Autor:** Arturo Pérez-Reverte
- **Páginas:** 296 págs.
- **Editorial:** Alfaguara
- **Idioma:** Castellà

### 📱 TODO ALATRISTE

- **Formato:** Ebook
- **ISBN:** 9788420425528
- **Autor:** Arturo Pérez-Reverte
- **Editorial:** Alfaguara
- **Idioma:** Castellà

### 📖 HOMBRES BUENOS

- **Formato:** En papel
- **ISBN:** 9788466329804
- **Autor:** Arturo Pérez-Reverte
- **Editorial:** Punto de Lectura
- **Año:** 2024
- **Descripción:** La heróica aventura de quienes se atrevieron a cambiar el mundo con libros. En tiempos de oscuridad siempre hubo hombres buenos que lucharon para llevar las luces y el progreso. Y otros que procuraron impedirlo.
```

---

