# 🖥️ Análisis forense de disco y memoria RAM – Caso de laboratorio

## 📌 Contexto del proyecto (entorno controlado)

Este proyecto demuestra un flujo de trabajo completo de **análisis forense digital** en un entorno de laboratorio (máquina virtual Windows 10). Se simuló actividad de usuario: creación y eliminación de archivos, navegación web, descarga de software (Chrome, Tor Browser, ROMs de juegos). Luego se realizó adquisición y análisis de evidencias.

## 🔧 Herramientas utilizadas

- **FTK Imager** – Adquisición forense del disco (imagen E01)
- **DumpIt** – Captura de memoria RAM
- **Autopsy** – Análisis de sistema de archivos, archivos eliminados, historial web
- **Volatility** – Análisis de volcado de memoria (procesos, estructuras del kernel)
- **PowerShell** – Cálculo de hashes SHA-256

## 📂 Documento incluido

| Documento | Descripción | Formato |
|-----------|-------------|---------|
| Informe completo de análisis forense | Adquisición, análisis de disco (Autopsy), análisis de memoria (Volatility), correlación de hallazgos, conclusiones. | [PDF](./analisis-forense-disco-memoria.pdf) |

## 🎯 Resultados clave

- Recuperación de archivos eliminados (`Passwords.txt`, `System Info.txt`, ROM de juego)
- Identificación de historial web y descargas (Tor Browser, sitios de juegos retro)
- Detección de procesos activos en memoria (`msedge.exe`, `WinRAR.exe`, `DumpIt.exe`)
- Correlación temporal entre actividad de disco y memoria
- Verificación de integridad con SHA-256

## ⚠️ Nota de confidencialidad

**Este proyecto se realizó en un entorno de laboratorio aislado.**  
Todos los datos personales, nombres de usuario y fechas exactas han sido anonimizados. No se incluye información confidencial de ninguna organización real.

---

*Informe adaptado para portafolio profesional. Mayo 2026.*
