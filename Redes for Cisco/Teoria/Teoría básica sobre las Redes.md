____
## 1. Introducción a las Redes

Una red informática es un conjunto de equipos conectados entre sí, que comparten recursos e información. Estos equipos pueden ser ordenadores, servidores, impresoras, etc. Las redes pueden clasificarse según su tamaño en los siguientes tipos:

- **Redes de Área Local (LAN)**: Son limitadas a una zona geográfica pequeña, como una oficina. Permiten la conexión de dispositivos cercanos para compartir recursos como archivos e impresoras.

- **Redes de Área Metropolitana (MAN)**: Abarcan una ciudad. Conectan varias redes locales para permitir la comunicación y el intercambio de datos entre ellas.

- **Redes de Área Extensa (WAN)**: Pueden cubrir grandes distancias, incluso países o continentes. Conectan múltiples redes locales y metropolitanas, permitiendo la comunicación global.

## 2. Sistemas de Numeración

Los sistemas de numeración en redes se refieren a la forma en que se representan las direcciones y los datos. Las direcciones IP, por ejemplo, se representan en notación decimal con puntos, como 192.168.0.1, que es una representación más amigable que la notación binaria equivalente. Además, existen direcciones públicas y privadas, siendo las privadas aquellas utilizadas dentro de una red local y no accesibles directamente desde Internet.

## 3. Protocolos y Modelos

Un protocolo de comunicación es un conjunto de reglas que permite la transferencia de datos entre dispositivos. Los protocolos más conocidos son TCP/IP, que permiten la comunicación en Internet. Los modelos de referencia, como el modelo OSI, estructuran la comunicación en capas, cada una con funciones específicas. El modelo OSI tiene siete capas: física, de enlace de datos, de red, de transporte, de sesión, de presentación y de aplicación. TCP/IP, en cambio, tiene cuatro capas: acceso a la red, Internet, transporte y aplicación.

## 4. Capa Física (OSI) y Acceso de Red (TCP/IP)

### Modelo OSI

El modelo OSI (Interconexión de Sistemas Abiertos) es un modelo de referencia que describe cómo los datos se transmiten y reciben en una red. Tiene siete capas, cada una con funciones específicas:

1. **Capa Física**: Se encarga de la transmisión de bits a través de un medio físico, como cables o fibra óptica. Incluye aspectos como las características eléctricas, mecánicas y de procedimiento para acceder a medios físicos.

2. **Capa de Enlace de Datos**: Proporciona la transferencia fiable de datos a través de un enlace físico. Gestiona errores en la capa física y controla el flujo de datos.

3. **Capa de Red**: Se encarga de la determinación de rutas y el encaminamiento de los datos entre dispositivos de una red, utilizando direcciones lógicas como las direcciones IP.

4. **Capa de Transporte**: Garantiza la transferencia de datos de extremo a extremo de manera fiable. Controla la segmentación de datos y la gestión de errores y flujo.

5. **Capa de Sesión**: Gestiona y controla las conexiones (sesiones) entre dos dispositivos. Establece, mantiene y termina sesiones de comunicación.

6. **Capa de Presentación**: Traduce, convierte y asegura los datos para la capa de aplicación. Gestiona la codificación y la compresión de datos.

7. **Capa de Aplicación**: Proporciona servicios de red a las aplicaciones del usuario. Incluye protocolos como HTTP, FTP, SMTP, entre otros.

### Modelo TCP/IP

El modelo TCP/IP (Protocolo de Control de Transmisión/Protocolo de Internet) es el conjunto de protocolos utilizados para la comunicación en Internet y otras redes. Tiene cuatro capas:

1. **Capa de Acceso a la Red**: Combina las funciones de las capas física y de enlace de datos del modelo OSI. Maneja tanto la transmisión de datos como el acceso al medio físico, incluyendo hardware y software necesarios para la transmisión.

2. **Capa de Internet**: Responsable de la dirección y encaminamiento de los paquetes de datos. Incluye el Protocolo de Internet (IP), que se encarga de entregar los paquetes a la dirección correcta.

3. **Capa de Transporte**: Asegura la transferencia fiable de datos de extremo a extremo. Incluye el Protocolo de Control de Transmisión (TCP), que garantiza la entrega fiable, y el Protocolo de Datagramas de Usuario (UDP), que permite la transmisión de datos sin garantía de entrega.

4. **Capa de Aplicación**: Proporciona servicios de red a las aplicaciones del usuario. Incluye protocolos de alto nivel como HTTP, FTP, SMTP, y otros.

En resumen, ambos modelos estructuran la comunicación en capas, aunque el modelo OSI es más teórico y detallado con siete capas, mientras que el modelo TCP/IP es más práctico y ampliamente utilizado en la actualidad con cuatro capas.

## 5. ARP e IP

El Protocolo de Resolución de Direcciones (ARP) se utiliza para mapear direcciones IP a direcciones MAC (físicas). Cuando un dispositivo quiere comunicarse con otro dentro de la misma red, usa ARP para encontrar la dirección MAC correspondiente a una dirección IP dada. IP (Protocolo de Internet) se encarga de dirigir los paquetes de datos desde el origen hasta el destino a través de distintas redes interconectadas.

## 6. Direccionamiento IP

El direccionamiento IP es fundamental para identificar dispositivos en una red. Una dirección IP se compone de dos partes: una parte de red y una parte de host. La máscara de subred se utiliza para distinguir estas dos partes. Las direcciones IP pueden ser estáticas (fijas) o dinámicas (asignadas temporalmente por un servidor DHCP). Las direcciones IP privadas son utilizadas para redes internas y no son accesibles desde Internet, mientras que las direcciones IP públicas son únicas en toda la red global de Internet.

## 7. Capa Internet

La capa de Internet del modelo TCP/IP es responsable de la dirección y encaminamiento de los paquetes de datos. Incluye protocolos como IP, ICMP (Protocolo de Mensajes de Control de Internet) y ARP. IP se encarga de entregar los paquetes de datos a la dirección correcta, mientras que ICMP se utiliza para enviar mensajes de error y control. ARP, como se mencionó, traduce direcciones IP a direcciones MAC.

**Inicio:** [[Redes Informáticas (Según Cisco)]]

#Teorico
