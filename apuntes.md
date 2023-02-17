# XC

Profesor: Llorenç Cerdà-Alabern
llorenc@ac.upc.edu

## Introducción

Nos centramoh en el Interneh

Ha dicho más cosas pero me da pereza apuntar

### Palabras importantes

bitrate: bits por segundo que se envían (característico de la línea de
transmisión de datos)

throughput: bits por segundo que se observan por la aplicación (valor esperado
del programa)

packet switching: la transmisión de datos no se envía toda conjunta si no que
se transmite en paquetes de datos que pueden tener errores, de forma que en
caso de que hayan el paquete se retransmite. En Internet muchos paquetes tienen
que desaparecer por congestión de la red.

Virtual circuit: **mirar apuntes**

En el primer paquete de transmisión está la información de
destino, de forma que la red gestiona el mejor camino que tienen que recorrer
los paquetes para llegar al destino.

### Estandarización

#### OSI

Estándar desarrollado por ISO que define las redes de computadores a patir de
un sistema de capas. A partir de determinados protocolos se permite la
interacción entre entidades de la misma capa.

- Physical: cableado y todo esperado
- Data link: interfaces
- Network: distintas redes
- Transport: crea los paquetes, gestiona que todos lleguen en el orden que
  deben y manteniéndose cómo deben ser
- Session: identifica a los usuarios que se conectan al servidor
- Presentation: las diferentes aplicaciones que funcionan dentro del mismo
  dispositivo y se encarga de representar esta información de los diferentes
  programas
- Application: cada aplicación que usa la red

#### TCP/IP

Se basa en el protocolo IP para transportar paquetes en la red en la capa de
red y en la de transporte se usa TCP o UDP.

##### Encapusulación de la información

Cada mensaje de una capa se envía a través de la capa inferior con ciertos
headers:

```
                                  |---------------|---------------|   (mensaje)
                                 /---------------/
                       |TCP head|---------------|                (segmento TCP)
               |IP head|------------------------|                (datagrama IP)
 |Ethernet head|--------------------------------|CRC|       (frame de ethernet)
 (cosas en binario)                                                      (bits)
```

El CRC sirve para comprobar que el dato esté bien enviado

### UDP

### TCP

**Mirar esto del libro**

## IP

Protocolo de Internet.

El protocolo se basa en un host que es el servidor, routers que ejecutan el
protocolo. Estos se encargan de crear y transferir los datagramas hasta el
cliente final que debe recibir el paquete.

Hay diferentes protocolos para usar IP: X25
