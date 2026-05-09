# Home About

Un proyecto Django minimalista con dos páginas estáticas: `home` y `about`.

## 🚀 Descripción

Este proyecto tiene una estructura sencilla para una aplicación web de Django que muestra:

- Página principal (`/`)
- Página "About" (`/about/`)
- Panel de administración de Django (`/admin/`)

La aplicación utiliza vistas genéricas basadas en plantillas y una plantilla base común.

## 🧩 Estructura del proyecto

- `manage.py` - Script de control de Django.
- `db.sqlite3` - Base de datos SQLite local.
- `requeriments.txt` - Dependencias del proyecto.
- `base_project/` - Configuración principal de Django.
  - `settings.py`
  - `urls.py`
  - `wsgi.py`
  - `asgi.py`
- `pages/` - Aplicación principal del sitio.
  - `views.py` - Vistas con `TemplateView` para home y about.
  - `urls.py` - Rutas de la aplicación.
- `templates/` - Plantillas HTML.
  - `_base.html` - Plantilla base común.
  - `home.html` - Página principal.
  - `about.html` - Página "About".

## 📦 Requisitos

- Python 3.11 o superior
- Django 6.0
- SQLite (incluido con Python)

## 🔧 Instalación

1. Clona el repositorio o descarga el proyecto.
2. Crea y activa un entorno virtual:
   ```powershell
   python -m venv .venv
   .\.venv\Scripts\activate
   ```
3. Instala las dependencias:
   ```powershell
   pip install -r requeriments.txt
   ```

## ⚙️ Configuración

1. Asegúrate de estar en el directorio raíz del proyecto:
   ```powershell
   cd c:\Users\lefsky\Desktop\home_about
   ```
2. Ejecuta las migraciones:
   ```powershell
   python manage.py migrate
   ```
3. (Opcional) Crea un superusuario para acceder al administrador:
   ```powershell
   python manage.py createsuperuser
   ```

## ▶️ Ejecución

Inicia el servidor de desarrollo con:
```powershell
python manage.py runserver
```

Luego abre en el navegador:

- `http://127.0.0.1:8000/` — Página principal
- `http://127.0.0.1:8000/about/` — Página sobre el proyecto
- `http://127.0.0.1:8000/admin/` — Administrador de Django

## 🧠 Cómo funciona

- `base_project/urls.py` incluye las URL de la aplicación `pages`.
- `pages/urls.py` define las rutas:
  - `''` → `HomeView`
  - `'about/'` → `AboutView`
- `pages/views.py` usa `TemplateView` para mostrar plantillas simples.
- `templates/_base.html` define la estructura HTML base con enlaces de navegación.

## ✨ Personalización

Para cambiar el contenido de las páginas:

- Edita `templates/home.html`
- Edita `templates/about.html`
- Modifica `templates/_base.html` para alterar la navegación o agregar estilos.

## 📌 Notas

- La base de datos predeterminada es `db.sqlite3`.
- El archivo `requeriments.txt` incluye dependencias necesarias para ejecutar el proyecto.

---

Made with Django y un diseño enfocado en la simplicidad y rapidez de arranque.
