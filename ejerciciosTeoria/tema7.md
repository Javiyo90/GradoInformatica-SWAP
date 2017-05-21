**TEMA 7: Almacenamiento de datos**


**Ejercicio T7.1:
¿Qué tamaño de unidad de unidad RAID se obtendrá al configurar un RAID 0 a partir de dos discos de 100 GB y 100 GB?**
Puesto que no se trata de redundancia de datos, el tamaño es 200 GB.

**
¿Qué tamaño de unidad de unidad RAID se obtendrá al configurar un RAID 0 a partir de tres discos de 200 GB cada uno?**

600 GB, como anteriormente he mencionado, no hay redundancia por tanto solo hay que sumar las capacidades de los discos en RAID.


**Ejercicio T7.2:
¿Qué tamaño de unidad de unidad RAID se obtendrá al configurar un RAID 1 a partir de dos discos de 100 GB y 100 GB?**

Ya que RAID 1 es un disco espejo, la capacidad sería 100 GB. 

**
¿Qué tamaño de unidad de unidad RAID se obtendrá al configurar un RAID 1 a partir de tres discos de 200 GB cada uno?**

La capacidad total sería 200 GB puesto que son discos espejo.


**Ejercicio T7.4:
Buscar información sobre los sistemas de ficheros en red más utilizados en la actualidad y comparar sus características. Hacer una lista de ventajas e inconvenientes de todos ellos, así como grandes sistemas en los que se utilicen.**

Los más comunes son:

- SMB: Samba es una implementación libre del protocolo de archivos compartidos de Microsoft Windows para sistemas UNIX. Permite validad usuarios haciendo de Controlador Principal de Dominio, como miembro de dominio e incluso como un dominio Active Directory para reder en Windows.
- NFS: Está introducido por defecto en los sistemas UNIX y la mayoría de distribuciones Linux. Hay tres versiones en uso actualmente.
-- NFSv2: La más antigua y está ampliamente soportada por muchos sistemas operativos.
-- NFSv3: Incluye manejos de archivos de tamaño variable y mejores facilidades de informes de errores.
-- NFSv4: Incluye seguridad Kerberos, trabaja con cortafuegos,permite ACLs y utiliza operaciones con descripción del estado.
- AFP: Es el principal protocolo para los servicios de archivo de Mac OS.