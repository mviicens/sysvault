________
En este documento se explica como **activar** i **configurar** los Dispositivos de Red, también se enseña a como activar la conexión vía **SSH** i **Telnet**.

### Configuración de contraseña para acceder al *Router/Switch*

> Modo de configuración: **Configure Terminal**

```
enable password <contrasenya>
line console 0
password <contrasenya>
login
```

### Configuración para encriptar la contraseña en modo *"Enable"*

> Modo de configuración: **Configure Terminal**

```
enable secret <contrasenya>
```

### Activación i configuración de contraseña del Telnet en un *Router/Switch*

> Modo de configuración: **Configure Terminal**

```
line vty 0 4
password <contrasenya>
login
```

### Activación i configuración de contraseña del **SSH** en un *Router/Switch*

> Mode de configuració: **Configure Terminal**

```
ip domain-name <domini>
crypto key generate rsa

ip ssh version 2
ip ssh time-out 60
ip ssh authentication-retries 2
line vty 0 4
transport input SSH
```

> [!CAUTION]
> Antes de realizar esta configuración, necesitas que el dispositivo tenga el **Hostname** y el **Telnet** previamente configurados.
> También, en caso de no tener el dominio, puedes utilizar este: **rto.cisco.com**

**Anterior Documento:** [[Comandos Iniciales (Básicas)]]
**Siguiente Documento:** [[Visualización de Configuraciones]]

#Basico #Redes #ASIX #Router #Switch 