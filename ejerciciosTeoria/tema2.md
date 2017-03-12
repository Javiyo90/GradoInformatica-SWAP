**TEMA 2: Alta disponibilidad y escalabilidad**


**Ejercicio T2.1:
Calcular la disponibilidad del sistema si tenemos dos réplicas de cada elemento (en total 3 elementos en cada subsistema).**

| Servidores | Sin réplica | 1 réplica | 2 réplicas |
|--------|--------|--------|--------|
|Web|85%|97,75%|85%+(1-85%)*97,75%= 99,6625%|
|Aplicación|90%|99%|90%+(1-90%)*99%= 99,9%|
|Database|99,9%|99,9999%|99,9%+(1-99,9%)*99,9999%= 100%|
|DNS|98%|99,96%|98%+(1-98%)*99,96%= 99,9992%|
|Firewall|85%|97,75%|85%+(1-85%)*97,75%= 99,6625%|
|Switch|99%|99,99%|99%+(1-99%)*99,99%= 99,9999%|
|Data Center|99,99%|99,99%|99,99%+(1-99,99%)*99,99%= 99,99%|
|ISP|95%|99,75%|95%+(1-95%)*99,75%= 99,9875%|
|**TOTAL**|59,866972%|94,30193%|99,203595%|


**Ejercicio T2.2:
Buscar frameworks y librerías para diferentes lenguajes que permitan hacer aplicaciones altamente disponibles con relativa facilidad.**

- Linux-HA provee de una solución de alta disponibilidad para Linux, FreeBSD, OpenBSD, Solaris y Mac OS X promoviendo fiabilidad, disponibilidad y servicialidad.

- QNX High Availability Framework permite tener máquinas de tiempo real QNX con alta disponibilidad de manera fácil.

- VMM library (Virtual Machine Manager library) es una librería de Microsoft con funciones de alta disponibilidad. Es un catálogo de recursos y se utilizan para crear y configurar máquinas virtuales.

**Ejercicio T2.3:
¿Cómo analizar el nivel de carga de cada uno de los subsistemas en el servidor?
Buscar herramientas y aprender a usarlas.**

Hay comandos el Linux que realizan esa función en la terminal:

- top: permite conocer en tiempo real la actividad del procesador y se pueden filtrar para ver que procesos tienen mayor carga de CPU.
- netstat: muestra un listado de las conexiones activas, tanto entrantes como salientes.
- vmstat: nos permite obtener un detalle general de procesos, E/S, uso de memoria, estado del sistema y actividad de la CPU. Detecta cuellos de botella, etc.

**Ejercicio T2.4:
Buscar ejemplos de balanceadores software y hardware (productos comerciales).
Buscar productos comerciales para servidores de aplicaciones.
Buscar productos comerciales para servidores de almacenamiento.**

Como balanceadores software hay algunos como:
- Cisco, tiene una gran variedad de balanceadores de carga.
- Nginx Plus
- Load Balancer ADC de Barracuda.
- Resonate

Productos comerciales para servidores de aplicaciones:
- Amazon
- Zope
- Internet Information Server

Procutos comerciales para servidores de almacenamiento:
- Dropbox Business
- Google Drive for Work
- One Drive