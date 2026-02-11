# Cibersecurity_Proyects

Este repositorio contiene un conjunto de herramientas desarrolladas en **Bash Scripting** diseñadas para la automatización de tareas de reconocimiento y defensa activa. El proyecto fue realizado como Producto Integrador de Aprendizaje (PIA) para la carrera de LSTI en la UANL.

🛠️ Herramientas Incluidas

1. PortScan.sh 
Este script permite realizar un reconocimiento detallado de una infraestructura de red mediante una metodología de doble validación.

* Metodología: Utiliza `nmap` para el escaneo masivo inicial y valida los puertos abiertos mediante `netcat` (nc) para reducir falsos positivos.
* Procesamiento de Datos: Implementa filtrado avanzado con `grep`, `awk` y `cut` para extraer IPs y puertos de los resultados tipo *Grepable*.
* Reporteo: Incluye una función de persistencia de datos que permite exportar los resultados directamente a archivos `.txt` para su posterior análisis.
* Lógica de Control: Diseñado con ciclos iterativos y estructuras de casos para facilitar múltiples escaneos sin reiniciar el script.

2. HoneypotCreation.sh (Colaborativo)
Un script de defensa activa orientado al monitoreo de intrusiones mediante la creación de servicios falsos.

* Monitoreo: Escucha de forma pasiva en puertos específicos (como 21, 22 o 80) para detectar intentos de conexión no autorizados.
* Gestión de Logs: Redirección automática de eventos al archivo `/var/log/honeypot.log` para facilitar auditorías de seguridad.
* Validación: Incluye funciones de validación de rangos de puertos y manejo de errores para asegurar la estabilidad del servicio.

 Requisitos de Ejecución

Para el correcto funcionamiento de los módulos, asegúrese de contar con:
* Dependencias: `nmap`, `netcat` (nc).
* Privilegios: Ejecución con `sudo` para el manejo de puertos bajos y escritura de logs en sistema.
* Servicios: Se recomienda tener activo el servicio SSH para pruebas de escaneo local.

