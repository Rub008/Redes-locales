# Redes-locales
#  Módulo: Redes Locales (0223)
## Proyecto Intermodular - Clínica "Fisiovita"

**Autor:** Rubén Aznar España | **Fecha:** 13/05/2026 | **Curso:** SMR1 (Prometeo)

---

##  Descripción del Proyecto
Diseño, estructuración y planificación de la infraestructura de red local (LAN) para la clínica de fisioterapia **Fisiovita**, garantizando una conectividad segura, rápida y eficiente para todos los empleados.

##  1. Análisis de Necesidades y Dispositivos
La red está diseñada para soportar un total de **9 dispositivos finales**:
* **8 Ordenadores Personales (PCs):** Distribuidos entre recepción (PC0 y PC1) y las salas de consulta de los fisioterapeutas (PC2 a PC7).
* **1 Impresora de Red:** Equipo centralizado e independiente para el uso común de toda la clínica.

##  2. Diseño de la Red y Topología
* **Topología en Estrella:** Todos los equipos finales se conectan de forma centralizada hacia los elementos de interconexión (switches), facilitando la detección de fallos y la escalabilidad.
* **Segmentación:** Organización física y lógica orientada a optimizar el tráfico de datos y garantizar que el acceso a Internet sea fluido en cada puesto de trabajo.

##  3. Plan de Direccionamiento IP
Se ha establecido un esquema de direccionamiento privado estructurado para una administración eficiente y sin conflictos de IP:
* **Segmento de Red:** Uso de direccionamiento de clase C.
* **Asignación Estática:** Configuración de IPs fijas para la impresora y los recursos críticos de la red local para evitar pérdidas de conectividad.

##  4. Servicios de Red Básicos Implementados
* **Compartición de Archivos:** Configuración de un entorno común seguro para el intercambio de documentos internos de la clínica.
* **Impresión Centralizada:** Acceso compartido de los 8 PCs hacia la impresora de red única.
* **Control de Usuarios en Red:** Gestión de identidades basada en roles y niveles de privilegios:
  * **Perfil Recepción (PC0/PC1):** Acceso a agenda, contactos y facturación (sin acceso a historiales médicos).
  * **Perfil Fisioterapeuta (PC2 a PC7):** Acceso a fichas clínicas de pacientes (restringido para modificar la facturación general).

##  5. Servicio Crítico de Copias de Seguridad (Backups)
* **Automatización:** Programación de copias de seguridad diarias automatizadas fuera del horario comercial.
* **Seguridad (RGPD):** Envío cifrado del tráfico de backup a través de los switches hacia un destino de almacenamiento seguro (servidor local aislado o nube).
* **Continuidad de Negocio:** Garantiza la restauración rápida ante averías, corrupción de bases de datos o ataques de malware sin afectar las citas de la clínica.

---
📂 **Documento completo con planos y esquemas en:** `docs/redes-locales/Intermodular_Redes_Locales.pdf`
