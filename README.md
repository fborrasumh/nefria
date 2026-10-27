# NefrIA

Patología médico-quirúrgica del sistema nefrourinario: calculadoras, problemas, casos secuenciales y simulacro. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/nefria/

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

- **Temario:** las 30 unidades de la guía docente de Patología Médico-Quirúrgica del Sistema Nefrourinario (asignatura 1956), en sus dos partes —Nefrología (U1–U15) y Urología (U16–U30)—, con dos o tres ideas clave por unidad y los once objetivos de aprendizaje (saber, saber hacer, saber ser), que el estudiante marca cuando los domina.
- **Calculadoras clínicas deterministas**, con la fórmula y los pasos a la vista: filtrado glomerular CKD-EPI 2021 (sin coeficiente de raza) y Cockcroft-Gault, categorías G y A con el mapa de riesgo KDIGO; ácido-base (trastorno primario, compensación esperada aguda o crónica, coherencia de Henderson-Hasselbalch, anión gap corregido por albúmina y delta/delta); sodio y agua (osmolalidad calculada, sodio corregido por glucosa, agua corporal total, Adrogué-Madias con el volumen necesario y aviso del límite de corrección, déficit de agua libre); daño renal agudo (estadio KDIGO, FENa y FEUrea); urología (densidad del PSA, PSA libre/total, riesgo de D'Amico e IPSS).
- **Problemas con solución calculada:** ocho tipos (CKD-EPI, anión gap corregido, Winter, Adrogué-Madias, sodio corregido, FENa, déficit de agua libre y densidad del PSA) con variantes reproducibles por semilla. Si la respuesta no coincide, el código recalcula el problema con los errores típicos (constantes del otro sexo, olvido de la edad, Cockcroft-Gault en lugar de CKD-EPI, albúmina sin corregir, potasio incluido, +1 olvidado del denominador, factor de agua equivocado, factor de Hillier, cociente invertido…) y explica cuál se ha cometido. Las variantes en las que un error típico daría casi el mismo resultado se descartan.
- **Casos clínicos de razonamiento secuencial:** ocho pacientes ficticios (hiponatremia por tiazida, daño renal agudo prerrenal, síndrome nefrótico por membranosa, enfermedad renal diabética, pielonefritis obstructiva, tumor urotelial, torsión testicular y retención aguda de orina). El estudiante pide solo las pruebas que quiere, elige diagnóstico y conducta, y el código puntúa las pruebas clave omitidas, las prescindibles pedidas y las decisiones, con su explicación. Después escribe su razonamiento y puede compararlo con los elementos esperados (sin IA) o pedir comentarios al tutor de IA.
- **Simulacro tipo test:** 40 preguntas de 4 alternativas (20 de Nefrología y 20 de Urología), filtrables por parte y unidad, con explicación inmediata, nota orientativa de cada parte y media compensada (la guía indica que las dos partes se compensan), sin penalización, y repaso de las falladas.
- **Progreso:** unidades dominadas, aciertos por unidad, problemas y casos, qué repasar, informe en Word (generado en el navegador, sin librerías externas) y copia JSON para continuar en otro ordenador.

## Cómo se usa la IA

Solo en los casos clínicos, para comentar el razonamiento escrito, con la propia clave de OpenAI, Google Gemini o Anthropic Claude. La clave se guarda solo en el navegador; no hace falta servidor. El resto (calculadoras, problemas, puntuación de casos, simulacro, informes) funciona sin clave. **La IA propone, el código comprueba:** cada elemento que la IA da por presente debe venir con una cita literal del texto del estudiante; si la cita no aparece, se marca «sin evidencia» y no cuenta; los elementos con identificadores inventados se descartan; las frases con notas o puntuaciones se retiran (el tutor no califica), y se avisa de cifras que no están ni en el caso ni en el texto. «Ver un ejemplo» muestra un caso resuelto con un comentario precalculado, sin usar la IA, en los tres idiomas.

## Privacidad

El progreso, las respuestas y la clave se guardan solo en el navegador (IndexedDB y localStorage). Al pedir comentarios al tutor sale hacia el proveedor elegido el caso ficticio y el razonamiento del estudiante, con correos, DNI/NIE y teléfonos enmascarados; antes del primer envío de la sesión se muestra lo que sale y se pide confirmación. La copia JSON no contiene la clave. No deben escribirse datos de pacientes reales.

## Límites

Es material de estudio: no sustituye a las clases, a la bibliografía de la guía ni al juicio clínico, y las calculadoras no deben usarse para decidir sobre pacientes reales. Las ideas clave, preguntas y casos los ha redactado el equipo autor a partir de la guía docente y de guías clínicas de referencia (KDIGO, Sociedad Española de Nefrología, European Association of Urology); conviene que el profesorado de la asignatura los revise y las recomendaciones clínicas cambian con el tiempo. Umbrales como el anión gap normal (12 mmol/L) o los factores de agua corporal son convencionales y varían según la fuente. La nota del simulacro es orientativa. Los comentarios del tutor los genera una IA y pueden ser incompletos o erróneos: el código verifica las citas, no la exactitud clínica. Probado con IA simulada en los tres proveedores; no se ha probado con claves reales.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche) y Luis Gómez Pérez (Universidad Miguel Hernández de Elche).

Construida a partir de la guía docente de Patología Médico-Quirúrgica del Sistema Nefrourinario (asignatura 1956, 5.º curso del Grado en Medicina, UMH, curso 2026-2027), de la que Luis Gómez Pérez es profesor responsable.

ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573) · Luis Gómez Pérez [0000-0003-1396-0484](https://orcid.org/0000-0003-1396-0484)

## Cómo citar

Borrás Rocher, F. y Gómez Pérez, L. (2026). *NefrIA* (v1.0.0) [Software]. (DOI en trámite)

## Licencia

MIT. Véase [LICENSE](LICENSE).
