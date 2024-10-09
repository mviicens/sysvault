________
En este documento se explica cómo **configurar** los protocolos de enrutamiento ***RIP***, ***RIPv2*** y ***OSPF*** en dispositivos de red. El enrutamiento es el proceso de seleccionar caminos en una red para enviar datos desde un origen a un destino, en este documento explicaremos el **enrutamiento** **dinámico** como el **estático**.

## 1. Enrutamiento Dinámico
___
### Configuración con RIP

> Modo de configuración: **Configure Terminal**

```
router rip
network <nom_xarxa>
```

> [!CAUTION]
> El protocolo RIP *(versión 1)*, **NO** tiene en cuenta les máscaras de red. El formato de la IP, `<nom_xarxa>`, ha de ser como la siguiente:
> - **Ejemplo 1 -->** *192.168.1.0*
> - **Ejemplo 2 -->** *10.0.0.0*

### Configuración con RIPv2

> Modo de configuración: **Configure Terminal**

```
router rip
version 2
network <nom_xarxa>
```

> [!CAUTION]
> El protocolo RIP versión 2, **SI** té en cuenta las máscaras de red. El formato de la IP, `<nom_xarxa>`, ha de ser como la seguiente:
> - **Exemple 1 -->** *192.168.2.0*
> - **Exemple 2 -->** *12.0.0.0*

### Configuración con OSPF

> Modo de configuración: **Configure Terminal**

```
router ospf <num>
network <nom_xarxa> <wildcard> area <num-area>
```

## 2. Enrutamiento Estático
___
### Configuración con enrutamiento estático:

> Modo de configuración: **Configure Terminal**

```
ip route <nom_xarxa> <mascara> <desti>
```

> [!NOTE]
> Per aclar una mica el enrutament estàtic, teniu la següent llegenda:
> **nom_xarxa ->** El nom de la xarxa que volem trobar.
> **mascara ->** La màscara de la xarxa que busquem.
> **desti ->** Per on ha da pasar el router per trobar la xarxa desti *(Ha de sert la IP del següent salt, ho sigui que un Router conectat directament al nostre Router)*.

**Anterior Documento:** [[Visualización de Configuraciones]]
**Siguiente Documento:** [[Configuración de subpuertos en un Router]]

#Basico #Redes #ASIX #Router