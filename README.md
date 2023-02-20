# Zapateria Angelina
Main branch

# Indice
- [Instalar git](#instalar-git)
- [Configuracion](#configuracion-inicial)
- [Github y SSH](#crear-un-usuario-en-github-y-agregar-clave-ssh)
- [Clonar un repositorio](#clonar-un-repositorio-de-github)
- [Obtener permisos](#obtener-permisos-de-lectura/escritura)
- [Subir cambios](#subir-los-cambios-al-repositorio)

# Instalar git
Segir la guia del sitio oficial para su instalacion dependiendo del sistema operativos
[Instalar git](https://git-scm.com/download/win)
**Tambien es posible instalarlo desde la terminal *powershell* de windows con:**

```bash
   winget install --id Git.Git -e --source winget
```

# Configuracion inicial
Una vez instalado es necesario abrir *git bash* o *powershell*
**Configuración global**
``` bash
  git config --global user.name "Tu nombre/usuario de github" #Solo mostrar en los commits que realices
  git config --global user.email "Correo el que tengas github" #Sera necesario para generar la clave SSH
```

Ahora generaremos una clave SSH que nos servira para poder realizar cambios en el repositorio de github
``` bash
  ssh-keygen -t ed25519 -C "Correo de la configuracion anterior"
```
Cuando se ejecute el comando te preguntara con que nombre deceas guardarla, de preferencia un nombre que
te resulte facil de recordar.
Despues del nombre te pedira que le asignes una contraseña, es recomendable que asignes una aunque tampoco
es un paso obligatorio por lo que puedes dejarla en blanco y dar un **ENTER**, en caso de que quieras asiganar
una contraseña solo la tecleas y listo, en la pantalla no se mostrara nada (por temas de seguridad), al dar
**ENTER** te pedira una confirmacion.
Despues de esto te dira en donde se guardaron los archivo de la clave uno tendra una terminacion *.pub* y 
el otro solo sera el nombre que asignaste, el *.pub* es la clave publica que sera necesaria para github.

***Disclamer***

Quiza puede ser un poco confuso, por lo que dejare unos enlaces que pueden ser de ayuda

[Libro de git](https://uniwebsidad.com/libros/pro-git) 
*Lo que necesitas de aqui es el capitulo 1.3 y 1.5*

[Generar claves SSH](https://docs.github.com/en/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent?platform=windows)
*Quiza sea necesario cambiar el idioma a español*

# Crear un usuario en github y agregar clave SSH
Si ya cuentas con una cuenta de github no es necesario este paso.
Si no es haci, tendras que crearla en el siguiente enlace [github](https://github.com)

Una vez creada la cuenta de github, en necesario agregar la clave SSH generada anteriormente.
Dentro de tu cuenta de github, iremos a la configuracion

![settings](./Imagenes/settings.png)

Despues al apartado de SSH y GPG keys

![ssh y gpg keys](./Imagenes/ssh.png)

Ahora se mostraran las claves que tienes registradas (en mi caso tengo 2) y para agregarla daremos click en 'Nueca clave'

![nueva ssh](./Imagenes/new-ssh.png)

Aqui le pondras el nombre con que el que la quieras identicar, puedes usar el mismo nombre de la clave que vas registrar
y en el otro apartado pondra todo el contenido del archivo *.pub* que generaste anteriormente, click en 'Agreger SSH key'
y listo tendras tu clave SSH vinculada con github.

![nueva ssh 2](./Imagenes/new-ssh-2.png)

Es posible que llegue a ser un poco complicado al principio, asi que dejare un video que pueda ser de ayuda

[SSH GITHUB](https://www.youtube.com/watch?v=tY6IKEYz5vU)

# Clonar un repositorio de github
Esto es muy sencillo, solamente tenemos que dirigirnos a una carpeta vacia donde querramos clonar el repositorio
y abrir git bash con click derecho abrir un terminal aqui o algo asi deberia aparecer el windows, y ejecutar el 
siguiente comando
``` bash
  git clone git@github.com:IsidroITT/ZapateriaAngenila.git
```

![clonar repo](./Imagenes/clone-ssh.png)

# Obtener permisos de lectura/escritura

# Moverse en una branch

# Subir los cambios al repositorio
