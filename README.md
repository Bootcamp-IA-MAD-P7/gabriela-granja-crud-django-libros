# 📚 CRUD de Libros con Django

## 📝 Descripción

Proyecto CRUD desarrollado con Django para gestionar libros utilizando el patrón MVT (Model - View - Template).

La aplicación permite crear, visualizar, editar y eliminar libros utilizando formularios, vistas, templates y una base de datos SQLite.

Además, se utiliza el panel de administración de Django para gestionar registros desde una interfaz visual.

---

# 🔄 ¿Qué es un CRUD?

CRUD es el conjunto de operaciones básicas utilizadas para manipular datos dentro de una aplicación web.

Las siglas significan:

- Create → Crear
- Read → Leer
- Update → Actualizar
- Delete → Eliminar

En este proyecto, el CRUD se aplica sobre libros almacenados en una base de datos.

---

# 🧠 ¿Qué es Django?

Django es un framework desarrollado en Python que permite crear aplicaciones web de forma rápida, organizada y segura.

Django incluye herramientas integradas para:

- bases de datos
- formularios
- autenticación
- panel administrativo
- migraciones
- arquitectura MVT

---

# ⚙️ Patrón MVT en Django

Django utiliza el patrón MVT:

## Model

Gestiona los datos y la conexión con la base de datos.

---

## View

Procesa la lógica de la aplicación y responde a las peticiones del usuario.

---

## Template

Representa la interfaz visual utilizando HTML.

---

# 🔁 Flujo de datos en Django

El flujo básico funciona así:

```text
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
Respuesta HTML
```

---

# 🚀 Tecnologías utilizadas

- Python
- Django
- SQLite
- HTML
- MVT (Model - View - Template)

---

# ✅ Funcionalidades

La aplicación permite:

- Crear libros
- Ver lista de libros
- Ver detalle de libros
- Editar libros
- Eliminar libros
- Gestionar libros desde Django Admin

---

# 🗂️ Estructura del proyecto

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
```

---

# 🛠️ Herramientas y comandos de Django

## Crear proyecto

```bash
python -m django startproject sistema_libros .
```

Crea un nuevo proyecto Django.

---

## Crear aplicación

```bash
python manage.py startapp libros
```

Crea una nueva app dentro del proyecto.

---

## Ejecutar servidor

```bash
python manage.py runserver
```

Inicia el servidor local.

---

## Crear migraciones

```bash
python manage.py makemigrations
```

Genera archivos de migración a partir de los Models.

---

## Aplicar migraciones

```bash
python manage.py migrate
```

Aplica las migraciones a la base de datos SQLite.

---

## Crear superusuario

```bash
python manage.py createsuperuser
```

Permite acceder al panel administrativo.

---

# 👩‍💻 Uso del Admin de Django

Django incluye un panel de administración automático.

Acceso:

```text
http://localhost:8000/admin/
```

Desde el admin se pueden:

- crear libros
- editar libros
- eliminar libros
- visualizar registros

---

# 🔗 URLs principales

## Admin Django

```text
http://localhost:8000/admin/
```

---

## Lista de libros

```text
http://localhost:8000/libros/
```

---

## Detalle de libro

```text
http://localhost:8000/libros/1/
```

---

# 💾 Base de datos

El proyecto utiliza SQLite como base de datos por defecto.

Archivo generado:

```text
db.sqlite3
```

---

# 📌 Conclusión

Este proyecto permitió practicar el desarrollo de aplicaciones CRUD utilizando Django y comprender:

- arquitectura MVT
- Models
- Views
- Templates
- URLs
- Formularios
- Migraciones
- Django Admin
- Flujo entre frontend y backend

Además, permitió comprender cómo Django facilita el desarrollo web mediante herramientas integradas y una estructura organizada.