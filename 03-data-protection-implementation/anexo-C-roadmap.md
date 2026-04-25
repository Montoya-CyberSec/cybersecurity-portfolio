# Anexo C – Roadmap de Implementación

El siguiente cronograma resume las fases, tareas clave, responsables y duraciones estimadas del programa de protección de datos. Los plazos son relativos (en semanas y meses) y se ajustarán según la contratación del proveedor externo especializado.

| Fase / Tarea | Responsable(s) | Duración estimada | Hito |
|--------------|----------------|-------------------|------|
| **FASE 1: GOBIERNO Y CONTRATACIÓN** | | | |
| Formalización de gobernanza (resolución) | DPD / Asesoría Legal | 1 semana | Fin semana 1 |
| Presentación de propuesta de contratación externa | DPD | 1 semana | Fin semana 1 |
| Aprobación de resolución y plan por Gerencia | Gerencia General | 2 días | Fin semana 2 |
| Elaboración de términos de referencia (TdR) | DPD / Jurídico / TI / OSI | 1 semana | Fin semana 2 |
| Evaluación de ofertas y selección de proveedor | Gerencia / Compras | 1 semana | Fin semana 3 |
| Contratación formal y firma de contrato | Gerencia / Compras | 1 semana | Fin semana 4 |
| **FASE 2: DIAGNÓSTICO DETALLADO Y LEVANTAMIENTO** | | | |
| Kick-off del proyecto con proveedor y áreas internas | Responsable Interno / DPD | 2 días | Inicio semana 5 |
| Levantamiento de información para RAT (envío de formularios) | Proveedor / Responsable Interno | 1 semana | Fin semana 5 |
| Reuniones de seguimiento y aclaraciones con áreas | Proveedor / Responsable Interno | 2 semanas | Fin semana 7 |
| Consolidación de información recibida | Proveedor / Responsable Interno | 1 semana | Fin semana 8 |
| Análisis de riesgos de protección de datos | Admin Riesgos / DPD | 1 semana | Fin semana 9 |
| **FASE 3: CONSTRUCCIÓN DE INSTRUMENTOS CLAVE** | | | |
| Elaboración del Registro de Actividades de Tratamiento (RAT) | Proveedor | 3 semanas | Fin semana 12 |
| Validación del RAT por áreas dueñas | Áreas operativas | 2 semanas | Fin semana 14 |
| Aprobación del RAT por Gerencia | Gerencia General | 1 semana | Fin semana 15 |
| Elaboración de Política Institucional de Protección de Datos | Proveedor / Cumplimiento / Responsable Interno | 1 semana | Fin semana 12 |
| Aprobación de política por Gerencia | Gerencia General | 1 semana | Fin semana 13 |
| Desarrollo de procedimiento de atención de derechos ARCO | Proveedor / Jurídico / Responsable Interno | 1 semana | Fin semana 14 |
| Desarrollo de procedimiento de gestión de incidentes | Proveedor / OSI / TI | 1 semana | Fin semana 14 |
| Desarrollo de procedimiento de conservación y eliminación | Proveedor / RRHH / Financiero | 1 semana | Fin semana 14 |
| Validación y aprobación de procedimientos | Gerencia / DPD | 1 semana | Fin semana 15 |
| **FASE 4: CONTROLES DE SEGURIDAD Y TERCEROS** | | | |
| Inventario de proveedores con acceso a datos (encargados) | Proveedor / Compras | 1 semana | Fin semana 9 (solapada) |
| Revisión y actualización de contratos con encargados | Jurídico / Compras | 2 semanas | Fin semana 11 |
| Evaluación de medidas técnicas de seguridad (diagnóstico) | TI / OSI / Proveedor | 1 semana | Fin semana 15 |
| Definición de plan de implementación de controles técnicos | TI / OSI / DPD | 1 semana | Fin semana 16 |
| Implementación inicial de controles priorizados (cifrado, MFA, DLP) | TI / OSI / Proveedor | 4 semanas | Fin semana 20 |
| Pruebas y ajustes de controles técnicos | TI / OSI | 2 semanas | Fin semana 22 |
| **FASE 5: CULTURA, CAPACITACIÓN Y CIERRE** | | | |
| Diseño de programa de capacitación | Proveedor / RRHH / DPD | 1 semana | Fin semana 22 |
| Ejecución de capacitación inicial a personal crítico | RRHH / Proveedor | 1 semana | Fin semana 23 |
| Evaluación de satisfacción y conocimientos | RRHH | 1 semana | Fin semana 24 |
| Elaboración de informe final de implementación inicial | Responsable Interno / DPD | 1 semana | Fin semana 25 |
| Presentación de resultados a Gerencia | Responsable Interno / DPD | 1 semana | Fin semana 26 |
| Acta de cierre de fase inicial y transición a operación | Gerencia / DPD | 1 semana | Fin semana 27 |

**_Nota._** *La duración total estimada es de aproximadamente 6-7 meses desde el inicio formal del proyecto. Los hitos están sujetos a la disponibilidad de recursos y a la contratación del proveedor externo.*

```mermaid
gantt
    title Programa de Protección de Datos – Cronograma de implementación
    dateFormat  YYYY-MM-DD
    axisFormat  %b %Y
    
    section Fase 1: Gobernanza y Contratación
    Formalización gobernanza        :active,    des1, 2024-04-01, 5d
    Presentación propuesta          :            des2, after des1, 5d
    Aprobación Gerencia              :            des3, after des2, 2d
    Términos de referencia (TdR)    :            des4, after des2, 5d
    Evaluación ofertas               :            des5, after des4, 5d
    Contratación formal              :            des6, after des5, 5d

    section Fase 2: Diagnóstico y Levantamiento
    Kick-off proyecto                :            des7, after des6, 2d
    Envío formularios RAT            :            des8, after des7, 5d
    Reuniones seguimiento            :            des9, after des8, 10d
    Consolidación información        :            des10, after des9, 5d
    Análisis de riesgos              :            des11, after des10, 5d

    section Fase 3: Instrumentos Clave
    Elaboración RAT                  :            des12, after des11, 15d
    Validación RAT por áreas         :            des13, after des12, 10d
    Aprobación RAT                   :            des14, after des13, 5d
    Política de Protección Datos     :            des15, after des11, 5d
    Procedimiento derechos ARCO      :            des16, after des15, 5d
    Procedimiento incidentes         :            des17, after des15, 5d
    Procedimiento conservación       :            des18, after des15, 5d
    Validación final de proceds.     :            des19, after des14, 5d

    section Fase 4: Controles y Terceros
    Inventario proveedores datos     :            des20, after des11, 5d
    Revisión contratos encargados    :            des21, after des20, 10d
    Diagnóstico medidas técnicas     :            des22, after des14, 5d
    Plan de controles técnicos       :            des23, after des22, 5d
    Implementación controles (cifrado, MFA, DLP) : des24, after des23, 20d
    Pruebas y ajustes                :            des25, after des24, 10d

    section Fase 5: Cultura y Cierre
    Diseño programa capacitación     :            des26, after des24, 5d
    Ejecución capacitación inicial   :            des27, after des26, 5d
    Evaluación satisfacción          :            des28, after des27, 5d
    Informe final implementación     :            des29, after des28, 5d
    Presentación a Gerencia          :            des30, after des29, 5d
    Acta de cierre y transición      : milestone,  after des30, 0d




