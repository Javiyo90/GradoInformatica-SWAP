**TEMA 3: La red de una granja web**


**Ejercicio T3.1:
Buscar con qué órdenes de terminal o herramientas gráficas
podemos configurar bajo Windows y bajo Linux el
enrutamiento del tráfico de un servidor para pasar el
tráfico desde una subred a otra.**

- Bajo Linux tenemos varios comandos:
	- iptables. Ej:
```
iptables -A FORWARD -j ACCEPT
iptables -t nat -A POSTROUTING -s 10.0.0.0/8 -o eth0 -j MASQUERADE
```

	- route. Ej:
```
route add -net 169.255.0.0/16 gw 192.168.1.1 dev eth0
```

- En Windows tenemos el comando route que es el más efectivo y simple para configurar el enrutamiento de subredes.

**Ejercicio T3.2:
Buscar con qué órdenes de terminal o herramientas gráficas
podemos configurar bajo Windows y bajo Linux el filtrado
y bloqueo de paquetes.**

- En Linux podemos utilizar la herramienta iptables que nos permite filtrar paquetes provenientes de un ping, ftp, ssh o peticiones http/https.

- En Windows podemos configurar el Firewall para filtrar y bloquear paquetes.