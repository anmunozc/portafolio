# 🧾 Botium Toys — Informe de Evaluación de Riesgos

## 1. Alcance de la auditoría
La auditoría cubre los activos críticos de la empresa **Botium Toys**, incluyendo:
- Servidores locales y servicios de red internos.  
- Sitio web corporativo y pasarela de pagos en línea.  
- Estaciones de trabajo del personal administrativo.  
- Políticas de contraseñas, backups y acceso remoto.  
- Cumplimiento con **PCI DSS** y **RGPD**.  

---

## 2. Objetivos
1. Evaluar la postura actual de seguridad de la organización.  
2. Identificar vulnerabilidades, amenazas y riesgos críticos.  
3. Revisar el cumplimiento con normativas aplicables.  
4. Proporcionar recomendaciones para mejorar la madurez de ciberseguridad según **NIST CSF**.

---

## 3. Activos identificados
| Activo | Tipo | Importancia | Riesgo asociado |
|---------|------|-------------|----------------|
| Servidor web | Infraestructura | Crítico | Acceso no autorizado, fuga de datos |
| Base de datos de clientes | Datos sensibles | Crítico | Violación RGPD |
| PCs administrativos | Hardware | Medio | Infección por malware |
| Red Wi-Fi interna | Comunicación | Alto | Acceso sin cifrado |
| Portal de pagos | Aplicación | Crítico | Cumplimiento PCI DSS |

---

## 4. Evaluación de riesgos
| Riesgo | Probabilidad | Impacto | Nivel | Mitigación |
|--------|---------------|----------|--------|-------------|
| Fuga de datos por mala gestión de contraseñas | Alta | Alto | Crítico | Implementar MFA y política de contraseñas seguras |
| Falta de cifrado en datos de clientes | Media | Alto | Alto | Cifrado AES-256 y protocolos HTTPS/TLS actualizados |
| Phishing al personal | Alta | Medio | Alto | Capacitación trimestral en seguridad |
| Actualizaciones de software pendientes | Media | Alto | Alto | Implementar sistema de parches automatizado |
| Pérdida de datos por backup incompleto | Baja | Alto | Medio | Validar copias de seguridad semanalmente |

---

## 5. Conclusiones
- Botium Toys presenta una madurez de seguridad **Tier 2 – Partial (NIST CSF)**.  
- Se requiere establecer políticas formales y revisiones periódicas.  
- Se recomienda priorizar la protección de datos sensibles y la capacitación del personal.

---

> *“La seguridad de una empresa no se mide por la ausencia de incidentes, sino por su capacidad de detectarlos y aprender de ellos.”*
