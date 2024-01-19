# Blue Team

## Filter Captures in Wireshark

- Wireshark es un potente analizador de protocolos de red.
- Permite capturar e inspeccionar los datos que viajan de un lado a otro en una red.
- Para filtrar capturas en Wireshark y obtener información muy detallada, puedes utilizar filtros de visualización.
- Estos filtros te ayudarán a centrarte en paquetes específicos o tipos de tráfico.
- Capturar solo los paquetes relevantes, conservando el espacio en disco y el tiempo de análisis.
- **Filtros de visualización comunes**
  + `ip.addr == X.X.X.X`: Este filtro muestra paquetes con una dirección IP de origen o destino de X.X.X.X.
  + `tcp.port == 80`: Muestra paquetes con un puerto de origen o destino de 80 (HTTP).
  + `dns`: Muestra solo el tráfico DNS.
  + `http`: Muestra solo el tráfico HTTP.
  + `frame.number <= 100`: Limita la visualización a los primeros 100 frames capturados.
- Puedes utilizar operadores lógicos (and, or, not) para combinar múltiples condiciones.

## Process Monitor (ProcMon)

- Es una herramienta que se utiliza para supervisar el sistema de archivos, el registro y la actividad en tiempo real.
- Herramienta poderosa para solucionar problemas, diagnosticar problemas y detectar malware.
- Captura una amplia gama de eventos, incluyendo accesos al sistema de archivos, cambios en el registro, creación y finalización de procesos y subprocesos.
- Utilizar ProcMon para capturar datos mientras se ejecuta un programa sospechoso.
- ProcMon también puede utilizarse para identificar las técnicas que utilizan los malware para propagarse o evadir la detección.
- ProcMon facilita la detección de comportamientos maliciosos, como la modificación no autorizada de archivos, la manipulación del registro del sistema o la comunicación sospechosa a través de la red.
- Sirve como una herramienta invaluable en el análisis forense de sistemas comprometidos.

<p align="center">
  <img src="https://learn.microsoft.com/en-us/sysinternals/downloads/media/procmon/procmon-main.png"/>
</p>

## Windows Registry Introduction and Structure

## Recycle Bin Forensic and Rifiuti2 Tool

## Introduction to Prefetch Files

## Introduction to Sysmon Sysinternals

## Introduction to Autopsy

## Introduction to Memory Forensics

## Memory Forensics using Volatility - Volatility - Registry and Network Connections
