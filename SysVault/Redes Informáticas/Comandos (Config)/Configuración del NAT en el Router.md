___
En este documento se explica cómo **activar** y **configurar** NAT (Network Address Translation) y PAT (Port Address Translation) en los dispositivos de red.

### Creación de ACL para el NAT-PAT

> Modo de configuración: **Configure Terminal**

```
access-list <num> permit <direccion_origen> <wildcard>
```

> [!NOTE]
> Es importante que la ACL Simple que creemos sea un rango sobre las IPs que queremos que el Router traduzca con el NAT.

### Configuración de la NAT-PAT

> Modo de configuración: **Configure Terminal**

```
ip nat inside source list <num-acl-permesa> interface <puerto> overload
```

### Asignación de puertos

> Modo de configuración: **Configure Terminal (Puerto)**

```
ip nat inside 
ip nat outside
```

> [!WARNING]
> **inside ->** Configurar el puerto donde se aplicará la NAT a la red.
> **outside ->** Configurar el puerto donde se encuentra la WAN: la dirección IP de todos será la del puerto en el que se aplique en el router.

> [!IMPORTANT]
> Para poder comprobar que funciona, puedes utilizar las suiguientes comandas: 
> `show ipnat translations`
> `show ipnat statistics`

**Anterior Documento:** [[Asignación de ACL en los Routers]]

#Intermedio #Redes #ASIX #Router