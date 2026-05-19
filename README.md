# CRUD de Libros con Django

## Descripción

Este proyecto consiste en una aplicación CRUD desarrollada con Django para la gestión de libros. El sistema permite crear, visualizar, editar y eliminar libros utilizando el patrón de arquitectura MVT (Model - View - Template).

Además, se utiliza el panel de administración de Django para gestionar los registros desde una interfaz visual.

---

# ¿Qué es un CRUD?

CRUD es un conjunto de operaciones básicas utilizadas en aplicaciones web para manipular datos.

Las siglas significan:

- Create → Crear
- Read → Leer
- Update → Actualizar
- Delete → Eliminar

En este proyecto, el CRUD se aplica sobre libros almacenados en una base de datos SQLite.

---

# Tecnologías utilizadas

- Python
- Django
- SQLite
- HTML
- MVT (Model - View - Template)

---

# Patrón MVT en Django

Django utiliza el patrón MVT:

## Model

Gestiona los datos y la conexión con la base de datos.

Ejemplo:

```python
class Libro(models.Model):
View

Procesa la lógica y conecta los datos con los templates.

Ejemplo:

def lista_libros(request):
Template

Muestra la interfaz HTML al usuario.

Ejemplo:

lista_libros.html
Estructura del proyecto
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

El proyecto permite:

Crear libros
Ver lista de libros
Ver detalle de un libro
Editar libros
Eliminar libros
Gestionar libros desde Django Admin
Comandos utilizados en Django
Crear proyecto
python -m django startproject sistema_libros .
Crear app
python manage.py startapp libros
Crear migraciones
python manage.py makemigrations

Este comando detecta cambios en los modelos y genera archivos de migración.

Aplicar migraciones
python manage.py migrate

Aplica las migraciones a la base de datos SQLite.

Ejecutar servidor
python manage.py runserver

Inicia el servidor local de Django.

Crear superusuario
python manage.py createsuperuser

Permite acceder al panel administrativo.

Uso del Admin de Django

Django incluye un panel de administración automático.

Acceso:

http://localhost:8000/admin/

Desde el admin se pueden:

crear libros
editar libros
eliminar libros
visualizar registros
URLs principales
Panel Admin
http://localhost:8000/admin/
Lista de libros
http://localhost:8000/libros/
Detalle de libro
http://localhost:8000/libros/1/
Flujo de datos en Django

El flujo básico funciona así:

Usuario
↓
Formulario HTML
↓
View
↓
Model
↓
Base de datos SQLite
↓
Template HTML
↓
Respuesta al usuario
Formularios en Django

El proyecto utiliza ModelForm para generar formularios automáticamente a partir del modelo Libro.

Archivo:

forms.py
Base de datos

Se utiliza SQLite como base de datos por defecto de Django.

Archivo generado:

db.sqlite3
Conclusión

Este proyecto permitió comprender el funcionamiento básico de Django y el desarrollo de aplicaciones CRUD utilizando:

modelos
vistas
templates
formularios
URLs
migraciones
panel administrativo

Además, se aprendió el flujo completo entre frontend, backend y base de datos usando el patrón MVT.