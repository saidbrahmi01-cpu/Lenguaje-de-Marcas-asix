# UD1.5 - Tablas

**Actividad:** UD1.5  
**Curso:** 1CFGS - Lenguaje de marcas y sistemas de gestión de la información  
**Fecha:** 2026

---

## 1. Horario semanal

### Requisitos

1. La primera fila con `<th>` de Lunes a Viernes.
2. La primera columna de cada fila siguiente con un `<th>` con el tramo horario.
3. El resto de celdas con `<td>` y el nombre del módulo.
4. Un `<caption>` con el título "Horario semanal".
5. Sin estilos CSS.

### Estructura de carpetas

```text
ud15_1/
└── index.html
```

### Código `ud15_1/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Horario semanal</title>
</head>
<body>
    <table>
        <caption>Horario semanal</caption>
        <tr>
            <th></th>
            <th>Lunes</th>
            <th>Martes</th>
            <th>Miércoles</th>
            <th>Jueves</th>
            <th>Viernes</th>
        </tr>
        <tr>
            <th>8:00 - 9:00</th>
            <td>Lenguajes de marcas</td>
            <td>Programación</td>
            <td>Sistemas informáticos</td>
            <td>Programación</td>
            <td>Lenguajes de marcas</td>
        </tr>
        <tr>
            <th>9:00 - 10:00</th>
            <td>Lenguajes de marcas</td>
            <td>Programación</td>
            <td>Sistemas informáticos</td>
            <td>Bases de datos</td>
            <td>Entornos de desarrollo</td>
        </tr>
        <tr>
            <th>10:00 - 11:00</th>
            <td>Bases de datos</td>
            <td>Entornos de desarrollo</td>
            <td>Programación</td>
            <td>Bases de datos</td>
            <td>Sistemas informáticos</td>
        </tr>
        <tr>
            <th>11:30 - 12:30</th>
            <td>Sistemas informáticos</td>
            <td>Bases de datos</td>
            <td>Entornos de desarrollo</td>
            <td>Lenguajes de marcas</td>
            <td>Programación</td>
        </tr>
    </table>
</body>
</html>
```

### Conclusión

Una tabla se construye con `<table>`, filas `<tr>`, celdas de encabezado `<th>` y celdas de datos `<td>`. El `<caption>` es el título de la tabla. Sin CSS, el navegador la muestra con su estilo por defecto, sin bordes.

---

## 2. Dando estilo a la tabla

### Requisitos

1. Borde en `table`, `th` y `td` con `border`.
2. `border-collapse: collapse` en la tabla.
3. Color de fondo distinto en `<th>` y `<td>` con `background-color`.
4. Texto centrado en todas las celdas con `text-align: center`.

### Estructura de carpetas

```text
ud15_2/
└── index.html
```

### Código `ud15_2/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Horario semanal con estilos</title>
</head>
<body>
    <table style="border: 1px solid black; border-collapse: collapse;">
        <caption>Horario semanal</caption>
        <tr>
            <th style="border: 1px solid black; background-color: #2c3e50; color: white; text-align: center;"></th>
            <th style="border: 1px solid black; background-color: #2c3e50; color: white; text-align: center;">Lunes</th>
            <th style="border: 1px solid black; background-color: #2c3e50; color: white; text-align: center;">Martes</th>
            <th style="border: 1px solid black; background-color: #2c3e50; color: white; text-align: center;">Miércoles</th>
            <th style="border: 1px solid black; background-color: #2c3e50; color: white; text-align: center;">Jueves</th>
            <th style="border: 1px solid black; background-color: #2c3e50; color: white; text-align: center;">Viernes</th>
        </tr>
        <tr>
            <th style="border: 1px solid black; background-color: #2c3e50; color: white; text-align: center;">8:00 - 9:00</th>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Lenguajes de marcas</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Programación</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Sistemas informáticos</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Programación</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Lenguajes de marcas</td>
        </tr>
        <tr>
            <th style="border: 1px solid black; background-color: #2c3e50; color: white; text-align: center;">9:00 - 10:00</th>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Lenguajes de marcas</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Programación</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Sistemas informáticos</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Bases de datos</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Entornos de desarrollo</td>
        </tr>
        <tr>
            <th style="border: 1px solid black; background-color: #2c3e50; color: white; text-align: center;">10:00 - 11:00</th>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Bases de datos</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Entornos de desarrollo</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Programación</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Bases de datos</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Sistemas informáticos</td>
        </tr>
        <tr>
            <th style="border: 1px solid black; background-color: #2c3e50; color: white; text-align: center;">11:30 - 12:30</th>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Sistemas informáticos</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Bases de datos</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Entornos de desarrollo</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Lenguajes de marcas</td>
            <td style="border: 1px solid black; background-color: #eaf2f8; text-align: center;">Programación</td>
        </tr>
    </table>
