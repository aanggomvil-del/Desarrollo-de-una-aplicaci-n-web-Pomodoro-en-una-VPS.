# Desarrollo-de-una-aplicación-web-Pomodoro-en-una-VPS.

# Índice

- Introducción
- 1. Título
- 2. Descripción
- 3. Justificación
- 4. Objetivos
- 5. Lenguajes de programación y tecnologías
- 6. Prototipo de interfaz de usuario
- 7. Gestor de bases de datos
- 8. Entornos de aplicación del proyecto
- 9. Fases de desarrollo
- 10. Módulos del ciclo formativo relacionados
- 11. Anexos y bibliografía

# Introducción

El propósito de este documento es presentar el anteproyecto del futuro Proyecto de Fin de Grado. Este anteproyecto es un paso fundamental, ya que servirá como una investigación preliminar del caso planteado. Su correcta elaboración es crucial para definir los conceptos clave y establecer las bases sólidas necesarias para el desarrollo del proyecto final.

# 1. Título

Desarrollo de una aplicación web Pomodoro en una VPS.

# 2. Descripción

El proyecto consiste en desarrollar una aplicación web basada en la técnica Pomodoro, un método de organización del tiempo que alterna periodos de trabajo concentrado con descansos. La aplicación permitirá a los usuarios registrarse, iniciar sesión, utilizar un temporizador y guardar sus sesiones de trabajo en una base de datos para poder consultar posteriormente su historial y el tiempo dedicado a sus actividades.

La aplicación se alojará en una máquina virtual privada (VPS) real, accesible a través de Internet. Además del desarrollo de la aplicación, se realizará la instalación y administración del sistema operativo del servidor, la configuración de los servicios necesarios y la aplicación de medidas de seguridad, copias de respaldo y monitorización.

# 3. Justificación

La organización del tiempo es importante para estudiantes y trabajadores, especialmente cuando necesitan mantener la concentración durante periodos prolongados. La técnica Pomodoro permite dividir el trabajo en intervalos de concentración y descanso, facilitando la planificación de las tareas y el seguimiento del tiempo empleado.

