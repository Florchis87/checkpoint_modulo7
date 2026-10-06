# Blog Django

## Descripción

Este proyecto consiste en la estructura inicial de un blog web desarrollado con Django.

Incluye el proyecto Django `blog_project` y una aplicación principal llamada `posts`.

## Aplicación principal

- `posts`: aplicación inicial para manejar las publicaciones del blog.

## Instalación

### 1. Clonar el repositorio

```bash
git clone URL_DEL_REPOSITORIO
```

### 2. Entrar a la carpeta del proyecto

```bash
cd blog_django
```

### 3. Crear el entorno virtual

```bash
python -m venv venv
```

### 4. Activar el entorno virtual

En Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

En Linux o macOS:

```bash
source venv/bin/activate
```

### 5. Instalar las dependencias

```bash
pip install -r requirements.txt
```

## Ejecutar el proyecto

Para iniciar el servidor de desarrollo:

```bash
python manage.py runserver
```

Luego abrir en el navegador:

```text
http://127.0.0.1:8000/
```

## Panel de administración

Para acceder al panel de administración de Django:

1. Iniciar el servidor con:

python manage.py runserver

2. Abrir en el navegador:
http://127.0.0.1:8000/admin/

3. Ingresar con el usuario y contraseña del superusuario creado mediante:
python manage.py createsuperuser

## Tecnologías utilizadas

- Python
- Django
- Git
- GitHub