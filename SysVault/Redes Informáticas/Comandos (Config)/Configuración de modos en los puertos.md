___
Este documento proporciona una guía completa sobre la configuración de diferentes modos en los puertos de un Switch, hay el modo **Access** y el modo **Trunk**.

- **Modo Access ->** El puerto en modo Access se utiliza para conectar dispositivos finales como computadoras, impresoras, y otros dispositivos de usuario final.

- **Modo Trunk ->** El puerto en modo Trunk se utiliza para conectar Switches entre sí o para conectar a dispositivos que necesitan entender múltiples VLANs, como los Routers.

### Puerto modo Access

> Modo de configuración: **Configure Terminal**

```
interface <tipu> <port>
switchport mode access
switchport access <vlan> <num_vlan>
```

### Puerto modo Trunk

> Modo de configuración: **Configure Terminal**

```
interface <tipu> <port>
switchport mode trunk
switchport trunk <modo> <vlan> <num_vlan>,<num_vlan> / <num_vlan - num_vlan>
```

> [!NOTE]
> En el apartado donde pone **modo**, tendréis que tener cuidado en si poner una **allowed** o **native**:
>
> - **allowed ->** Define un conjunto de VLANs que pueden pasar a través del enlace trunk. Las tramas de otras VLANs serán bloqueadas.
> 
> - **native ->** La nativa especifica a qué VLAN se asignarán las tramas que llegan sin etiquetar a través de un enlace trunk.
> 
> ***(Normalmente se utilizar mas el modo allowed)***

> [!CAUTION]
> Siempre ha de estar la **VLAN 1 incluida** en la configuración del Trunk.

**Anterior Documento:** [[Creación de VLAN en un Switch]]
**Siguiente Documento:** [[Configuración del Spanning Tree (STP)]]

#Basico #Redes #ASIX #Switch