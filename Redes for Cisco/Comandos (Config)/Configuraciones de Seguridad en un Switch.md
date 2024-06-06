___
En este documento se enseña la configuración de la seguridad en un Switch, que básicamente se basa en las restricciones que se pueden aplicar a los puertos mediante un filtro de direcciones MAC.

> Modo de configuración: **Configure Terminal**

```
interface <tipo> <port>
switchport port-security
switchport port-security mac-address sticky
switchport port-security maximum <num>
switchport port-security violation <tipo-proteccion>
switchport port-security mac-address <mac>
```

> [!NOTE]
> Aquí hay una leyenda sobre el `<tipo-proteccion>`:
> - **restrict -->** Permite el tráfico de dispositivos autorizados, pero registra una violación de seguridad.
> - **protect -->** Descarta el tráfico de dispositivos no autorizados sin registrar una violación.
> - **shutdown -->** Apaga el puerto en caso de violación de seguridad.

**Anterior Documento:**  [[Configuración del Spanning Tree (STP)]]

#Switch