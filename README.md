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

## CRUD de publicaciones

El proyecto permite realizar las operaciones principales sobre las publicaciones:

- Crear una publicación.
- Ver el listado de publicaciones.
- Ver el detalle de una publicación.
- Editar una publicación.
- Eliminar una publicación con confirmación.

## Manejo de imágenes

Las publicaciones pueden tener una imagen opcional.

El modelo `Post` utiliza un `ImageField` para guardar las imágenes en la carpeta `media/posts/`.

Se configuraron:

- `MEDIA_URL = '/media/'`
- `MEDIA_ROOT = BASE_DIR / 'media'`

También se utiliza **Pillow** para permitir el manejo de imágenes.

## Formularios

Se creó `posts/forms.py` utilizando `ModelForm` para facilitar la creación y edición de publicaciones.

El formulario permite ingresar:

- Título
- Contenido
- Autor
- Estado
- Imagen

Para subir imágenes se utiliza un formulario con `enctype="multipart/form-data"`.

## Cómo probar la carga de imágenes

1. Iniciar el servidor:
python manage.py runserver

2. Ingresar a:
http://127.0.0.1:8000/posts/

3. Seleccionar Crear nueva publicación.
Completar los datos y seleccionar una imagen.

4. Guardar la publicación.
Entrar al detalle de la publicación para comprobar que la imagen se muestra correctamente.

También es posible editar una publicación y cambiar su imagen.

## Tecnologías utilizadas

- Python
- Django
- Git
- GitHub