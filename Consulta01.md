# Consulta 01: Git, Gradle y Maven

# Git
![](Source/img/git01.png)

Imagen tomada de [aqui.](https://medium.com/@jclopex/que-es-git-desde-0-7678f4c3598d)<br/>

[Git](https://git-scm.com/) es un software de **control de versiones** diseñado por [**Linus Torvalds**](https://es.wikipedia.org/wiki/Linus_Torvalds), pensando en la eficiencia y la confiabilidad del mantenimiento de versiones de aplicaciones cuando éstas tienen un **gran número de archivos de código fuente**. Es decir **Git** nos proporciona las herramientas para desarrollar un trabajo en equipo de manera inteligente y rápida y por *trabajo* nos referimos a algún software o página que implique código el cual necesitemos hacerlo con un grupo de personas.

En cuanto a derechos de autor Git es un **software libre** distribuible bajo los términos de la versión 2 de la [Licencia Pública General de GNU](https://www.gnu.org/licenses/gpl-3.0.html).

<br />

![](Source/img/git02.jpg)

Imagen tomada de [aqui.](https://blog.dinahosting.com/herramientas-de-control-de-versiones/)<br/>

## ¿Qué es control de versiones?

Pues bien, se define como control de versiones a la gestión de los diversos cambios que se realizan sobre los elementos de algún producto o una configuración del mismo es decir a la gestión de los diversos cambios que se realizan sobre los elementos de algún producto o una configuración, y para los que aún no les queda claro del todo, control de versiones es lo que se hace al momento de estar desarrollando un software o una página web. Exactamente es eso que haces cuando subes y actualizas tu código en la nube, o le añades alguna parte o simplemente le editas cosas que no funcionan como deberían o al menos no como tú esperarías.

## Y, entonces ¿A qué le llamamos *sistema de control de versiones*?

Muy sencillo, son todas las herramientas que nos permiten hacer todas esas modificaciones antes mencionadas en nuestro código y hacen que sea más fácil la administración de las distintas versiones de cada producto desarrollado; es decir Git.

![](Source/img/git03.png)

Imagen tomada de [aqui.](https://medium.com/@jointdeveloper/sistemas-de-control-de-versiones-qu%C3%A9-son-y-por-qu%C3%A9-amarlos-24b6957e716e)<br/><br/>
[Sobre el Control de Versiones.](https://git-scm.com/book/es/v2/Inicio---Sobre-el-Control-de-Versiones-Fundamentos-de-Git)
<br/>

### Algunas de las características más importantes de Git son:

- Rapidez en la gestión de ramas, debido a que Git nos dice que un cambio será fusionado mucho más frecuentemente de lo que se escribe originalmente.

- Gestión distribuida; Los cambios se importan como ramas adicionales y pueden ser fusionados de la misma manera como se hace en la rama local.

- Gestión eficiente de proyectos grandes.

- Realmacenamiento periódico en paquetes.

## Los Tres Estados

Git tiene tres estados principales en los que se pueden encontrar tus archivos: confirmado (committed), modificado (modified), y preparado (staged). Confirmado: significa que los datos están almacenados de manera segura en tu base de datos local. Modificado: significa que has modificado el archivo pero todavía no lo has confirmado a tu base de datos. Preparado: significa que has marcado un archivo modificado en su versión actual para que vaya en tu próxima confirmación.

Esto nos lleva a las tres secciones principales de un proyecto de Git: El directorio de Git (Git directory), el directorio de trabajo (working directory), y el área de preparación (staging area).

![](Source/img/git04.png)

Imagen tomada de [aqui.](https://medium.com/@_moisesdelacruz/tutorial-b%C3%A1sico-de-git-y-github-42e46ff41194)<br/>

## Funcionamiento de Git

Básicamente, Git funciona del siguiente modo:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**1.** Crea un “repositorio” (proyecto) con una herramienta de alojamiento de git (como Bitbucket).  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**2.** Copia (o clona) el repositorio en tu equipo local.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**3.** Añade un archivo en tu repositorio local y “confirma” (guarda) los cambios.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**4.** “Envía” tus cambios a la rama maestra.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**5.** Realiza un cambio en tu archivo con una herramienta de alojamiento de git y confírmalo.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**6.** “Incorpora” los cambios en tu equipo local.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**7.** Crea una “rama” (versión), haz un cambio y confírmalo.  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**8.** Abre una “solicitud de incorporación de cambios” (propón cambios en la rama maestra).  
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;**9.** “Fusiona” tu rama con la rama maestra.  
<br/>
[Guía sencilla.](https://rogerdudler.github.io/git-guide/index.es.html)

![](Source/img/git05.png)

Imagen tomada de [aqui.](https://www.syloper.com/blog/desarrollo/versionando-codigo-con-git/)

### Guías de Instalación

[Windows.](https://git-scm.com/download/win)  
[Linux/Unix.](https://git-scm.com/download/linux) (Aunque generalmente viene preinstalado)  
[Mac OS X.](https://git-scm.com/download/mac)  

## Comandos Básicos

> "Añadir" se refiere a agregar archivos al *Staging Area* de git, es decir que git ya le estaría haciendo seguimiento a los cambios en dichos archivos

- Iniciar un repositorio vacío en unas carpeta específica:  
`git init`
- Añadir un archivo especifico:  
`git add <nombre_archivo>`
- Añadir todos los archivos del directorio "actual":  
`git add .`
- Guardar/confirmar cambios de los archivos que se encuentren en el *Staging Area*. El agregado `-m` es para añadir un mensaje **descriptivo** al commit:  
`git commit -m "<mensaje>"`
- Es el equivalente a hacer `git add .` y `git commit -m` juntos:  
`git commit -am "<mensaje>"`
- Lista todos los `commits` realizados a lo largo de nuestro proyecto:  
`git log`
- Sube la rama “nombre_rama” al servidor remoto:  
`git push origin <nombre_rama>`
- Descarga los cambios realizados en el repositorio remoto:  
`git fetch`
- Incluye en la rama que te encuentras parado, los cambios realizados en la rama “nombre_rama”:  
`git merge <nombre_rama>`
- Unifica los comandos `fetch` y `merge` en un único comando:  
`git pull`
- Muestra el estado actual de la rama, como los cambios que hay sin commitear:  
`git status`
- Crea una rama a partir de la que te encuentres parado con el nombre “nombre_rama_nueva”, y luego salta sobre la rama nueva, por lo que quedas parado en esta última:  
`git checkout -b <nombre_rama_nueva>`
- Si existe una rama remota de nombre “nombre_rama”, al ejecutar este comando se crea una rama local con el nombre “nombre_rama” para hacer un seguimiento de la rama remota con el mismo nombre:  
`git checkout -t origin/<nombre_rama>`
- Lista todas las ramas locales:  
`git branch`
- Lista todas las ramas locales y remotas:  
`git branch -a`
- Elimina la rama local con el nombre “nombre_rama”:  
`git branch -d <nombre_rama>`
- Actualiza tu repositorio remoto en caso que algún otro desarrollador haya eliminado alguna rama remota:  
`git remote prune origin`
- Elimina los cambios realizados que aún no se hayan hecho commit:  
`git reset --hard HEAD`
- Revierte el commit realizado, identificado por el “hash_commit”:  
`git revert <hash_commit>`

## Flujo de Trabajo

Git plantea una gran libertad en la forma de trabajar en torno a un proyecto. Sin embargo, para coordinar el trabajo de un grupo de personas en torno a un proyecto es necesario acordar como se va a trabajar con Git. A estos acuerdos se les llama **flujo de trabajo**.Un flujo de trabajo de Git es una **fórmula** o una **recomendación** acerca del uso de Git para realizar trabajo de forma **uniforme y productiva.** Los flujos de trabajo más populares son git-flow, GitHub-flow, GitLab Flow y One Flow.

### Git-Flow

Creado en 2010 por Vincent Driessen. Es el flujo de trabajo más conocido. Está pensado para aquellos proyectos que tienen entregables y ciclos de desarrollo bien definidos.Está basado en dos grandes ramas con infinito tiempo de vida (ramas **master** y **develop**) y varias ramas de apoyo, unas orientadas al desarrollo de nuevas funcionalidades (ramas **feature**), otras al arreglo de errores (**hotfix**) y otras orientadas a la preparación de nuevas versiones de producción (ramas **release**). La herramienta [gitflow](https://github.com/nvie/gitflow) facilita la automatización de las tareas implicadas en este flujo de trabajo

#### Master

Es la rama principal. Contiene el repositorio que se encuentra publicado en producción, por lo que debe estar siempre estable.

#### Development

Es una rama sacada de Master. Es la rama de integración, todas las nuevas funcionalidades se deben integrar en esta rama. Luego que se realice la integración y se corrijan los errores (en caso de haber alguno), es decir que la rama se encuentre estable, se puede hacer un merge de development sobre la rama Master.

#### Features

Cada nueva funcionalidad se debe realizar en una rama nueva, específica para esa funcionalidad. Estas se deben sacar de Development. Una vez que la funcionalidad esté desarrollada, se hace un merge de la rama sobre Development, donde se integrará con las demás funcionalidades.

#### Hotfix

Son errores de software que surgen en producción, por lo que se deben arreglar y publicar de forma urgente. Es por ello, que son ramas sacadas de Master. Una vez corregido el error, se debe hacer una unificación de la rama sobre Master. Al final, para que no quede desactualizada, se debe realizar la unificación de Master sobre Development.

#### Release

Las ramas de release apoyan la preparación de nuevas versiones de producción. Para ellos se arreglan muchos errores menores y se preparan adecuadamente los metadatos. Se suelen original de la rama develop y deben fusionarse en las ramas master y develop.

### GitHub-Flow

Creado en 2011 por [**GitHub**](https://github.com/) y es la forma de trabajo sugerida por las funcionalidades propias de GitHub . Está centrado en un modelo de desarrollo iterativo y de despliegue constante. Está basado en cinco principios:

- Todo lo que está en la rama master está listo para ser puesto en producción.  
- Para trabajar en algo nuevo, debes crear una nueva rama a partir de la rama master con un nombre descriptivo. El trabajo se irá integrando sobre esa rama en local y regularmente también a esa rama en el servidor.  
- Cuando se necesite ayuda o información o cuando creemos que la rama está lista para integrarla en la rama master, se debe abrir una pull request (solicitud de integración de cambios).  
- Alguien debe revisar y visar los cambios para fusionarlos con la rama master.  
- Los cambios integrados se pueden poner en producción.  

**GitHub** intenta simplificar la gestión de ramas, trabajando directamente sobre la rama master y generando integrando las distintas features directamente a esta rama.

### GitLab Flow

Creado en 2014 por [**Gitlab**](https://about.gitlab.com/). Es una especie de **extensión de GitHub Flow** acompañado de un conjunto de pautas y mejores prácticas que apuntan a estandarizar aún más el proceso. Al igual que GitHub Flow propone el uso de ramas de funcionalidad (feature) que se originan a partir de la rama master y que al finalizarse se mezclan con la rama master. Además introduce otros dos tipos de ramas:

- **Ramas de entorno.** Por ejemplo pre-production production. Se crean a partir de la rama master cuando estamos listos para implementar nuestra aplicación. Si hay un error crítico lo podemos arreglar en un rama y luego mezclarla en la rama de entorno.  
- **Ramas de versión.** Por ejemplo 1.5-stable 1.6-stable. El flujo puede incluir ramas de versión en caso de que el software requiera lanzamientos frecuentes.  

### One Flow

Creado en 2015 por Adam Ruka. En él cada nueva versión de producción está basada en la versión previa de producción. La mayor diferencia entre One Flow y Git Flow es que One Flow no tiene rama de desarrollo.

[comment]: <> (Cristhian)



## Github, Gitlab y Bitbucket
[comment]: <> (Alejandro)


# Gradle
[comment]: <> (Janer)

Gradle es una herramienta de código abierto para automatizar la construcción de proyectos, se centra en la flexibilidad y el rendimiento. 

Los scripts de compilación de Gradle se escriben utilizando **Groovy**, el cual es un lenguaje de programación orientado a objetos implementado sobre la plataforma Java, o **Kotlin DSL (Domain Specific Language)** el cual es también un lenguaje de programación de tipado estático que corre sobre la máquina virtual de Java y que también puede ser compilado a código fuente de JavaScript.

![Texto alternativo opcional si no se carga la imagen](https://gradle.org/images/gradle-knowledge-graph-logo.png?20170228)
> Imagen tomada de: https://gradle.org/images/gradle-knowledge-graph-logo.png?20170228 

Gradle fue seleccionado como la herramienta **oficial** de construcción para Android y cuenta con soporte para diversas tecnologías y lenguajes.

Algunas de las características que ofrece esta herramienta:

  - Altamente personalizable
  - Rápido
  - Potente
  - Flexibilidad
  - Permite trabajar en varios lenguajes
  - Tiene lenguaje DSL que simplifica
  - Tiene gestión de tendencias bastante optimizada

Gradle tiene una gran flexibilidad y nos permite hacer usos otros lenguajes además de **Java**, también cuenta con un sistema de **gestión de dependencias** muy estable. Gradle es altamente **personalizable y rápido** ya que completa las tareas de forma rápida y precisa **reutilizando** las salidas de las ejecuciones anteriores, sólo procesa las entradas que presentan cambios en paralelo.

![Texto alternativo opcional si no se carga la imagen](https://www.arquitecturajava.com/wp-content/uploads/diagramaGradle.gif)
> Imagen tomada de: https://www.arquitecturajava.com/wp-content/uploads/diagramaGradle.gif

### Iniciar en Gradle
Comenzar con Gradle es fácil, solo debe seguir las guías para [Descargar e Instalar Gradle](https://docs.gradle.org/current/userguide/installation.html) y luego consulte las [Guías de Introducción a Gradle](https://gradle.org/guides/#getting-started) para crear su primer proyecto, extraído desde la pagina oficial de Gradle. 

### Funcionalidades de la herramienta
Gradle al ser una herramienta tan flexible y potente, tiene una gran cantidad de funciones que puedes implementar en su uso, algunas de ellas son:
  - **Depuración colaborativa:** Permite compartir los resultados de la compilación para resolver en equipo de forma eficiente posibles problemas que aparezcan.
  - **Construcción incremental:** Valida en el proceso de compilación si la entrada, salida o implementación de una tarea ha cambiado, en caso de no existir algún cambio la considera actualizada y no se ejecuta.
  - **Diseño de repositorio personalizado:** Podremos tratar prácticamente cualquier estructura de directorios del sistema de archivos como un repositorio de Artifacts.
  - **Dependencias transitivas:** Es uno de los principales beneficios que ofrece al utilizar la gestión de dependencias ya que se encarga de descargar y administrar las dependencias transitivas.
  - **Soporte a Groovy y Scala incorporado:** Compatibilidad con los proyectos de Groovy, permitiendo trabajar con código Groovy o código Scala e inclusive desarrollar código mixto Java y Groovy o Java y Scala.
  - **Integración con Android Studio:** Android Studio no cuenta con un generador interno, sino que delega todas las tareas de compilación en Gradle, garantizando la corrección en todas las construcciones, ya sea que se ejecuten desde Android Studio, la línea de comandos o un servidor de construcción de integración continua.
  - **TestKit para pruebas funcionales:** Permite la ejecución prágramática de builds inspeccionando los resultados de compilación, ésta es una prueba de compatibilidad entre versiones.
  - **Lee el formato POM:** Es compatible con el formato de metadatos POM, por lo que es posible recuperar dependencias de cualquier repositorio compatible con Maven.
  - **Caché de dependencia de terceros:** Las dependencias de repositorios remotos se descargan y almacenan en caché localmente, las compilaciones posteriores utilizan los artifacts almacenados en caché para evitar el tráfico de red innecesario.
  - **Compara builds:** Resalta de forma rápida las diferencias entre compilaciones, lo que hace que el análisis de la causa raíz sea mucho más rápido y eficaz.

### Complementos de Gradle
Gradle permite construir desde **microservicios** hasta **aplicaciones móviles**, puede ser utilizado por pequeños **startups** como por grandes empresas, ya que ayuda a los equipos a desarrollar, automatizar y entregar software de calidad en un menor tiempo, aumentando su eficiencia.

Esta herramienta cuenta con una gran variedad de complementos o plugins que ayudan agilizar la construcción, entre los cuales destacamos los siguientes:

- **javamuc.gradle-semantic-build-versioning:** Proporciona soporte para vel ersionado semántico de las compilaciones, es fácil de usar y configurar.
- **io.freefair.maven-publish-war:** Permite crear una publicación de mavenWeb.
- **io.freefair.maven-publish-java:** Crea una publicación mavenJava.
- **org.mozilla.rust-android-gradle.rust-android:** Un complemento que ayuda a construir bibliotecas Rust JNI con Cargo para su uso en proyectos de Android.
- **net.wooga.build-unity:** Este complemento proporciona tareas para exportar proyectos de plataforma desde los proyectos de Unity3D.
- **de.db.vz.msintplugin:** Este complemento nos permitirá ejecutar pruebas de integración de microservicio con docker.
- **com.bmuschko.docker-remote-api:** Nos facilita la gestión de imágenes y contenedores Docker.
- **com.google.cloud.tools.jib:** Crea un contenedor para tu aplicación Java.

**Gradle** cuenta con paquetes para ser implementado en cualquier plataforma su gran versatilidad permite trabajar con monorepos o multirepositorios, modelando, sistematizando y construyendo soluciones exitosas, de forma rápida y precisa.


# Maven
[comment]: <> (Hernan)
