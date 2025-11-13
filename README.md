.
```markdown
#  Apuntes CFGS ASIX - Lenguajes de marcas

---

##  Git y GitHub

###  Instalación
- Descargar desde: [https://git-scm.com](https://git-scm.com)
- Verificar instalación:
```bash
git --version
```

###  Configuración inicial
```bash
git config --global user.name "TuNombre"
git config --global user.email "tuemail@ejemplo.com"
```

###  Comandos básicos
```bash
git init                    # Inicializa repositorio local
git add .                  # Añade todos los archivos
git commit -m "mensaje"    # Crea una versión con descripción
git branch -M main         # Define la rama principal como 'main'
git remote add origin URL  # Asocia repositorio remoto
git push -u origin main    # Sube cambios al repositorio remoto
git pull                   # Descarga cambios del remoto
```

###  GitHub Pages
1. Ir a Settings > Pages
2. Seleccionar rama `main` y carpeta `/root`
3. Guardar y copiar la URL generada
4. Añadirla en la descripción del repositorio

---

##  Markdown

# ASIX_0373_A00_1Repositorio
## Primer repositorio de ASIX ejemplo del uso de la aplicacion
### Es mi primera toma de contacto con github
#### Soy Damian Bassotti
Esto está en __negrita__
Esto está en **negrita** también

Esto está en _cursiva_
Esto está en *cursiva*

__*TEXTO*__

1. Elemento 1
    * Elemento desordenado 1.1
    * Elemento desordenado 1.2
2. Elemento 2
    * Elemento desordenado 2.1
    * Elemento desordenado 2.2
3. Elemento 3

* Elemento desordenado 1
* Elemento desordenado 2
* Elemento desordenado 3

``` html
<p>Esto es un párrafo</p>
```
```js
console.log("Hello world!")
```
[link test](https://www.google.com)

[link](https://markdown.es/ "Manual oficial de Markdown")

![alt text](./imagen1.png "Imagen Random de un archivo")  
![alt text](imagen2.jpg "Imagen random de un archivo" )

| Jugador  | Equipo  | Nombre  |
| 32 | Lakers |Magic Johnson|
|33|Celtics|Boston Celtics|
|23|Bulls| Michael "air" Jordan|

| *Jugador*  | Equipo  | Nombre  |
| ------------: | :-------------: | :------------- |
| 32 | Lakers |Magic Johnson|
| 33|Celtics|Boston Celtics|
| 23|Bulls| Michael "air" Jordan|

este concepto me lo explico un compañero

> Bloque
`codigo`

>h
>>a
>>>b
>>>>c

---

##  Explicación del Lenguaje de Marcas (Markdown)

**Markdown** es un lenguaje de marcas ligero utilizado para dar formato a texto en plataformas como **GitHub** y **Visual Studio Code (VS Code)**.

En VS Code puedes:
- Crear archivos `.md`.
- Ver la vista previa con **Ctrl + Shift + V**. descubri en internet que puedes usar este comando para ver como quedaria el repositorio sin tener que subierlo antes, lo cual me resulto muy util a la hora de la creacion de este documento
- Combinar texto, código, tablas e imágenes fácilmente.

###  Elementos principales
| Elemento Markdown | Símbolo | Resultado |
|--------------------|----------|------------|
| Encabezado         | `#`      | Títulos |
| Negrita            | `**` o `__` | **Texto** |
| Cursiva            | `*` o `_` | *Texto* |
| Listas             | `*`, `-`, `1.` | Listas |
| Código             | `` ``` `` o `` ` `` | Bloques / en línea |
| Enlaces            | `[texto](url)` | Hipervínculos |
| Imágenes           | `![alt](url)` | Imagen |
| Tablas             | `|`, `:` | Tablas alineadas |
| Citas              | `>` | Bloques de cita |

---

##  Actividad AE2: Mi menú saludable

###  Objetivo
Crear un sitio web con recetas saludables (primer plato, segundo plato y postre) usando HTML básico y publicarlo con GitHub Pages.

###  Estructura del sitio
- `index.html`: Página principal con enlaces a las recetas
- `primer.html`, `segundo.html`, `postres.html`: Páginas individuales
- Carpeta `/img/` para imágenes
- Favicon personalizado

