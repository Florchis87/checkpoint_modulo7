
Blog Django

Descripción

Proyecto web desarrollado con Django que permite gestionar publicaciones y usuarios. Incluye el proyecto blog_project y las aplicaciones posts y accounts.

Aplicaciones

posts: permite crear, listar, consultar, editar y eliminar publicaciones.

accounts: permite registrar usuarios, iniciar y cerrar sesión, y gestionar perfiles personales.

Instalación

1. Clonar el repositorio

git clone https://github.com/Florchis87/checkpoint_modulo7.git

2. Entrar a la carpeta del proyecto

cd blog_django

3. Crear el entorno virtual

python -m venv venv

4. Activar el entorno virtual

En Windows PowerShell:

.\venv\Scripts\Activate.ps1

En Linux o macOS:

source venv/bin/activate

5. Instalar las dependencias

pip install -r requirements.txt

6. Aplicar las migraciones

python manage.py migrate

7. Iniciar el servidor

python manage.py runserver

Abrir el sitio en el navegador:

http://127.0.0.1:8000/

Usuarios y autenticación

La aplicación permite:

Registrar nuevos usuarios.

Iniciar sesión.

Cerrar sesión.

Acceder a las funcionalidades protegidas después de iniciar sesión.

Las páginas de listado y detalle de publicaciones permanecen disponibles para visitantes.

Perfiles de usuario

Cada usuario dispone de un perfil con los siguientes campos:

Biografía.

Enlace web.

Avatar opcional.

El perfil puede consultarse y editarse desde las páginas correspondientes.

CRUD de publicaciones

El proyecto permite realizar las operaciones principales sobre las publicaciones:

Crear una publicación.

Ver el listado de publicaciones.

Consultar el detalle de una publicación.

Editar una publicación.

Eliminar una publicación mediante una confirmación.

Las funciones para crear, editar y eliminar publicaciones requieren iniciar sesión.

Manejo de imágenes

Las publicaciones pueden incluir una imagen opcional mediante el campo ImageField del modelo Post.

Las imágenes de las publicaciones se guardan en media/posts/. Los avatares se gestionan mediante el campo correspondiente del perfil.

La configuración de archivos multimedia utiliza:

MEDIA_URL = '/media/'
MEDIA_ROOT = BASE_DIR / 'media'

Se utiliza Pillow para permitir el manejo de imágenes.

Formularios

En la aplicación posts se utiliza PostForm, basado en ModelForm, para crear y editar publicaciones.

El formulario incluye:

Título.

Contenido.

Autor.

Estado.

Imagen.

Los formularios que permiten subir archivos utilizan enctype="multipart/form-data".

La aplicación accounts incluye formularios para el registro y la edición del perfil.

Cómo probar el proyecto

Iniciar el servidor con python manage.py runserver.

Entrar a http://127.0.0.1:8000/accounts/registro/ para registrar un usuario.

Iniciar sesión desde la página correspondiente.

Entrar a http://127.0.0.1:8000/accounts/perfil/ para consultar el perfil.

Editar la biografía y probar la carga de un avatar.

Entrar a http://127.0.0.1:8000/posts/ para consultar las publicaciones.

Crear una publicación y probar la carga de una imagen.

Abrir el detalle para comprobar que la imagen se muestra correctamente.

Probar la edición y la eliminación de una publicación.

Cerrar sesión e intentar acceder a una ruta protegida para comprobar la redirección al login.

Panel de administración

Para acceder al panel de administración:

Iniciar el servidor.

Abrir http://127.0.0.1:8000/admin/.

Ingresar con un superusuario creado mediante:

python manage.py createsuperuser

Tecnologías utilizadas

Python
Django
Pillow
HTML
CSS
Git
GitHub

## Autora
María Florencia Vega
Proyecto desarrollado como trabajo final del curso de Python.