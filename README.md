# NefrIA 4.0

Aprendizaje, simulación clínica y evaluación adaptativa en Nefrología y Urología (Patología Médico-Quirúrgica del Sistema Nefrourinario, asignatura 1956, Grado en Medicina, UMH). Aplicación web de un solo fichero, sin servidor.

**Usar la app:** https://fborrasumh.github.io/nefria/

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23692688.svg)](https://doi.org/10.5281/zenodo.23692688)

**Idiomas:** español (por defecto), inglés y portugués.

## Qué hace (versión 2.0.0, «NefrIA 4.0»)

- **Mapa de competencias y motor adaptativo.** 20 competencias en 6 dimensiones (conocimiento, interpretación, razonamiento, decisiones terapéuticas, seguridad, comunicación) con niveles 0–4. Toda actividad deja una evidencia; unas reglas deterministas y auditables estiman el dominio, programan el repaso espaciado y recomiendan la siguiente actividad explicando por qué. La IA no modifica el perfil.
- **Aprender:** las 30 unidades de la guía docente con sus objetivos.
- **Laboratorio de fisiología renal:** nefrona interactiva (filtrado, angiotensina II, aldosterona, ADH, PTH, carga de sodio), escenarios patológicos y retos de predicción. Modelo cualitativo educativo: direcciones de cambio, no valores de un paciente.
- **Laboratorio de diagnóstico:** analíticas con lectura de valores y clasificación KDIGO, gasometrías generadas por semilla y corregidas por código, sedimento urinario e imagen renal con imágenes de licencia libre (Wikimedia Commons; autor y licencia bajo cada imagen; necesitan conexión).
- **Calculadoras y problemas** de la versión 1 (CKD-EPI 2021, KDIGO, ácido-base, sodio y agua, FENa/FEUrea, PSA y D’Amico).
- **30 pacientes virtuales** con hasta 10 estados (presentación, anamnesis, exploración, pruebas, interpretación, diferencial, diagnóstico, tratamiento, evolución y evaluación). La evolución depende de la decisión; la puntuación es por dimensiones y un error crítico de seguridad la limita al 40 % sin compensación.
- **Diálisis y trasplante:** comparador de modalidades, simulador de urea de un compartimento con Kt/V de Daugirdas II (no prescribe) y práctica.
- **ECOE:** 9 estaciones con tiempo, lista ponderada y errores críticos no compensables; práctica libre, cronometrada, simulacro y evaluación docente.
- **Simulacro** tipo test de 40 preguntas.
- **Tutor IA** con contexto docente visible (competencia, nivel, errores, referencias autorizadas) y seis modos; el código marca cifras ajenas al contexto, referencias fuera de la lista y frases con notas.
- **Mi progreso:** mapa de competencias, plan individual, errores recurrentes, evolución, informe en Word, copia completa (esquema `nefria/2`, migra las copias de la v1) y exportación seudonimizada para el profesorado.
- **Panel del profesorado:** importa varios JSON (descarta duplicados), muestra competencias del grupo (estimación del motor) e ítems con más errores y su discriminación (datos observados), propone refuerzos, exporta CSV, Word y PDF, configura los tiempos ECOE y registra qué contenidos se han validado.

## Estado del contenido

Todo el contenido clínico nuevo (22 pacientes, 9 estaciones ECOE, paneles de laboratorio, ítems de sedimento e imagen, modelos de fisiología y diálisis) figura como **pendiente de revisión** hasta que lo valide el profesorado responsable.

## Privacidad

Los datos se guardan solo en el navegador. La IA es opcional (OpenAI, Google Gemini o Anthropic Claude, con clave propia); antes del primer envío se muestra lo que sale y se enmascaran datos personales. La exportación para el profesorado no incluye textos libres ni claves. Para investigar con estos datos se necesita aprobación de un comité de ética y consentimiento informado.

## Autoría

Fernando Borrás Rocher (ORCID 0000-0002-5519-4573) y Luis Gómez Pérez (ORCID 0000-0003-1396-0484), Universidad Miguel Hernández de Elche. Licencia MIT.

## Fuentes del proyecto

El fichero `nefria_fuentes.zip`, archivado en el registro de Zenodo junto al código, contiene el proyecto Forja (`src/`, `build.py`, `app.json`) y las pruebas (`tests/`: 6 pruebas de lógica en Node y una prueba de humo en Chromium con IA simulada). Para regenerar: `python3 build.py`.
