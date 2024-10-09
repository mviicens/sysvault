________
En este documento se enseñan los comandos para poder **ver** i **previsualizar** las configuraciones que estamos haciendo o que ya venían configuradas en el *Router/Switch*.

### Visualizar la configuración *(Actual)*

> Modo de configuración: **Enable**

```
show running-config
```

### Visualizar la configuración *(Con la que arranca)*

> Modo de configuración: **Enable**

```
show startup-config
```

### Visualizar la tabla de Enrutamiento

> Modo de configuración: **Enable**

```
show ip route
```

> [!NOTE]
> Al proyectarse la tabla saldrán unas **letras** al lado de las **IP visibles por el Router**, cada una tienen su **respectivo significado** i esta es la forma correcta de interpretarlo:
> - **C -->** Interficie directament conectada.
> - **S -->** Ruta estàtica.
> - **S * -->** Ruta estàtica per defecte.

### Visualizar el estado de les Interficies

> Modo de configuración: **Enable**

```
show ip interface brief
```

### Visualizar la configuración de los dispositivos que están directamente conectados al Router

> Modo de configuración: **Enable**

```
show cdp neighbors detail
```

### Visualizar la lista de IPs proporcionadas con les MACs *(DHCP)*

> Modo de configuración: **Enable**

```
show ip dhcp binding
```

> [!TIP]
> Otra comando que puede ser útil es: `show ip dhcp server statistics`. 
> Lo que hace es mostrar información relacionada con el número de mensajes DHCPv4 que se han enviado y recibido.

### Visualizar la tabla de MACs

> Modo de configuración: **Enable**

```
show mac-address-table
```

### Ver historial de comandos utilizados

> Modo de configuración: **Enable**

```
show history
```

### Comprobar el estado i configuración de las VLANs

> Modo de configuración: **Enable**

```
show vlan brief
```

### Visualizar la configuración del Spanning Tree *(STP)*

> Modo de configuración: **Enable**

```
show spanning-tree 
show spanning-tree detail
```

### Visualizar matches de ACL

> Modo de configuración: **Enable**

```
show access-lists
show access-list <num-acl>
```

### Comprobación del funcionamiento de NAT-PAT 

> Modo de configuración: **Enable**

```
show ipnat translations
show ipnat statistics
```

**Anterior Documento:**  [[Activación de Contraseñas en Dispositivos de Red]]
**Inicio de Routers:** [[Configuración del Enrutamiento Dinámico i Estático]]
**Inicio de Switches:** [[Creación de VLAN en un Switch]]

#Basico #View #Redes #ASIX #Router #Switch 