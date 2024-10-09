____
En este documento se **explica** **que es** el protocolo STP y como **configurarlo**, aunque la mayoría de veces no es necesario configurarlo.

El **Spanning Tree Protocol *(STP)*** evita bucles en redes Ethernet seleccionando un *"switch raíz"* y bloqueando enlaces redundantes. Cada segmento de red tiene un *"puente designado"* que retransmite paquetes, mientras que los puertos redundantes se bloquean para **garantizar la** **estabilidad** y **eficiencia** de la red.
### Cambiar el coste de la interfaz

Este comando se utiliza para cambiar el coste de una interfaz en el protocolo **STP** *(Spanning Tree Protocol)*. El valor especificado representa el nuevo coste de la interfaz.

> Modo de configuración: **Configure terminal**

```
spanning-tree cost <valor>
```

### Obligar a ser switch raíz

Este comando se utiliza para forzar al switch a convertirse en el switch raíz para la VLAN especificada. El switch enviará mensajes de Bridge Protocol Data Unit (BPDU) con la prioridad más baja posible para asegurar que sea elegido como el switch raíz.

> Modo de configuración: **Configure terminal**

```
spanning-tree vlan <id_vlan> root primary
```

### Raíz alternativa

Este comando se utiliza para designar al switch como raíz alternativa para la VLAN especificada. Si el switch raíz falla, el switch configurado como raíz secundaria tomará su lugar como switch raíz para esa VLAN.

> Modo de configuración: **Configure terminal**

```
spanning-tree vlan <id_vlan> root secondary
```

**Anterior Documento:** [[Configuración de modos en los puertos]]
**Siguiente Documento:** [[Configuraciones de Seguridad en un Switch]]

#Intermedio #Redes #ASIX #Switch