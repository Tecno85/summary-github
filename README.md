# Git & GitHub - JonMircha

Git es un software de conrtol de versiones distribuido y descentralizado que permite a un equipo de desarrolladores trabajar sobre el mismo código.

Se denomina **"distribudido"** porque cada mienbro del equipo deispone de una copia completa de código.

Los miembros del equipo pueden enviarse código, recibirlo y desarrollar funcionalidades de forma conjunta y separada del servidor central.

## Algunas ventajas de usarlo

- Es el estandar actual
- Código colaborativo, vresionado y distribuido
- Recupareción de archivos
- Mayor control
- Shorcuts y plugins
- Mejora la productividad
- Imagen Git

![Mapa de Git](./img/git-mapa.png)

## Configuración Inicial

### Configurando Git por primera vez

![Configuración Git](./img/confiInicial.png)

### Inicializar Git en un directorio local

![Directorio Local](./img/iniciarRepositorio.png)

## Flujo Básico

El flujo de _Git_, consta de tres estados locales, es decir en la computadora donde se está trabajando y uno más de forma remota cuando accedemos al código centralizado en platadormas como GitHub, Gitlab, Bitbucket, etc.

Dichos estados con **modified**, **stage**, **committed** y **remote** A cada uno de ellos les corresponde un área de trabajo:

1. **Working Directory**: Es el área correspondiente al estado **_Modified_** y es la carpeta local de tu computadora donde se almacenan los archivos de tu proyecto. El estado **Modified(Modificado)**, hace referencia ha que se han realizado cambios en el **archivo(Editado)**, pero aún no se han prepadarado esos cambios para ser confirmados. Ejemplo: Se ha editado un o varios archivos de código, pero no has indicado a _Git_ que quieres incluir esos cambios al proximo commit.

1. **Staging Area(Área de Preparación):** Es el área correspondiente al estado **Stage(preparación)**, tambien se le llama index porque es el área donde _git_ indexa (área intermedia donde se almacenan los cambios antes de confirmarlos - zona de espera donde puedes seleccionar y revisar los cambios que deseas incluir enntu próximo commit) y agrega los cambios realizados en los atchivos previos a comprometerlos en su registro. Ejemplo: Después de editar un archivo, decides que está listo para ser guardado en el historial de cambios. Usas _git add_ para moverlo al área de preparación _(staging area)_. **git add**: Este comando se usa para agregar cambios al índice git add archivo.txt

1. **Local Repository(Repositorio Local)**: Es el área correspodiente al estado committed, en esta se guardan los cambios en el historial de _Git_. Estos cambios ahora estan en tu repositorio local. Ejmplo: Despues de preparar los cambios, los confirmas para que se añadan al historial de _Git_ o _HEAD_, creando un punto de referencia en el proyecto. **git commit -m** "Mensaje del commit"

1. **Remote Repository(Repositorio Remoto)**: Es el área correspondiente al estado remote y es el directorio remoto donde se almacena una versión del proyecto o los archivos del proyecto en alguna plataforma web como _GitHub_, _GitLab_, _BitBucket_ etc. _Git_ denomina origin al repositorio remoto.Y permite colaborar y sincronizar tu trabajo con otros. Ejemplo: Después de hacer commits en tu repositorio local, puedes enviar esos cambios al repositorio remoto para compartirlos con otros o para tener una copia de seguridad.

![Flujo Básico Git](./img/git-flow.png)

![Pasos Flujo Básico](./img/pasos-git.jpeg)

## Ignorar Archivos

En el archivo **_.gitignore_** colocamos todo lo archivo que **NO** deseemos incluir en nuestro repositiorio. Lo podemos crear manualmente o con _.gitignore.io_

![Imagen gitignore](./img/gitignore.jpeg)

## Clonar Repositorios

Para realizar la clonación de un repositorio, nos dirigimos a la URL del repositorio, la copiamos, abrimos la terminal de comandos y utilizamos el comando  ``git clone`` seguida de la URL del repositorio que deseamos clonar. Finalmente para verificar la clonación usamos el comando ``ls``

``git clone https: //github.com/usuario/repositorio.git``

## Ramas

Una rama es como una línea de desarrollo separada dentro de un proyecto. Es como una copia en la que se puede trabajar si afectar la versión principal del proyecto(main). En otras palabras nos permite aislar una nueva funcionalidad en nuestro código la cual después podremos añadir a la versión principal.

Pasos:

1. **Rama Principal(main/master)**: Esta es la línea de desarrollo principal donde normalmente se encuentra el código más estable y listo para producción.

1. **Crear una Nueva Rama**: Cuando quieras trabajar en una nueva funcionalidad o corregir un error, creas una nueva rama. Esto permite realizar cambios sin alterar la rama principal.

1. **Trabajaar en la Nueva Rama**: Realizas todos tus cambios en esta nueva rama. Puedo realizar commits y pruebas sin preocuparme por romper nada en la rama principal.

1. **Funcionar (merge)**: Una vez que termino de trabajar y todo está probado, puedo fusionar mi rama con la rama principal. Esto incorpora todos mis cambios al código estable.

1. **Eliminar la Rama**: Despúes de fusionar, puedes eliminar la rama ya que los cambios han sido incorporados a la rama principal.

**Nota**: Si quiero que una rama en la cual estoy trabajando exista en remoto, debo de escribir este comando al momento de realizar el git push: `git push -u origin "nombre-nueva-rama"`
Para eliminar una rama remota escribo el siguiente comando: `git push origin --delete "nombre-rama"`

![Ramas Git](./img/ramas.jpeg)

## Fusiones

Une dos ramas. Para ahcer una fusión necesitamos:

1. Situarnos en la rama que se quedará en el contenido fusionado.
1. Fusionar.

Cuando se fusionan ramas se pueden dar 2 resultados diferentes:

- **_Fast-Forwad:_**: La fusión se hace automática, no hay conflictos por resolver.
- **_Manual Merge_**: La fusión hay que hacerla maual, para resolver conflictos de la duplicación de contenido.

![Fusion Rama Git](./img/fusion-rama-git.jpeg)

## Cambios

Puedes agregar modificaciones al ultimo cambio

![Imagen Cambios Commits](./img/cambios-commit.jpeg)

Podemos desplazarnos en el historial del repositorio hacia atrás o adelante en cambios o ramas, sin afectar el respositorio como tal. Nota: Se recomienda `NO` realizar el `push` antes de hacer el cambio en el `commit` puesto que dicha acción traera conflictos entre el archivo en local y el remoto.

![Imagen Moverse Commit](./img/moverse-commit.jpeg)

## Registro del Historial

**_Git log_** nos permite conocer todo el historial de un proyecto, con la información de fecha, el autor y el id de cada cambio. Para salir de este se presiona la tecla `q`.

La opción `git log --oneline --graph --all`, nos permite ver los direferentes `commits` en forma gráfica.

![Registro Commits](./img/registro-commit.jpeg)

![Gráficas Commits](./img/grafica-commits.png)

## Reseteo del Historial

Podemos eliminar el historial de cambios del proyecto hacia adelante con respecto de un punto de referencia.

Esta es una <span style="color:orange;">palabra</span> en color azul en una oración.
