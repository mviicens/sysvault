___

En un Router, las Listas de Control de Acceso (ACL) se pueden aplicar en las interfaces para controlar el tráfico que entra o sale de la interfaz. Es importante entender cuándo utilizar la opción "in" o "out" al configurar una ACL en un puerto del Router. A continuación, se proporcionan ejemplos y explicaciones detalladas.

## ACL de Entrada *(in)*

Las ACL de entrada se aplican al tráfico que entra en la interfaz del Router. Se utilizan para filtrar el tráfico antes de que ingrese al Router desde dispositivos externos. A menudo, se utilizan para proteger la red interna del tráfico no deseado o malicioso proveniente del exterior.
### Ejemplo:

Supongamos que queremos aplicar una ACL extendida 101 en la interfaz GigabitEthernet0/1 del Router para permitir el tráfico TCP desde la red 192.168.1.0/24 hacia el servidor web con la dirección IP 203.0.113.10 en el puerto 80.

```
interface GigabitEthernet0/1
ip access-group 101 in
```

En este ejemplo:

- **GigabitEthernet0/1** es la interfaz en la que se aplicará la ACL.
- **ip access-group 101 in** aplica la ACL de entrada número 101 en la interfaz especificada.

Esta configuración permitirá el tráfico TCP desde la red 192.168.1.0/24 hacia el servidor web con la dirección IP 203.0.113.10 en el puerto 80 antes de que entre en el Router.

## ACL de Salida *(out)*

Las ACL de salida se aplican al tráfico que sale de la interfaz del Router. Se utilizan para filtrar el tráfico antes de que salga del Router hacia dispositivos externos. A menudo, se utilizan para controlar el tráfico que sale de la red interna y para aplicar políticas de seguridad en el tráfico saliente.
### Ejemplo:

Supongamos que queremos aplicar una ACL extendida 102 en la interfaz GigabitEthernet0/2 del Router para permitir el tráfico TCP desde el servidor web con la dirección IP 203.0.113.10 en el puerto 80 hacia la red 192.168.1.0/24.

```
interface GigabitEthernet0/2
ip access-group 102 out
```

En este ejemplo:

- **GigabitEthernet0/2** es la interfaz en la que se aplicará la ACL.
- **ip access-group 102 out** aplica la ACL de salida número 102 en la interfaz especificada.

Esta configuración permitirá el tráfico TCP desde el servidor web con la dirección IP 203.0.113.10 en el puerto 80 hacia la red 192.168.1.0/24 antes de que salga del Router.

## Conclusiones

- **ACL de Entrada (in):** Se utiliza para filtrar el tráfico que entra en el Router desde dispositivos externos.
- **ACL de Salida (out):** Se utiliza para filtrar el tráfico que sale del Router hacia dispositivos externos.

Es importante elegir cuidadosamente la dirección de la ACL ("in" o "out") según los requisitos de seguridad y las políticas de red para garantizar un control de tráfico efectivo y una implementación de seguridad adecuada en el Router.

#Router