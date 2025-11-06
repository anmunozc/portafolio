## 💥 Análisis de Incidente: Ataque DDoS (NIST CSF)

## Descripción

Análisis de la gestión de un incidente de **Denegación de Servicio Distribuido (DDoS)** que afectó a la red interna de una organización multimedia. La respuesta y el análisis se estructuraron siguiendo las cinco funciones del **NIST Cybersecurity Framework (CSF)**.

---

## 📋 Detalles Clave del Incidente

| Aspecto | Resumen |
|----------|-------------|
| **Incidente** | Ataque de Denegación de Servicio Distribuido (**DDoS**). |
| **Tipo de Ataque** | Inundación de ICMP (**Ping Flood**), un ataque volumétrico de Capa 3. |
| **Impacto** | **Indisponibilidad total** de la red interna por **2 horas**. |
| **Vulnerabilidad** | **Firewall perimetral no configurado** (ausencia de `rate-limiting` y filtrado estricto de ICMP). |
| **Respuesta Inicial** | Bloqueo inmediato de paquetes ICMP entrantes, desconexión de servicios no críticos y restablecimiento priorizado de servicios esenciales. |

---

## 🧭 Resultados Principales y Acciones Correctivas

Este incidente identificó fallas en la postura de **Proteger** y **Detectar**, impulsando acciones de mejora inmediatas:

- **Riesgo Prioritario:** Indisponibilidad Operativa y afectación a la Continuidad del Negocio.
- **Acción de Protección:** Implementación inmediata de **reglas de `rate-limiting`** para ICMP y **Hardening** de la configuración del firewall (política de denegación por defecto).
- **Acción de Detección:** Implementación de un **IDS/IPS** y centralización de alertas en un **SIEM** para monitoreo de picos de tráfico.
- **Lección Clave:** Necesidad de un proceso formal de **revisión de la configuración de seguridad** (*security review*) antes de la puesta en producción de cualquier dispositivo perimetral.

---

## 💡 Recomendaciones y Plan de Mejora (Post-Incidente)

Las acciones proactivas, guiadas por el NIST CSF, se centran en el fortalecimiento de la ciberseguridad perimetral:

1. **Fortalecer Protección:** Implementar **IDS/IPS** con filtrado de tráfico sospechoso (función **Proteger**).
2. **Mejorar Detección:** Configurar monitoreo continuo de red (línea base y umbrales de alerta) y centralizar registros en un **SIEM** (función **Detectar**).
3. **Formalizar Respuesta:** Documentar el protocolo de **contención técnica** (bloqueo de ICMP y desconexión de servicios) y automatizar la **captura de paquetes** para análisis forense (función **Responder**).
4. **Optimizar Recuperación:** Documentar el procedimiento de **restauración priorizada** de servicios y realizar una **revisión Post-Mortem** para alimentar el ciclo de mejora (función **Recuperar**).
5. **Auditoría de Configuración:** Establecer un proceso riguroso de **auditoría de configuraciones de seguridad** para todos los dispositivos de red antes de su despliegue.

---

## 🧩 Análisis Detallado por Función NIST CSF

### 🛡️ Proteger

| Medida | Descripción |
|----------|-------------|
| **Protecciones Perimetrales** | Implementación de **nueva regla de limitación de tasa** (`rate-limiting`) para ICMP entrante y verificación de IP de origen. |
| **Tecnología de Mitigación** | Despliegue de un **IDS/IPS** configurado para filtrar tráfico ICMP sospechoso. |
| **Control de Acceso** | **Hardening de la Configuración del Firewall:** Política de seguridad de negar por defecto el tráfico no esencial. |

### 🔍 Detectar

| Medida | Descripción |
|----------|-------------|
| **Monitoreo Continuo** | Implementación de Software de Monitoreo de Red para establecer una línea base y **detectar picos anormales de tráfico ICMP** en tiempo real. |
| **Detección de Intrusiones** | Configurar el IDS/IPS para generar **alertas inmediatas** al superar umbrales de tráfico ICMP definidos. |
| **Comunicaciones** | Centralización de alertas de firewall e IDS/IPS en un sistema **SIEM**. |

### 🚨 Responder

| Medida | Descripción |
|----------|-------------|
| **Contención** | Formalizar el protocolo de **bloqueo inmediato de paquetes ICMP** y la **desconexión controlada de servicios no críticos**. |
| **Análisis** | Implementar **captura de paquetes** automatizada durante el incidente para evidencia forense detallada. |
| **Mejoras del Proceso** | Documentar la necesidad de un proceso formal de **revisión de la configuración de seguridad** pre-producción. |

---

> “Un ataque DDoS nos enseñó que la **disponibilidad** es la primera línea de defensa que debemos proteger con configuración y control.”

## Referencias

📎 **Volver al portafolio principal:**
[⬅️ Inicio](https://anmunozc.github.io/portafolio/)
