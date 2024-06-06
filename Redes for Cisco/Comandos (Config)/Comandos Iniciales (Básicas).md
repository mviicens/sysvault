________
Básicamente, aquí enseña como poner un **Nombre** al *Router/Switch*, la comanda para que no haga ping a dominios que no existen o que no tienen conexión entre otros comandos básicos i esenciales.
### Implementación de un nombre a un dispositivo de Red

> Modo de configuración: **Configure Terminal**

```
hostname <nom>
```

### Quitar la comprobación de Dominios

> Modo de configuración: **Configure Terminal**

```
no ip domain lookup
```

### Guardar la configuración del *Router/Switch*

> Modo de configuración: **Enable**

```
copy running-config startup-config
```

### Asignar una IP a una Interficie/Vlan

> Modo de configuración: **Configure Terminal**

```
interface <tipo-puerto>
ip address <ip> <mascara>
no shutdown
```

> [!NOTE]
> Hay diferentes tipos de puertos, estos son los que hemos tocado en el ciclo *(también son los mas frecuentes)*:
> - **Serial -->** *serial 0/0/0*
> - **Fast -->** *FastEthernet 0/0*
> - **Giga -->** *GigaEthernet 0/0*

____
**Anterior Documento:** [[Redes Informáticas (Según Cisco)]]
**Siguiente Documento:**  [[Activación de Contraseñas en Dispositivos de Red]]

#Basico