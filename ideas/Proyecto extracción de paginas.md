

Fase 1: Fundamentos de Python

Antes del proyecto, repasarás:

Variables y tipos de datos.

Condicionales (if, elif, else).

Bucles (for, while).

Funciones.

Listas, diccionarios y conjuntos (set).

Manejo de archivos.

Módulos y librerías.

Manejo de errores (try y except).

Clases y objetos.


Objetivo: sentirte cómodo leyendo y escribiendo Python.


---

Fase 2: Primera prueba con páginas web

Aquí todavía no construiremos el crawler.

Aprenderás a:

Instalar librerías:

``` python
pip install requests beautifulsoup4
```


Descargar una página.

Obtener el HTML.

Encontrar títulos, párrafos y enlaces.

Guardar el texto en un archivo.


Objetivo: entender cómo "ve" Python una página web.


---

Fase 3: Extraer enlaces internos

El programa deberá:

Encontrar todos los enlaces (<a>).

Diferenciar enlaces internos y externos.

Ignorar enlaces repetidos.

Crear una lista de páginas pendientes.


Objetivo: empezar a recorrer la documentación.


---

Fase 4: Construir el crawler

Implementaremos reglas:

Permanecer en el mismo dominio.

No visitar la misma página dos veces.

Limitar la profundidad.

Ignorar archivos peligrosos (.exe, .zip, .apk, etc.).

Registrar errores.


Objetivo: recorrer automáticamente un sitio completo.


---

Fase 5: Organizar el contenido

El programa convertirá:

https://docs.python.org/es/3/tutorial/introduction.html

en:

output/
└── tutorial/
    └── introduction.md

También:

Creará carpetas automáticamente.

Guardará imágenes opcionales.

Generará un índice.


Objetivo: obtener una copia organizada de la documentación.


---

Fase 6: Integración con IA

Más adelante podrás:

Unir todos los archivos.

Enviarlos a NotebookLM.

Buscar temas concretos.

Generar resúmenes.

Crear tu propia base de conocimiento.



---

Tecnologías que usaremos

Herramienta	Para qué sirve

Python	Lenguaje principal
requests	Descargar páginas
BeautifulSoup	Analizar HTML
pathlib	Crear carpetas y archivos
markdownify	Convertir HTML a Markdown
playwright	Páginas con JavaScript
json	Guardar metadatos
