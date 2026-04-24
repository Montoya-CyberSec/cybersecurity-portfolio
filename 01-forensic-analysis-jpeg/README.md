# 🔍 Análisis forense de imagen JPEG y extracción de archivo oculto

## 📌 Descripción del proyecto
Este proyecto demuestra técnicas fundamentales de **análisis forense digital** aplicadas a una imagen en formato JPEG. El objetivo es identificar el tipo de archivo, verificar su integridad mediante hashes, extraer metadatos ocultos y recuperar un segundo archivo embebido mediante esteganografía y extracción manual a bajo nivel.

## 🛠️ Herramientas y comandos utilizados
- **Kali Linux** / Windows 11
- `file` – Identificación de tipo de archivo por cabeceras
- `sha256sum` / PowerShell / HashMyFiles – Cálculo de hash SHA-256
- `exiftool` – Extracción de metadatos EXIF
- `steghide` – Detección inicial de datos ocultos
- `binwalk` – Análisis de firmas y detección de archivos embebidos
- `dd` – Extracción manual por offset
- **HxD** – Editor hexadecimal para verificar magic numbers

## 📋 Metodología aplicada
1. **Identificación del formato** – Comando `file` y análisis de cabeceras (magic numbers `FF D8` para JPEG).
2. **Cálculo de hash SHA-256** – Para el archivo original, garantizando integridad durante el análisis.
3. **Extracción de metadatos** – Uso de `exiftool` para obtener autor, modelo de cámara, fechas y posibles coordenadas.
4. **Búsqueda de esteganografía** – `steghide` (solicita contraseña) y `binwalk` (detecta firmas de archivos adicionales).
5. **Extracción manual** – Empleo de `dd` con el offset preciso para copiar el archivo oculto (PNG).
6. **Verificación final** – Cálculo del hash SHA-256 del archivo extraído y validación del formato con `file`.

## 📄 Resultados obtenidos
- El archivo original es un **JPEG válido** (JFIF).
- Metadatos revelan autor **Pedro J. López H.** (nombre ficticio) y cámara **Sony DSC-H300**.
- Se detectó un **archivo PNG oculto** a partir del offset `209939`.
- Extracción exitosa mediante `dd` generando `fichero_oculto.png`.
- Hash SHA-256 del archivo extraído: *(el que calculaste – puedes ponerlo)*

## 📎 Informe completo
El detalle paso a paso, con capturas de pantalla y comandos, está disponible en el siguiente PDF:  
[📄 Descargar informe de análisis forense](./01_report-forensic-analysis.pdf)

## ⚠️ Declaración de confidencialidad
Este proyecto se ha realizado exclusivamente con **archivos de prueba y datos ficticios**. No se incluye información confidencial de ninguna organización real, ni se han utilizado vulnerabilidades reales. El contenido es puramente educativo y demostrativo, alineado con buenas prácticas de divulgación responsable.

## 🗓️ Fecha de realización
Diciembre 2025 – Adaptado para portafolio profesional (Abril 2026).