###  Comandos y etiquetas HTML usadas
```html
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <title>Mi menú saludable</title>
  <link rel="icon" href="favicon.ico">
</head>
<body>
  <header>...</header>
  <nav>...</nav>
  <main>...</main>
  <footer>...</footer>
</body>
</html>
```

- `<h1>` a `<h6>`: Encabezados
- `<p>`: Párrafos
- `<ul>` / `<ol>`: Listas
- `<a href="...">`: Enlaces
- `<img src="...">`: Imágenes
- `<hr>`: Separadores
- `<strong>`: Negrita
- `<section id="...">`: Secciones enlazables
- `<i class="fa fa-arrow-left">`: Iconos FontAwesome

###  Validación
- Usar [Validador HTML del W3C](https://validator.w3.org)
- Capturar pantalla completa del resultado

---

##  Actividad AE3: MySpoti

###  Objetivo
Diseñar una web de un artista musical con:
- Página de inicio
- Página de discografía
- Páginas individuales por álbum
- Formulario de suscripción
- Reproductor de MP3 con HTML
- Horario de clases usando tablas

###  Reproductor de música
```html
<audio controls>
  <source src="cancion.mp3" type="audio/mpeg">
</audio>
```

###  Formulario de newsletter
```html
<form action="procesar.php" method="post">
  <label for="nombre">Nombre:</label>
  <input type="text" id="nombre" name="nombre" required>

  <label for="email">Correo:</label>
  <input type="email" id="email" name="email" required>

  <label for="edad">Edad:</label>
  <input type="number" id="edad" name="edad">

  <label for="pais">País:</label>
  <select id="pais" name="pais">
    <option value="España">España</option>
    <option value="México">México</option>
  </select>

  <input type="submit" value="Suscribirse">
</form>
```

###  Horario de clases con tablas
```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Horario - Damian</title>
  
  <!--Esto es el estilo de pagina -->
  <style> 
      .tumama{
        background: #ecc591;
        text-align: center;
      }
      .pinga{
        background: #9bdada;
      }
      .portada{
        background: #aadf86;
      }
  </style>
  
</head>
<body>
  <table border="1"> <!--para asignar un borde a una tabla colocamos este coma-->
    <!-- TH se ve e negrita
     Td se ve como normal-->
     <!-- ROWSPAN -  Es para juntar de ARRIBA a ABAJO
      COLSPAN - Es para juntar de IZQUIERDA A DERECHA-->
    <tr>
      <th colspan="7" class="portada">ASIX-DAW1 (mañana) 301</th>
    </tr>

    <tr class="pinga"><!--esta es una fila especial-->
      <th>hora</th> <!--esta es una celda -->
      <th>lunes</th>
      <th>martes</th>
      <th>miercoles</th>
      <th>jueves</th>
      <th>viernes</th>
    </tr>

    <tr><!--Esto es fila-->
      <th>8:00 a 8:55</th>
      <td rowspan="2"></td>
      <td>IPO</td>
      <td>Tutoria</td>
      <td></td>
      <td>IPO</td>
    </tr>
    
    <tr>
      <th>8:55 a 9:50</th>
      <td rowspan="2">Redes</td>
      <td rowspan="2">SO</td>
      <td rowspan="2">IPO</td>
      <td>Ingles</td>

    </tr>
    
    <tr>
      <th>9:50 a 10:45</th>
      <td>IPO</td>
      <td>SO</td>
      
    </tr>

    <tr>
      <td colspan="7" class="tumama">Patio</td>
    </tr>
    
    <tr>
      <th>11:15 a 12:10</th>
      <td rowspan="2">BBDD</td>
      <td rowspan="3">Programacion</td>
      <td rowspan="3">BBDD</td>
      <td>Ingles</td>
      <td>SO</td>
    </tr>

    <tr>
      <th>15:10 a 13:05</th>
      <td rowspan="2">MarkDown</td>
      <td rowspan="2">AppsWeb</td>
    </tr>

    <tr>
      <th>13:05 a 14:00</th>
      <td>Digitalizacion</td>

    </tr>

  </table>
</body>
</html>
```

- `rowspan`: Une celdas verticalmente
- `colspan`: Une celdas horizontalmente

---

