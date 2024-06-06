____
Este apartado se centra en la configuración de una **IP en el Switch**, cómo asignar **nombres a las VLANs** y asignarle un gateway al Switch.

### Configuración de una IP a un Switch

> Modo de configuración: **Configure Terminal**

```
interface <vlan> <num_vlan>
ip address <ip> <mascara>
no shutdown
```

> [!CAUTION]
> En el switch las IPs se ponen en las **VLAN**, **NO** en los **PUERTOS**.

### Asignar un nombre a una VLAN

> Modo de configuración: **Configure Terminal (VLAN)**

```
name <nom>
```

### Configuración en un rango de Puertos

> Modo de configuración: **Configure Terminal**

```
interface range <tipu> <port-port>
```

### Configuración de un Gateway al Switch

> Modo de configuración: **Configure Terminal**

```
ip default-gateway <ip>
```

**Anterior Documento:** [[Visualización de Configuraciones]]
**Siguiente Documento:** [[Configuración de modos en los puertos]]

#Switch