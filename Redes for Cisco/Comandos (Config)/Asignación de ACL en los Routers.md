___
## 1. ACL Simples

Las **Listas de Control de Acceso *(ACL)* simples** son filtros de paquetes básicos que se aplican a interfaces de red para permitir o denegar el paso de tráfico basado únicamente en la dirección IP de origen. El numero asignación de las ACL Simples son **del 1-99.**

**Función:** Permiten o deniegan el tráfico en función de la dirección IP de origen.

**Configuración:** Se aplican en interfaces de entrada o salida y se pueden configurar para permitir o denegar el tráfico de acuerdo con una dirección IP específica o un rango de direcciones IP.

**Ejemplo de ACL Simple:**

```
access-list 1 permit icmp 192.168.1.0 0.0.0.255 any
```

- **1** es el número de la lista de acceso.
- **permit** indica que se permitirá el tráfico.
- **icmp** especifica el protocolo ICMP.
- **192.168.1.0** es la dirección IP de origen.
- **0.0.0.255** es la máscara de subred que coincide con cualquier dirección IP de la red 192.168.1.0/24.
- **any** indica que el tráfico puede ir hacia cualquier destino fuera de la red local.

## 2. ACL Extendida

Las **Listas de Control de Acceso (ACL) extendidas** proporcionan un **mayor nivel de control** y **flexibilidad en comparación** con las ACL simples, ya que permiten filtrar el tráfico basado en múltiples criterios, como direcciones IP, protocolos, puertos, etc. El numero asignación de las ACL Extendidas son **del 100 - 199**.

**Función:** Permiten o deniegan el tráfico en función de criterios más específicos, como direcciones IP, protocolos, puertos, etc.

**Configuración:** Se aplican en interfaces de entrada o salida y se pueden configurar para permitir o denegar el tráfico en base a una amplia gama de criterios.

**Ejemplo de ACL Extendida:**

```
access-list 102 permit tcp 192.168.1.0 0.0.0.255 host 203.0.113.10 eq 80
```

- **102** es el número de la lista de acceso.
- **permit** indica que se permitirá el tráfico.
- **tcp** especifica el protocolo TCP.
- **192.168.1.0** es la dirección IP de origen.
- **0.0.0.255** es la máscara de subred que coincide con cualquier dirección IP de la red 192.168.1.0/24.
- **host 203.0.113.10** especifica la dirección IP de destino.
- **eq 80** especifica que el tráfico debe ser dirigido al puerto 80 del servidor web *(http)*.

## 3. Asignación a los puertos

Las **Listas de Control de Acceso (ACL)** se deben aplicar en los **puertos del Router** para controlar el tráfico de red que **entra** o **sale** de una interfaz específica. 

### Cuándo usar *"in"* o *"out"*

- **in ->** Se aplica a tráfico entrante en la interfaz. Es útil para filtrar el tráfico antes de que ingrese al Router, por lo que se utiliza para controlar el tráfico que entra en la red desde dispositivos externos.
- **out ->** Se aplica a tráfico saliente de la interfaz. Es útil para filtrar el tráfico antes de que salga del Router, por lo que se utiliza para controlar el tráfico que sale de la red hacia dispositivos externos.

**Ejemplo de la Asignación:**

Supongamos que queremos aplicar una ACL extendida 101 en la interfaz GigabitEthernet0/1 del Router para permitir el tráfico TCP desde la red 192.168.1.0/24 hacia el servidor web con la dirección IP 203.0.113.10 en el puerto 80. Aquí está la configuración:

```
interface GigabitEthernet0/1
ip access-group 101 in
```

En este ejemplo:

- **GigabitEthernet0/1** es la interfaz en la que se aplicará la ACL.
- **ip access-group 101 in** aplica la ACL de entrada número 101 en la interfaz especificada.

Si quieres una explicación mas detallada, ve al **siguiente documento**: [[Cuando es In o Out (ACL)]]

## 4. Configuración de ACL

### Configuración ACL Simple

> Modo de configuración: **Configure Terminal**

```
access-list <num> permit/deny <direccion_origen> <wildcard>
```

> [!NOTE]
> - **num:** Número de la lista de acceso.
> - **permit/deny:** Acción a realizar sobre el tráfico que coincide con la regla.
> - **direccion_origen:** Dirección IP de origen o rango de direcciones IP.
> - **wildcard:** Máscara de bits que especifica qué parte de la dirección IP es de interés.

### Configuración ACL Extendida

> Modo de configuración: **Configure Terminal**

```
access-list <num> permit/deny <protocolo> <direccion_origen> <wildcard_origen> <direccion_destino> <wildcard_destino> <puerto_origen> <puerto_destino>
```

> [!NOTE]
> - **num:** Número de la lista de acceso.
> - **permit/deny:** Acción a realizar sobre el tráfico que coincide con la regla.
> - **protocolo:** Protocolo sobre el cual se aplica la regla *(tcp, udp, icmp, etc)*.
> - **dirección_origen:** Dirección IP de origen o rango de direcciones IP.
> - **wildcard_origen:** Máscara de bits que especifica qué parte de la dirección IP de origen es de interés.
> - **dirección_destino:** Dirección IP de destino o rango de direcciones IP.
> -  **wildcard_destino:** Máscara de bits que especifica qué parte de la dirección IP de destino es de interés.
> - **puerto_origen:** Puerto de origen (solo en ACL extendidas).
> - **puerto_destino:** Puerto de destino (solo en ACL extendidas).

### Aplicar la ACL en una Interficie

> Modo de configuración: **Configure Terminal**

```
interface <tipo-puerto>
ip access-group <num-acl> in/out
```

> [!IMPORTANT]
> Para poder comprobar que funciona, puedes utilizar las suiguientes comandas: 
> `show access-lists`
> `show access-list <num-acl>`

**Anterior Documento:** [[Configuración de DHCP en un Router]]
**Siguiente Documento:**  [[Configuración del NAT en el Router]]

#Router