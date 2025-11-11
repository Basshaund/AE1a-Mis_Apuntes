# Apuntes de Git, GitHub, Markdown y HTML básico

## 1. Creación de una cuenta de GitHub
Para crear una cuenta hay que entrar a [https://github.com](https://github.com)  
Ahí se hace clic en **Sign Up** y se completa con usuario, correo y contraseña.  
Después GitHub manda un correo para confirmar la cuenta.  
Se puede usar la versión gratuita (Free).  
Cuando ya está creada se puede agregar una foto y una descripción en el perfil.

La tarea era mandar la URL de la cuenta, por ejemplo:https://github.com/Basshaund

---

## 2. Instalación de GIT en local
Primero hay que ir a la página oficial: [https://git-scm.com/](https://git-scm.com/)  
Se descarga la versión para el sistema operativo que uno tenga (Windows, Mac o Linux).  
En la instalación se puede dejar todo por defecto.  

Para comprobar si se instaló bien: git --version

Si aparece algo como `git version 2.x.x` entonces está instalado.

Configuración inicial (solo se hace una vez):
git config --global user.name "Basshaund"
git config --global user.email "441330.joan23@fje.edu"


---

## 3. Instalación de Visual Studio Code
Descargar desde [https://code.visualstudio.com/](https://code.visualstudio.com/)  
Instalar normalmente.  
Visual Studio Code sirve como editor de código, se pueden abrir carpetas, proyectos, usar terminal, etc.  
Conviene instalar las extensiones de GitHub y Markdown.  
La terminal se abre con `Ctrl + ñ`.

---

## 4. Qué es GitHub y cómo se trabaja con control de versiones
Git es un sistema de control de versiones, o sea, guarda los cambios que se hacen en los archivos del proyecto.  
GitHub es una plataforma online que usa Git y permite guardar los proyectos en la nube y trabajar en equipo.  

Sirve para:
- Llevar registro de los cambios del código.
- Trabajar con ramas (branches).
- Colaborar con otros programadores.
- Subir proyectos públicos o privados.

Flujo básico:
1. Crear o clonar un repositorio.
2. Hacer cambios en los archivos.
3. Guardar esos cambios (commit).
4. Subirlos a GitHub (push).

---

## 5. Formas de crear un repositorio nuevo

### a) Clonado y trabajo en local (repositorio ya existente en GitHub)
Primero se crea el repo en GitHub y se copia la URL HTTPS.  
En la terminal:

git clone https://github.com/usuario/repositorio.git
cd repositorio

cd repositorio

Después se puede trabajar con los archivos normalmente.

### b) Crear un repositorio local nuevo desde la terminal (CLI)
Se crea una carpeta:

mkdir mi-proyecto
cd mi-proyecto


Se inicializa git:

git init


Se agregan archivos y se hace el primer commit:

git add .
git commit -m "primer commit"


### c) Sincronizar un repositorio local con GitHub
En GitHub se crea un nuevo repositorio vacío.  
Después se conecta con el que tenemos en local:

git remote add origin https://github.com/Basshaund/nuevo-repo.git


git branch -M main
git push -u origin main


Esto enlaza el proyecto local con el remoto.

### d) Importar un repositorio existente (Clone)
Si el proyecto ya existe en GitHub, se clona con:

git clone https://github.com/usuario/repo-existente.git

Eso crea una copia completa con todo el historial.

---

## 6. Activación de GitHub Pages
GitHub Pages sirve para publicar páginas estáticas (HTML, CSS, JS).  
Para activarlo hay que ir al repositorio en GitHub, después a **Settings → Pages**.  
En **Source** se elige la rama `main` y la carpeta raíz (root).  
Se guarda y GitHub genera un enlace tipo:

https://usuario.github.io/nombre-del-repo/


Es importante que exista un archivo llamado `index.html` porque es el que se muestra como página principal.

---

## 7. Introducción al lenguaje de marcas Markdown
Markdown es un lenguaje de marcado ligero.  
Se usa para escribir archivos `README.md` y documentación.  
Permite dar formato sin usar HTML.

### Sintaxis básica

**Encabezados:**

Título 1
Título 2
Título 3


**Negrita y cursiva:**

texto en negrita
texto en cursiva


**Listas:**

    elemento uno

    elemento dos

        subelemento


**Listas numeradas:**

    paso uno

    paso dos


**Enlaces:**

Texto del enlace


**Imágenes:**


**Código:**

git status


**Citas:**

    Esto es una cita


---

## 8. HTML básico
HTML (HyperText Markup Language) se usa para crear la estructura de páginas web. Permite organizar títulos, párrafos, listas, enlaces, imágenes y tablas.

---

## 1. Estructura mínima de un documento HTML

<!DOCTYPE html> <html> <head> <title>Título de la página</title> </head> <body> <!-- Contenido visible --> </body> </html> ```
2. Títulos y párrafos

<h1>Título principal</h1>
<h2>Subtítulo</h2>
<h3>Encabezado menor</h3>

<p>Este es un párrafo.</p>

3. Enlaces e imágenes

<br>

<img src="doge.jpg" alt="Descripción de la imagen">

4. Negrita y cursiva

<strong>Texto en negrita</strong>
<em>Texto en cursiva</em>

5. Saltos y separación

<br>  <!-- Salto de línea -->
<hr>  <!-- Línea horizontal -->

6. Listas
Lista desordenada

<ul>
  <li>Elemento 1</li>
  <li>Elemento 2</li>
</ul>

Lista ordenada

<ol>
  <li>Primer elemento</li>
  <li>Segundo elemento</li>
</ol>

7. Tablas

<table>
  <tr>
    <th>Encabezado 1</th>
    <th>Encabezado 2</th>
  </tr>
  <tr>
    <td>Dato 1</td>
    <td>Dato 2</td>
  </tr>
  <tr>
    <td>Dato 3</td>
    <td>Dato 4</td>
  </tr>
</table>

8. Comentarios

<!-- Esto es un comentario -->

9. Ejemplo completo de HTML básico

<!DOCTYPE html>
<html>
  <head>
    <title>Mi primera página HTML</title>
  </head>
  <body>
    <h1>Bienvenidos</h1>
    <p>Este es un párrafo con <strong>negrita</strong> y <em>cursiva</em>.</p>

    <h2>Lista de tareas</h2>
    <ul>
      <li>Aprender HTML</li>
      <li>Practicar CSS</li>
      <li>Hacer un proyecto</li>
    </ul>

    <h2>Tabla de ejemplo</h2>
    <table>
      <tr>
        <th>Nombre</th>
        <th>Edad</th>
      </tr>
      <tr>
        <td>Ana</td>
        <td>25</td>
      </tr>
      <tr>
        <td>Juan</td>
        <td>30</td>
      </tr>
    </table>

    <p>Visita <a href="https://www.ejemplo.com">este sitio</a>.</p>

    <img src="imagen.jpg" alt="Imagen de ejemplo">
  </body>
</html>
    


<strong>: sirve para resaltar texto (en negrita).

    <p>Esto es <strong>importante</strong>.</p>

    <br>: salto de línea.

    <hr>: línea horizontal para separar contenido.

9. Creación de tablas en HTML

Las tablas se usan para mostrar datos organizados en filas y columnas.

Estructura básica:

<table>
  <tr>
    <th>Encabezado 1</th>
    <th>Encabezado 2</th>
  </tr>
  <tr>
    <td>Dato 1</td>
    <td>Dato 2</td>
  </tr>
  <tr>
    <td>Dato 3</td>
    <td>Dato 4</td>
  </tr>
</table>

Explicación:

    <table> abre y cierra la tabla.

    <tr> crea una fila.

    <th> es una celda de encabezado (título de columna).

    <td> es una celda de datos normal.


