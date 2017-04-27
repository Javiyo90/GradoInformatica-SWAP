**TEMA 6: Asegurar el sistema web**


**Ejercicio T6.1:
Aplicar con iptables una política de denegar todo el tráfico en una de las máquinas de prácticas.
Comprobar el funcionamiento.
Aplicar con iptables una política de permitir todo el tráfico en una de las máquinas de prácticas.**

Siguiendo las diapositivas de clase vamos a realizar las diferentes políticas:

DENEGAR TODO EL TRÁFICO
iptable -F
iptables -P INPUT DROP
iptables -P OUTPUT DROP
iptables -P FORWARD DROP

PERMITIR TODO EL TRÁFICO
iptables -F
iptables -I INPUT -j ACCEPT


**Ejercicio T6.2:
Comprobar qué puertos tienen abiertos nuestras máquinas, su estado, y qué programa o demonio lo ocupa.**

Con la herramienta nmap obtengo la siguiente salida:

```
Starting Nmap 6.40 ( http://nmap.org ) at 2017-04-27 17:33 CEST
Nmap scan report for localhost (127.0.0.1)
Host is up (0.013s latency).
Not shown: 999 filtered ports
PORT   STATE SERVICE
22/tcp open  ssh

Nmap done: 1 IP address (1 host up) scanned in 5.73 seconds
```

Se observa que esta máquina sigue con diferentes reglas de iptables establecidas anteriormente y solo admite peticiones ssh.

**Ejercicio T6.3:
Buscar información acerca de los tipos de ataques más comunes en servidores web (p.ej. secuestros de sesión).
Detallar en qué consisten, y cómo se pueden evitar.**

Los más comunes han sido comentados en clase. Serían los siguientes:

- DDos: Ataque de denegación de servicio distribuido. El usuario maligno inicia peticiones, recibe la respuesta y no confirma que recibe la respuesta. La reserva de recursos en el servidor hace que se sobrecargue y se caiga el servicio. Es imposible de evitar el ataque pero si se puede combatir intentando reducir el tamaño de los paquetes transferidos por el servidor para ofrecer el servicio y que el servidor tenga tiempos de espera para rechazar una conexión que no se ha realizado.
- SQL Injection: Es un ataque al servidor de base de datos que se produce por la inyección de un código creado por el atacante al propio código fuente de la base de datos. La causa suele ser la mala filtración de las variables de manera que realizando un código seguro que no se pueda ver, el problema quedaría resuelto.