Actualmente existen aplicaciones que utilizan este método, como [Pomofocus](https://pomofocus.io) y [Focus To-Do](https://www.focustodo.cn). Estas herramientas ofrecen temporizadores y funcionalidades relacionadas con la productividad, y algunas incorporan estadísticas o gestión de tareas. Por tanto, existe una necesidad real de aplicaciones que permitan organizar el tiempo y consultar el progreso personal.

La propuesta se diferencia de estas soluciones en que el objetivo no es únicamente crear un temporizador, sino también administrar toda la infraestructura necesaria para poner en funcionamiento una aplicación web propia. El sistema se desplegará en una VPS real, con una base de datos propia y medidas de seguridad configuradas manualmente.

El proyecto permitirá aplicar conocimientos de administración de sistemas operativos, redes, servicios web, bases de datos y ciberseguridad. Además, permitirá comprender el funcionamiento de una aplicación accesible desde Internet, desde la configuración del servidor hasta la interacción del usuario con la interfaz web.

# 4. Objetivos

## Objetivo principal

Desarrollar y desplegar una aplicación web Pomodoro funcional en una VPS real, accesible desde Internet, que permita gestionar usuarios, realizar sesiones de concentración y almacenar su historial en una base de datos.

## Objetivos específicos

1. Contratar o conseguir una VPS adecuada para alojar la aplicación.
2. Instalar y configurar un sistema operativo Linux en el servidor.
3. Configurar el acceso remoto mediante SSH para administrar el servidor.
4. Aplicar medidas básicas de seguridad, como la configuración del cortafuegos, la actualización del sistema y la protección del acceso administrativo.
5. Desarrollar una interfaz web sencilla e intuitiva, adaptable a ordenadores y dispositivos móviles.
6. Implementar un sistema de registro de usuarios, inicio de sesión y cierre de sesión.
7. Desarrollar un temporizador Pomodoro que permita iniciar, pausar y reiniciar los periodos de trabajo y descanso.
8. Crear una base de datos para almacenar los usuarios y las sesiones realizadas.
9. Permitir que cada usuario consulte exclusivamente su propio historial de sesiones y su tiempo acumulado.
10. Configurar un servidor web para publicar la aplicación y permitir su acceso desde Internet.
11. Configurar copias de seguridad de la base de datos y comprobar que pueden restaurarse.
12. Realizar pruebas funcionales y de seguridad para verificar el correcto funcionamiento del sistema.
13. Documentar la instalación, configuración, administración y mantenimiento de la infraestructura.

# 5. Lenguajes de programación y tecnologías

| Tecnología | Utilidad |
|---|---|
| HTML | Crear la estructura de las páginas web. |
| CSS | Diseñar la apariencia visual y adaptar la interfaz a diferentes dispositivos. |
| JavaScript | Implementar el temporizador, sus controles y las interacciones de la interfaz. |
| Python | Desarrollar la lógica de la aplicación web y gestionar las peticiones de los usuarios. |
| Flask | Utilizar un framework ligero de Python para desarrollar el sistema web. |
| SQL | Consultar, insertar, modificar y eliminar información en la base de datos. |
| Bash | Automatizar tareas de administración, copias de seguridad y mantenimiento del servidor. |
| Linux (Ubuntu Server) | Sistema operativo para alojar y administrar la aplicación en la VPS. |
| MySQL | Sistema gestor de bases de datos para almacenar usuarios y sesiones. |
| Nginx | Servidor web y proxy inverso para publicar la aplicación. |
| Gunicorn | Ejecutar la aplicación Flask mediante un servidor WSGI adecuado para producción. |
| SSH | Administrar remotamente el servidor de forma segura. |
| UFW | Configurar las reglas básicas del cortafuegos de Linux. |
| HTTPS y TLS | Cifrar las comunicaciones entre el navegador y la aplicación web. |
| Git | Controlar las versiones del código fuente y registrar los cambios realizados. |

# 6. Prototipo de interfaz de usuario

La aplicación contará con una interfaz sencilla, con un diseño limpio y orientado a facilitar la concentración. Se priorizarán los elementos esenciales para evitar distracciones.

Se plantean las siguientes pantallas principales:

## Pantalla de inicio de sesión

Permitirá a los usuarios acceder a su cuenta mediante su correo electrónico o nombre de usuario y contraseña. También incluirá un enlace para registrarse si todavía no tienen una cuenta.

## Pantalla de registro

Permitirá crear una cuenta mediante un nombre de usuario, correo electrónico y contraseña. Se comprobará que los datos introducidos sean válidos y que no exista otra cuenta con el mismo correo electrónico.

## Pantalla principal del temporizador

Será la pantalla central de la aplicación. Mostrará el tiempo restante, el tipo de intervalo y los controles necesarios para manejar el temporizador.

Los tiempos iniciales podrán configurarse, por ejemplo, en 25 minutos de trabajo y 5 minutos de descanso. Como mejora, se podrá incorporar un descanso largo después de varias sesiones completadas.

## Pantalla de historial

Permitirá consultar las sesiones almacenadas en la base de datos, mostrando la fecha, la duración y el tipo de sesión. También incluirá un resumen del tiempo de concentración acumulado. La interfaz definitiva se concretará durante la fase de diseño y podrá modificarse según los resultados de las pruebas.

**Prototipo realizado con Figma:**

[Ver prototipo de la aplicación en Figma](https://www.figma.com/make/n5s3H0z8S6rrPO1G47NaG4/Login-and-Registration-Screens?t=RmFLVqNqZYIlehIS-1)

# 7. Gestor de bases de datos

El sistema gestor de bases de datos propuesto es MySQL Server, que permitirá almacenar de manera estructurada la información de los usuarios y las sesiones Pomodoro.

La base de datos se denominará `pomodoro_db` y estará formada inicialmente por dos tablas principales: usuarios y sesiones.

## Tabla usuarios

| Campo | Tipo propuesto | Descripción |
|---|---|---|
| id_usuario | INT | Identificador único del usuario y clave primaria. |
| nombre_usuario | VARCHAR(50) | Nombre utilizado por el usuario. |
| email | VARCHAR(120) | Correo electrónico único. |
| password_hash | VARCHAR(255) | Hash de la contraseña, nunca la contraseña en texto plano. |
| fecha_registro | DATETIME | Fecha de creación de la cuenta. |

## Tabla sesiones

| Campo | Tipo propuesto | Descripción |
|---|---|---|
| id_sesion | INT | Identificador único de la sesión y clave primaria. |
| id_usuario | INT | Identificador del usuario propietario y clave foránea. |
| tipo_sesion | VARCHAR(20) | Tipo de intervalo: trabajo, descanso corto o descanso largo. |
| duracion_segundos | INT | Duración efectiva registrada de la sesión. |
| fecha_inicio | DATETIME | Fecha y hora de inicio. |
| fecha_fin | DATETIME | Fecha y hora de finalización. |
| completada | BOOLEAN | Indica si la sesión se ha completado. |

## Modelo Entidad-Relación

La relación entre las entidades será de uno a muchos: un usuario podrá tener numerosas sesiones, mientras que cada sesión pertenecerá exclusivamente a un usuario.

La clave foránea `id_usuario` permitirá relacionar ambas tablas. Además, las consultas del historial deberán filtrar las sesiones por el usuario autenticado, evitando que una persona pueda consultar los registros de otra.

# 8. Entornos de aplicación del proyecto

El proyecto se desarrollará, probará y desplegará en dos entornos diferentes.

## Entorno de desarrollo y pruebas

- **Ordenador personal:** equipo utilizado para escribir el código, diseñar la interfaz y administrar el proyecto.
- **Sistema operativo local:** Windows o Linux, según el equipo disponible.
- **Editor de código:** Visual Studio Code o un editor equivalente.
- **Git:** control de versiones del código fuente.
- **Python y Flask:** desarrollo y pruebas de la aplicación.
- **MySQL:** instalamos y administramos MySQL en la VPS, configurando los permisos de acceso, las copias de seguridad y la restauración de la base de datos.
- **Navegador web:** comprobación de la interfaz y de las funcionalidades.
- **Terminal:** ejecución de comandos, pruebas y scripts de administración.
- Este entorno permitirá desarrollar y corregir los errores antes de publicar los cambios en el servidor real.

## Entorno de producción

- **VPS real:** servidor contratado o conseguido a través de un proveedor de alojamiento. No se utilizará una máquina virtual de VirtualBox como servidor definitivo.
- **Ubuntu Server:** sistema operativo para administrar los recursos del servidor.
- **Conexión a Internet:** permitirá acceder a la aplicación desde otros equipos.
- **Dirección IP pública y dominio:** permitirán localizar la aplicación desde Internet. El dominio dependerá de su disponibilidad y de los recursos económicos.
- **SSH:** administración remota del sistema.
- **Nginx y Gunicorn:** publicación y ejecución de la aplicación.
- **MySQL:** almacenamiento de los datos de usuarios y sesiones.
- **Cortafuegos:** control de los puertos y conexiones permitidos.
- **Certificado TLS:** habilitación de HTTPS para proteger las comunicaciones.
- **Sistema de copias de seguridad:** protección de la información ante pérdidas o errores.
- **Herramientas de monitorización y registros:** seguimiento del funcionamiento del sistema, consumo de recursos y posibles incidencias.

No será necesario utilizar routers o switches físicos adicionales, ya que la infraestructura de red será proporcionada por el proveedor de la VPS.

# 9. Fases de desarrollo

El proyecto se organizará en las siguientes fases:

## 1. Planificación inicial

Todas las tareas se han definido en la plataforma Jira, proporciono el enlace para consultarlas:
[Consultar tareas en Jira](https://iestriana-team-htu9wsyr.atlassian.net/jira/software/projects/KAN/boards/1/timeline)

## 2. Análisis y diseño

Se diseñarán las pantallas principales de la aplicación, la estructura de la base de datos y la arquitectura del sistema. Se determinarán los requisitos funcionales y las medidas de seguridad que deberán aplicarse.

## 3. Preparación de la VPS

Se instalará y configurará Ubuntu Server, se creará el acceso administrativo mediante SSH y se preparará el entorno necesario para desplegar la aplicación. Se aplicarán las primeras medidas de bastionado del sistema.

## 4. Desarrollo de la aplicación

Se implementarán las siguientes funciones:

- Registro de usuarios e inicio de sesión.
- Temporizador de trabajo y descanso.
- Registro de las sesiones completadas.
- Almacenamiento de información en MySQL.
- Consulta del historial personal.
- Interfaz web adaptable a distintos dispositivos.

## 5. Configuración de los servicios

Se configurarán MySQL, Gunicorn y Nginx. Se establecerá la conexión entre la aplicación y la base de datos, y se preparará el acceso desde Internet mediante la dirección IP pública o un dominio. También se configurará HTTPS y se revisarán las reglas del cortafuegos.

## 6. Pruebas y validación

Se comprobará que el registro y el inicio de sesión funcionan correctamente, que el temporizador respeta los intervalos configurados y que las sesiones se almacenan y consultan correctamente. Se probará también que los usuarios no pueden acceder al historial de otras cuentas, que los servicios funcionan correctamente y que las copias de seguridad pueden restaurarse.

## 7. Despliegue y puesta en marcha

Se publicará la versión validada de la aplicación en la VPS y se comprobará su accesibilidad desde un equipo externo.

Se verificará el funcionamiento de los servicios y se documentará la configuración final.

## 8. Mantenimiento y documentación

Se elaborará la documentación técnica con los pasos de instalación, configuración, administración, seguridad, copias de respaldo y recuperación. Se registrarán las incidencias encontradas y las soluciones aplicadas.

# 10. Módulos del ciclo formativo relacionados

## Administración de Sistemas Operativos (ASO)

Se aplicarán conocimientos de instalación y administración de Linux, gestión de usuarios y permisos, administración de servicios, automatización mediante Bash y mantenimiento del sistema operativo de la VPS.

## Administración de Sistemas Gestores de Bases de Datos (ASGBD)

Se diseñará e implementará la base de datos relacional, se crearán las tablas y relaciones necesarias y se realizarán consultas, copias de seguridad y restauraciones.

## Implantación de Aplicaciones Web (IAW)

Se desarrollará la aplicación web mediante HTML, CSS, JavaScript, Python y Flask. También se configurarán los servicios necesarios para publicar la aplicación y permitir su acceso desde Internet.

## Planificación y Administración de Redes (PAR)

Se trabajará con direccionamiento IP, puertos, servicios de red, DNS si se dispone de un dominio y comunicaciones entre el navegador, el servidor web y la aplicación.

## Seguridad y Alta Disponibilidad (SAD)

Se aplicarán medidas de bastionado, control de accesos, cortafuegos, protección de las comunicaciones, copias de seguridad y comprobaciones de recuperación. También se revisarán los registros y el estado de los servicios.

## Servicios de Red e Internet (SRI)

Se configurarán servicios relacionados con el acceso remoto, la publicación de la aplicación web y las comunicaciones seguras. Se estudiará el funcionamiento de los servicios necesarios para que la aplicación esté disponible desde Internet.

# 11. Anexos y bibliografía

Aquí se incluye el material complementario.

- **Anexos:** El prototipo de interfaz de usuario hecho con Figma, el gestor de base de datos.

- **Bibliografía:**

**Documentación oficial de Flask:** Guía de desarrollo y despliegue de aplicaciones web.

https://flask.palletsprojects.com

**Documentación oficial de Python:** Referencia del lenguaje de programación.

https://docs.python.org/3

**Documentación oficial de MySQL:** Manual del sistema gestor de bases de datos.

[https://dev.mysql.com/doc/](https://dev.mysql.com/doc/)

**Documentación oficial de Ubuntu Server:** Instalación, administración y seguridad del sistema operativo.

https://documentation.ubuntu.com/server

**Documentación oficial de Nginx:** Configuración y funcionamiento del servidor web.

https://nginx.org/en/docs

**Pomofocus:** Aplicación de referencia para el estudio de temporizadores Pomodoro y herramientas de productividad.

https://pomofocus.io

**Focus To-Do:** Aplicación de referencia para la organización de tareas y el seguimiento de sesiones de concentración.

https://www.focustodo.cn

