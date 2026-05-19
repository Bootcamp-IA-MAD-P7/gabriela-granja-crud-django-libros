# CRUD con Django

## ¿Qué es Django?

Django es un framework desarrollado en Python que permite crear aplicaciones web de forma rápida, organizada y segura. Django incluye herramientas integradas para trabajar con bases de datos, formularios, paneles de administración y sistemas CRUD.

---

# 1. ¿Qué es un CRUD?

CRUD es el conjunto de las cuatro operaciones básicas que una aplicación realiza sobre los datos:

- Create → Crear
- Read → Leer
- Update → Actualizar
- Delete → Eliminar

Estas operaciones están presentes en prácticamente todas las aplicaciones web modernas.

Por ejemplo, en una aplicación de tareas el usuario puede:

- crear una nueva tarea
- visualizar tareas guardadas
- modificar tareas existentes
- eliminar tareas

El objetivo principal de un CRUD es permitir la gestión completa de información dentro de una aplicación.

---

# 2. Patrones de arquitectura

Los patrones de arquitectura son formas organizadas de estructurar una aplicación para mantener el código limpio, ordenado y fácil de mantener.

## MVC (Modelo – Vista – Controlador)

En este patrón:

- el Modelo gestiona los datos
- la Vista muestra la información al usuario
- el Controlador procesa la lógica

---

## MVT (Modelo – Vista – Template)

Django utiliza una variante llamada MVT.

En este patrón:

- el Modelo gestiona los datos
- la View procesa la lógica
- el Template representa la parte visual mediante HTML

La principal diferencia entre MVC y MVT es que en Django la View cumple funciones similares al Controller de MVC.

---

# 3. Estructura de un proyecto Django

Un proyecto Django se organiza en distintos componentes:

## Models

Representan los datos y la conexión con la base de datos.

## Views

Reciben las peticiones del usuario y procesan la lógica.

## Templates

Son archivos HTML que muestran información visualmente.

## URLs

Conectan rutas web con las Views correspondientes.

---

## Uso de {% %} y {{ }}

En Django:

```django
{% %}
se utiliza para lógica:

bucles
condiciones
estructuras de control

Mientras que:
{{ }}
se utiliza para mostrar datos dinámicos.
4. Flujo entre formulario HTML y base de datos

El flujo en Django funciona así:
Usuario
↓
Formulario HTML
↓
View
↓
Model
↓
Base de datos
↓
Respuesta HTML
5. Herramientas y comandos de Django
startproject

Crea un proyecto Django nuevo.
python -m django startproject sistema_libros .

startapp
Crea una aplicación dentro del proyecto.
python manage.py startapp libros

runserver
Ejecuta el servidor local.
python manage.py runserver

makemigrations
Genera archivos de migración a partir de los Models.
python manage.py makemigrations

migrate
Aplica migraciones a la base de datos.
python manage.py migrate

ModelForm

Permite generar formularios automáticamente usando Models.
El Admin permite:

crear registros
editar registros
eliminar registros
visualizar información

sin necesidad de programar un panel manualmente.
7. REST y Django REST Framework

Django puede trabajar con APIs REST usando Django REST Framework.

REST es una arquitectura que permite comunicar aplicaciones mediante HTTP.

Las operaciones CRUD suelen relacionarse con:

GET → Leer
POST → Crear
PUT/PATCH → Actualizar
DELETE → Eliminar

Django REST Framework facilita la creación de APIs que devuelven información en formato JSON.

Conclusión

Django facilita enormemente el desarrollo de aplicaciones CRUD gracias a:

arquitectura MVT
sistema de Models
panel Admin automático
formularios automáticos
migraciones
Django REST Framework

Estas herramientas permiten desarrollar aplicaciones web organizadas y escalables incluso para desarrolladores junior.


---

# PARTE 2 — README DEL PROYECTO

```md
# CRUD de Libros con Django

## Descripción

Este proyecto consiste en una aplicación CRUD desarrollada con Django para gestionar libros.

La aplicación permite:

- crear libros
- visualizar libros
- editar libros
- eliminar libros

También se utiliza el panel de administración de Django para gestionar registros desde una interfaz visual.

---

# Tecnologías utilizadas

- Python
- Django
- SQLite
- HTML
- MVT (Model - View - Template)

---

# Estructura del proyecto

```text
crud_python/
│
├── libros/
│   ├── migrations/
│   ├── templates/
│   │   └── libros/
│   │       ├── lista_libros.html
│   │       ├── detalle_libro.html
│   │       ├── crear_libro.html
│   │       ├── editar_libro.html
│   │       └── eliminar_libro.html
│   │
│   ├── admin.py
│   ├── apps.py
│   ├── forms.py
│   ├── models.py
│   ├── urls.py
│   └── views.py
│
├── sistema_libros/
│   ├── settings.py
│   ├── urls.py
│   ├── asgi.py
│   └── wsgi.py
│
├── db.sqlite3
├── manage.py
└── README.md

Funcionalidades

La aplicación permite:

Crear libros
Ver lista de libros
Ver detalle de libros
Editar libros
Eliminar libros
Gestionar libros desde Django Admin
Ejecución del proyecto
Crear migraciones
python manage.py makemigrations
Aplicar migraciones
python manage.py migrate
Crear superusuario
python manage.py createsuperuser
Ejecutar servidor
python manage.py runserver
Acceso al proyecto
Admin Django
http://localhost:8000/admin/
Lista de libros
http://localhost:8000/libros/
Detalle de libro
http://localhost:8000/libros/1/
Base de datos

El proyecto utiliza SQLite como base de datos por defecto.

Archivo generado:

db.sqlite3
Conclusión

Este proyecto permitió comprender el flujo completo de desarrollo CRUD en Django utilizando:

Models
Views
Templates
URLs
Forms
Admin
Migraciones
Base de datos SQLite

Además, permitió comprender el patrón MVT y el flujo entre frontend y backend dentro de Django.