</body>
</html>
```

### Conclusión

Sin `border-collapse: collapse`, cada celda dibuja su propio borde y se ven dobles. Con esta propiedad los bordes se fusionan en uno solo. El borde se aplica con `style` y no con el atributo HTML `border`, que está obsoleto.

---

## 3. Lista de precios con celdas combinadas

### Requisitos

1. Al menos 4 filas de datos y 3 columnas.
2. Al menos una celda con `colspan`.
3. Al menos una celda con `rowspan`.
4. `border-collapse: collapse` y colores de fondo alternos.

### Estructura de carpetas

```text
ud15_3/
└── index.html
```

### Código `ud15_3/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Carta de la cafetería</title>
</head>
<body>
    <h1>Carta de la cafetería</h1>

    <table style="border: 1px solid black; border-collapse: collapse;">
        <tr style="background-color: #2c3e50; color: white;">
            <th style="border: 1px solid black;">Producto</th>
            <th style="border: 1px solid black;">Tamaño</th>
            <th style="border: 1px solid black;">Precio</th>
        </tr>

        <!-- Título de sección: una celda que ocupa las 3 columnas (colspan) -->
        <tr style="background-color: #aed6f1;">
            <th colspan="3" style="border: 1px solid black;">Desayunos</th>
        </tr>

        <!-- Café: el nombre aparece una sola vez y ocupa 2 filas (rowspan) -->
        <tr style="background-color: #ffffff;">
            <td rowspan="2" style="border: 1px solid black;">Café</td>
            <td style="border: 1px solid black;">Pequeño</td>
            <td style="border: 1px solid black;">1,20 €</td>
        </tr>
        <tr style="background-color: #ffffff;">
            <td style="border: 1px solid black;">Grande</td>
            <td style="border: 1px solid black;">1,80 €</td>
        </tr>

        <tr style="background-color: #eaf2f8;">
            <td style="border: 1px solid black;">Tostada con tomate</td>
            <td style="border: 1px solid black;">Única</td>
            <td style="border: 1px solid black;">2,00 €</td>
        </tr>

        <tr style="background-color: #aed6f1;">
            <th colspan="3" style="border: 1px solid black;">Bebidas</th>
        </tr>

        <tr style="background-color: #ffffff;">
            <td rowspan="2" style="border: 1px solid black;">Zumo de naranja</td>
            <td style="border: 1px solid black;">Pequeño</td>
            <td style="border: 1px solid black;">2,00 €</td>
        </tr>
        <tr style="background-color: #ffffff;">
            <td style="border: 1px solid black;">Grande</td>
            <td style="border: 1px solid black;">3,00 €</td>
        </tr>

        <tr style="background-color: #eaf2f8;">
            <td style="border: 1px solid black;">Refresco</td>
            <td style="border: 1px solid black;">Lata</td>
            <td style="border: 1px solid black;">1,50 €</td>
        </tr>
    </table>
</body>
</html>
```

### Conclusión

`colspan` combina varias columnas y `rowspan` varias filas. Al usarlos hay que contar bien las celdas: por ejemplo, en la fila de "Grande" solo hay 2 `<td>`, porque la primera columna la ocupa la celda con `rowspan` de la fila anterior. Los colores alternos se aplican por grupos de productos para que las celdas combinadas mantengan el mismo fondo.

---

## 4. Reto: tabla de datos completa

### Requisitos

1. `<thead>`, `<tbody>` con al menos 5 filas y `<tfoot>` con totales.
2. `<caption>` en la parte inferior con `caption-side`.
3. `border-spacing` en lugar de `border-collapse`.
4. `vertical-align` en alguna celda combinada con `rowspan`.
5. `empty-cells` con una celda vacía y un comentario explicativo.

### Estructura de carpetas

```text
ud15_4/
└── index.html
```

### Código `ud15_4/index.html`

```html
<!DOCTYPE html>
<html lang="es">
<head>
    <meta charset="UTF-8">
    <title>Inventario de productos</title>
</head>
<body>
    <h1>Inventario de la tienda</h1>

    <!--
        empty-cells: hide
        La webcam no tiene precio, así que su celda se deja vacía a propósito.
        - Con empty-cells: show (valor por defecto) la celda vacía se dibuja con su
          fondo y su borde, y se nota que falta un dato.
        - Con empty-cells: hide la celda vacía no se dibuja: desaparecen su fondo y
          su borde y queda un hueco en la tabla.
        Esta propiedad solo funciona con border-collapse: separate (el valor por
        defecto), por eso la tabla usa border-spacing y no border-collapse.
    -->
    <table style="border-spacing: 8px; empty-cells: hide; background-color: #f4f6f7;">
        <caption style="caption-side: bottom;">Tabla 1. Inventario de productos</caption>

        <thead>
            <tr style="background-color: #2c3e50; color: white;">
                <th>Producto</th>
                <th>Categoría</th>
                <th>Unidades</th>
                <th>Precio unitario</th>
            </tr>
        </thead>

        <tbody>
            <tr style="background-color: #eaf2f8;">
                <td>Teclado</td>
                <td rowspan="2" style="vertical-align: middle;">Periféricos</td>
                <td>10</td>
                <td>25,00 €</td>
            </tr>
            <tr style="background-color: #eaf2f8;">
                <td>Ratón</td>
                <td>15</td>
                <td>12,50 €</td>
            </tr>
            <tr style="background-color: #eaf2f8;">
                <td>Monitor</td>
                <td>Pantallas</td>
                <td>5</td>
                <td>150,00 €</td>
            </tr>
            <tr style="background-color: #eaf2f8;">
                <td>Webcam</td>
                <td>Accesorios</td>
                <td>8</td>
                <td></td>
            </tr>
            <tr style="background-color: #eaf2f8;">
                <td>Alfombrilla</td>
                <td>Accesorios</td>
                <td>20</td>
                <td>5,00 €</td>
            </tr>
        </tbody>

        <tfoot>
            <tr style="background-color: #aed6f1; font-weight: bold;">
                <td colspan="2">Total de unidades</td>
                <td>58</td>
                <td></td>
            </tr>
        </tfoot>
    </table>
</body>
</html>
```

### Conclusión

`<thead>`, `<tbody>` y `<tfoot>` dividen la tabla en cabecera, cuerpo y pie. `caption-side: bottom` coloca el título debajo de la tabla. `border-spacing` separa las celdas y `empty-cells` decide si las celdas vacías se pintan o se ocultan. `vertical-align` alinea el contenido de una celda dentro de su altura, algo muy visible cuando la celda ocupa varias filas con `rowspan`.

---
