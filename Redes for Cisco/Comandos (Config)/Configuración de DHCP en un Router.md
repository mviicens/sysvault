___
En este documento explicamos la configuración **DHCP**, que sirve para que el Router asigne IPs de forma automática a su respectiva red, también se pueden configurar algunos parámetros en concreto, como IPs que no quieras incluir en tus rangos.

### Creación de una Pool DHCP

> Modo de configuración: **Configure Terminal**

```
ip dhcp pool <nom_rang>
network <nom_xarxa> <mascara>
default-router <ip_gateway>
dns-server <ip_dns>
domain-name <domini>
```

### IPs Reservadas / IPs Excluidas

> Modo de configuración: **Configure Terminal (DHCP)**

```
ip dhcp excluded-address <ip>
ip dhcp excluded-address <primera_ip> <ultima_ip>
```

>[!TIP]
>Este comando se puede utilizar con una **IP en concreto** *(primer comando)* o también puedes aplicarlo en **un rango** *(segundo comando)*.

**Anterior Documento:**  [[Configuración de subpuertos en un Router]]
**Siguiente Documento:** [[Asignación de ACL en los Routers]]

#Router
