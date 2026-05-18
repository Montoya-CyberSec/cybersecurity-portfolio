# 🦠 Detección de Ransomware Hive con Splunk y MITRE ATT&CK

## 📌 Contexto

Este proyecto simula la detección del **ransomware Hive** utilizando el SIEM **Splunk Enterprise**.  
Se comienza con el informe técnico de INCIBE-CERT, se mapean las técnicas del malware al framework **MITRE ATT&CK** y se diseñan consultas **SPL** para identificar comportamientos maliciosos en logs reales (EVTX-ATTACK-SAMPLES). Finalmente, se construyen dashboards que consolidan las detecciones.

## 🎯 Objetivo

- Analizar un ransomware real (Hive) y extraer sus Indicadores de Compromiso (IoC).
- Mapear tácticas y técnicas al framework MITRE ATT&CK.
- Implementar búsquedas SPL en Splunk para detectar actividad maliciosa.
- Crear visualizaciones (dashboards) para monitoreo en tiempo real.

## 🧩 Técnicas MITRE ATT&CK identificadas

| Técnica | ID MITRE | Descripción | Búsqueda SPL |
|---------|----------|-------------|--------------|
| Command and Scripting Interpreter | T1059.003 | Ejecución de `cmd.exe`, `powershell.exe` | `CommandLine="*cmd.exe*" OR "*powershell*"` |
| Inhibit System Recovery | T1490 | Eliminación de copias de seguridad (`vssadmin`, `wmic`) | `CommandLine="*vssadmin delete shadows*" OR "*wmic shadowcopy delete*"` |
| Impair Defenses | T1562.001 | Desactivación de Windows Defender | `CommandLine="*reg.exe* DisableRealtimeMonitoring"` |
| Data Encrypted for Impact | T1486 | Cifrado de archivos con extensiones `.hive`, `.cggbt` | `TargetFilename="*.hive" OR "*.cggbt"` |
| Scheduled Task | T1053.005 | Creación de tareas programadas | `CommandLine="*schtasks*"` |

## 📊 Ejemplos de consultas SPL

### Eliminación de copias de seguridad (T1490)
```spl
index=* source="evtx_data.csv" sourcetype="csv" 
CommandLine="*vssadmin delete shadows*" OR CommandLine="*wmic shadowcopy delete*"
