# Task List

Proyecto Django sencillo para gestionar y visualizar tareas.

## 📌 Descripción

Esta aplicación es una lista de tareas mínima desarrollada con Django 6.0.5. Permite:

- Ver la lista de tareas actuales.
- Consultar el detalle de una tarea individual.
- Usar SQLite como base de datos local.

## 🚀 Características principales

- Modelo `Task` con campos:
  - `title`: título de la tarea
  - `description`: descripción
  - `completed`: estado de completado
  - `created_at`: fecha de creación
  - `updated_at`: fecha de última actualización
- Vista de lista de tareas (`TaskListView`).
- Vista de detalle de tarea (`TaskDetailView`).
- Plantillas basadas en `base.html`.
- Estilos estáticos ubicados en `static/css/style.css`.

## 📁 Estructura del proyecto

- `manage.py` - comando principal de Django.
- `base_project/` - configuración del proyecto.
  - `settings.py` - ajustes generales.
  - `urls.py` - rutas principales.
  - `wsgi.py` / `asgi.py`.
- `tasks/` - aplicación principal.
  - `models.py` - definición de la entidad `Task`.
  - `views.py` - vistas de lista y detalle.
  - `urls.py` - rutas de la app.
- `templates/` - plantillas HTML.
- `static/css/` - estilos CSS.
- `db.sqlite3` - base de datos local SQLite.
- `requirements.txt` - dependencias del proyecto.

## ⚙️ Instalación y ejecución

1. Clona o copia el proyecto en tu equipo.
2. En Windows, activa el entorno virtual si ya existe:

```powershell
.\.venv\Scripts\Activate.ps1
```

3. Instala dependencias:

```powershell
pip install -r requirements.txt
```

4. Aplica migraciones:

```powershell
python manage.py migrate
```

5. Inicia el servidor de desarrollo:

```powershell
python manage.py runserver
```

6. Abre el navegador en:

```text
http://127.0.0.1:8000/
```

## 🌐 Rutas disponibles

- `/` → lista de tareas
- `/tareas/<id>/` → detalle de una tarea concreta
- `/admin/` → panel de administración de Django

## 📝 Notas importantes

- El proyecto usa `DEBUG = True`, por lo que no está preparado para producción.
- La base de datos por defecto es `db.sqlite3`.
- En caso de cambios de modelo, ejecuta de nuevo:

```powershell
python manage.py makemigrations
python manage.py migrate
```

## 🛠️ Personalización

- Para agregar nuevas tareas, usa el admin o crea fixtures.
- Para mostrar el estado `completed`, modifica las plantillas y views.
- Si deseas usar otro motor de base de datos, actualiza `DATABASES` en `base_project/settings.py`.

## 📚 Recursos

- Documentación Django: https://docs.djangoproject.com/en/6.0/
- Guía rápida de plantillas Django: https://docs.djangoproject.com/en/6.0/topics/templates/

---

### 💡 Sugerencia
Si quieres ampliar la app, puedes añadir:
- creación/edición/eliminación de tareas
- filtros por estado completado
- autenticación de usuarios
- búsqueda y ordenación de tareas
