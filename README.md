# coder-session-mongo-atlas LOG-IN POR FORMULARIO


## Consigna: 
Continuando con el desafío de la clase anterior, vamos a incorporar un mecanismo sencillo que
permite loguear un cliente por su nombre, mediante un formulario de ingreso.
Luego de que el usuario esté logueado, se mostrará sobre el contenido del sitio un cartel con el
mensaje “Bienvenido” y el nombre de usuario. Este cartel tendrá un botón de deslogueo a su
derecha.
Verificar que el cliente permanezca logueado en los reinicios de la página, mientras no expire el
tiempo de inactividad de un minuto, que se recargará con cada request. En caso de alcanzarse ese
tiempo, el próximo request de usuario nos llevará al formulario de login.
Al desloguearse, se mostrará una vista con el mensaje de 'Hasta luego' más el nombre y se
retornará automáticamente, luego de dos segundos, a la vista de login de usuario.

## Aspectos a incluir en el entregable:
* La solución entregada deberá persistir las sesiones de usuario en Mongo Atlas

* Verificar que en los reinicios del servidor, no se pierdan las sesiones activas de los clientes.

* Mediante el cliente web de Mongo Atlas, revisar los id de sesión correspondientes a cada
cliente y sus datos.

* Borrar una sesión de cliente en la base y comprobar que en el próximo request al usuario se le
presente la vista de login.

* Fijar un tiempo de expiración de sesión de 10 minutos recargable con cada visita del cliente al
sitio y verificar que si pasa ese tiempo de inactividad el cliente quede deslogueado.

<sup>Formato de entrega: link a un repositorio en Github con los tres proyectos en
carpetas separadas. No incluir los node_modules.</sup>

# Como ejecutar el proyecto
### En tu pc
- Antes que nada debes tener instalado en tu pc node.js
- Debes clonar el repositorio
- Abrir una terminal y en ella dirigirte a la carpeta con el nombre del proyecto
- Ejecutar el comando ``` npm install ```
- Deves configurar un archivo ``` .env ``` con los siguientes datos
    ```
    MONGO_USER = "<usuario de mongo atlas>"
    MONGO_PASS = "<contraseña de mongo atlas>"
    ```
- Una vez finalizado el punto anterior, ejecutar el comando ``` npm run start ```
- Luego dirigite a tu navegador de preferencia a [esta ruta](http://localhost:8080/api/productos-test) 
para testear la app