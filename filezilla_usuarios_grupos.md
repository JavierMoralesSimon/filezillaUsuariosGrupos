# Creación de usuarios y grupos en FileZilla

## Creación de un grupo con permisos limitados
  1. Abrimos FileZilla Server Administration.
  2. Vamos a "Server-Configure-Groups".
    ![Server-Configure-Groups](https://github.com/JavierMoralesSimon/filezillaUsuariosGrupos/blob/main/Capturas/1.1.png)
  3. Damos a "Add" y le ponemos un nombre al grupo.
    ![Añadir grupo](https://github.com/JavierMoralesSimon/filezillaUsuariosGrupos/blob/main/Capturas/1.2.png)
  4. Definimos el directorio raíz poniendo "/" en el "Virtual path" que es la ruta que ve el usuario FTP, y "/home" en "Native path" que es la ruta real del sistema.
    ![Directorio raíz](https://github.com/JavierMoralesSimon/filezillaUsuariosGrupos/blob/main/Capturas/1.3.png)
  5. Definimos los permisos en "Mount options - Access mode" y le damos tanto de lectura como escritura. De borrado no porque ya lo controla FileZilla internamente.
    ![Permisos](https://github.com/JavierMoralesSimon/filezillaUsuariosGrupos/blob/main/Capturas/1.3.png)
  6. Definimos los límites de conexión en la sección "Limits". En este caso ponemos 5 conexiones simultáneas máximas entre todos los usuarios del grupo y 200kb/s de límite de velocidad por sesión a la hora de realizar subidas al servidor.
    ![Límites de conexión](https://github.com/JavierMoralesSimon/filezillaUsuariosGrupos/blob/main/Capturas/1.4.png)

## Creación de dos usuarios asociados al grupo anterior
  1. Vamos a "Users" que está justo debajo de "Groups".
  2. Damos a "Add" y le ponemos un nombre al usuario.
    ![Añadir usuario](https://github.com/JavierMoralesSimon/filezillaUsuariosGrupos/blob/main/Capturas/2.1.png)
  3. Ponemos que se requiera una contraseña para loguearse e introducimos la misma.
    ![Contraseña](https://github.com/JavierMoralesSimon/filezillaUsuariosGrupos/blob/main/Capturas/2.2.png)
  4. Lo hacemos miembro del grupo anteriormente creado.
    ![Miembro de grupo](https://github.com/JavierMoralesSimon/filezillaUsuariosGrupos/blob/main/Capturas/2.3.png)
  5. Repetimos el proceso para crear otro usuario.
    ![Creación del segundo usuario](https://github.com/JavierMoralesSimon/filezillaUsuariosGrupos/blob/main/Capturas/2.4.png)

## Permisos de grupo vs de usuario
* Permisos de grupo:
  * Se definen una sola vez.
  * Contienen:
    * Directorios compartidos.
    * Permisos.
    * Límites de conexión.
  * Funcionamiento:
    * Todos los usuarios asociados al grupo heredan automáticamente estos permisos.
    * Se aplican por defecto a los usuarios.
    * Permite gestionar muchos usuarios a la vez sin tocar cada uno.

* Permisos de usuario:
  * Se definen individualmente por cada usuario.
  * Pueden incluir:
    * Contraseña / métodos de autenticación.
    * Directorios compartidos propios.
    * Permisos propios.
    * Límites propios.
  * Funcionamiento:
    * Solo afectan a un usuario.
    * Sobrescriben o añaden a los permisos de grupo al que pertenece el usuario (si es el caso), dependiendo de la opción.
