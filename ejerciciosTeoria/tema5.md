**TEMA 5: Medir Prestaciones**


**Ejercicio T5.1:
Buscar información sobre cómo calcular el número de conexiones por segundo.**

En apache podemos verlo realizando apache2ctl status | grep request
Con netstat podemos comprobar cuantas conexiones tenemos en un momento dado de forma que podemos realizar un pequeño script que calcule el número de conexiones en el tiempo deseado.

**Ejercicio T5.2:
Revisar los análisis de tráfico que se ofrecen en:
http://bit.ly/1g0dkKj
Instalar wireshark y observar cómo fluye el tráfico de red en uno de los servidores web mientras se le hacen peticiones HTTP.**

Una vez instalado con apt-get install wireshark, al hacer capture se puede observar como se ve el diferente tráfico.
Un ejemplo de tráfico es: 

```
dst port 80 or dst port 80...
```

**Ejercicio T5.3:
Buscar información sobre características, disponibilidad para diversos SO, etc de herramientas para monitorizar las prestaciones de un servidor.
Para empezar, podemos comenzar utilizando las clásicas de Linux:
- top
- vmstat
- netstat
**

La herramienta más conocida encontrada por internet es netdata. Está escrito en C y muestra en tiempo real gran detalle las métricas del sistema Linux. Lo más importante es que controla servidores de squid, nfs, postfix, nginx, mysql,... y muchos más.

