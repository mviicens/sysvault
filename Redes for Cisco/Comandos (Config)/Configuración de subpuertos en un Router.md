________
Este apartado es para explicar la configuración de **Subpuertos**, que nos es muy útil para no decir que es esencial cuando tenemos que configurar **VLANs**.

> Modo de configuración: **Configure Terminal**

```
interface <tipo> <puerto>.<subpuerto> 
encapsulation dot1q <num> 
no shutdown
```

> [!CAUTION]
> Es importante hacer un `no shutdown` al **puerto principal**.

**Anterior Documento:**  [[Configuración del Enrutamiento Dinámico i Estático]]
**Siguiente Documento:** [[Configuración de DHCP en un Router]]

#Router