# Creación de usuarios y grupos en FileZilla

## Creación de un grupo con permisos limitados
  1. Abrimos FileZilla Server Administration.
  2. Vamos a "Server-Configure-Groups".
    ![](https://github.com/JavierMoralesSimon/filezillaUsuariosGrupos/blob/main/Capturas/1.1.png)
  3. Damos a "Add" y le ponemos un nombre al grupo.
    ![](https://github.com/JavierMoralesSimon/filezillaUsuariosGrupos/blob/main/Capturas/1.2.png)
  4. Definimos el directorio raíz poniendo "/" en el "Virtual path" que es la ruta que ve el usuario FTP, y "/home" en "Native path" que es la ruta real del sistema.
    ![](https://github.com/JavierMoralesSimon/filezillaUsuariosGrupos/blob/main/Capturas/1.3.png)
  5. Definimos los permisos en "Mount options - Access mode" y le damos tanto de lectura como escritura. De borrado no porque ya lo controla FileZilla internamente.
    ![](https://github.com/JavierMoralesSimon/filezillaUsuariosGrupos/blob/main/Capturas/1.3.png)
  6. Definimos los límites de conexión en la sección "Limits". En este caso ponemos 5 conexiones simultáneas máximas entre todos los usuarios del grupo y 200kb/s de límite de velocidad por sesión a la hora de realizar subidas al servidor.
    ![](https://github.com/JavierMoralesSimon/filezillaUsuariosGrupos/blob/main/Capturas/1.4.png)
## Creación de dos usuarios asociados al grupo anterior


