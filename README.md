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

Una rama nos permite aislar una nueva funcionalidad en nuestro código la cual después podremos añadir a la versión principal.

![Ramas Git](./img/ramas.jpeg)

## Fusiones

Une dos ramas. Para ahcer una fusión necesitamos:

1. Situarnos en la rama que se quedará en el contenido fusionado.
1. Fusionar.

Cuando se fusionan ramas se pueden dar 2 resultados diferentes:

- **_Fast-Forwad:_**: La fusión se hace automática, no hay conflictos por resolver.
- **_Manual Merge_**: La fusión hay que hacerla maual, para resolver conflictos de la duplicación de contenido. 

![Fusion Rama Git](./img/fusion-rama-git.jpeg)

Como vas ivan
