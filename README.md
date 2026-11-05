# SinapsIA

Asistente de investigación con segundo cerebro y fuentes verificadas. Aplicación web de un solo fichero.

**Usar la app:** https://fborrasumh.github.io/sinapsia/

[![DOI](https://zenodo.org/badge/DOI/10.5281/zenodo.23985229.svg)](https://doi.org/10.5281/zenodo.23985229)

**Idiomas:** español (por defecto), inglés, portugués; selector en la barra superior (o `?lang=en` / `?lang=pt` en la URL).

## Qué hace

- **Consulta en lenguaje natural, escrita o dictada.** La IA convierte la pregunta en una o dos búsquedas en inglés para [OpenAlex](https://openalex.org) (todas las disciplinas, solo trabajos con resumen).
- **Verifica cada DOI en [Crossref](https://www.crossref.org):** ✓ si existe y su título coincide; avisa si no existe o el título es otro. Los trabajos **retractados** (según OpenAlex) se marcan en rojo.
- **Responde solo con los resúmenes recuperados.** Cada afirmación lleva una cita literal del resumen de su fuente y el **código** comprueba que la cita está: ✓ verificada, ⚠ no verificada. También detecta fuentes que la IA cite sin haberlas recibido y cifras que no aparecen en las fuentes.
- **Segundo cerebro:** las fuentes se capturan como notas con su referencia y la cita verificada; las respuestas se guardan como ideas enlazadas a sus fuentes. Las notas se organizan con el método PARA (Proyectos, Áreas, Recursos, Archivo) y se enlazan escribiendo `[[Título]]`, con retroenlaces y enlaces rotos que se pueden crear con un clic.
- **Conexiones con lo que ya sabes:** antes de preguntar, el código busca tus notas relacionadas; la IA indica si la evidencia las apoya, matiza, contradice o amplía.
- **Grafo de conocimiento** animado de notas y enlaces.
- **Sincronización con Google Drive para ordenador** (Chrome/Edge de escritorio): un único `sinapsia-cerebro.json` en la carpeta elegida, fusionado nota a nota (gana la modificación más reciente; los borrados se guardan como lápidas) y copia diaria (se conservan las 14 últimas). En otros navegadores, abrir y descargar el expediente a mano.
- **Voz:** dictado de la pregunta y lectura de las respuestas en voz alta con las funciones del navegador.
- **Descargas:** bibliografía en CSV y bóveda Markdown en ZIP (se abre en Obsidian o Logseq), sin depender de ninguna librería externa.
- **Ejemplo sin clave** en los tres idiomas, con fuentes ficticias marcadas como tales.

## Cómo se usa la IA

Con la propia clave de OpenAI, Google Gemini o Anthropic Claude, y una **clave gratuita de OpenAlex** (desde febrero de 2026 OpenAlex la exige para un uso normal; se crea en openalex.org → Settings → API). Las claves se guardan solo en el navegador y nunca van al fichero de Drive ni a las descargas. No hace falta servidor.

## Privacidad

- En el navegador (IndexedDB): las notas, la conversación y las claves.
- Hacia OpenAlex: las palabras de búsqueda. Hacia Crossref: los DOI.
- Hacia el proveedor de IA: la pregunta, los resúmenes públicos encontrados y hasta cuatro notas relacionadas, con correos, DNI/NIE y teléfonos enmascarados; antes del primer envío de cada sesión se muestra una muestra de lo que sale y se pide confirmación.
- Dictado: en Chrome y Edge el audio se procesa en los servidores de voz del navegador (Google o Microsoft); se avisa antes del primer uso.
- Drive: el expediente queda en la carpeta que elijas, sincronizada por el cliente de Google Drive.

## Límites

- Lee **resúmenes, no artículos completos**: lo que no está en el resumen no lo sabe. Consulta el artículo antes de citarlo.
- Cada consulta trae hasta 8 trabajos: no es una revisión sistemática ni garantiza exhaustividad.
- La verificación comprueba que la cita está en el resumen, no que la afirmación de la IA la interprete correctamente: léela.
- Si se edita la misma nota en dos equipos a la vez, gana la última guardada; los retrasos de sincronización dependen del cliente de Drive.
- El dictado solo funciona en navegadores con reconocimiento de voz (Chrome, Edge).
- Probada con IA, OpenAlex, Crossref, carpeta de Drive y voz **simulados** (55 pruebas en Chromium, 29 de lógica en Node, 0 infracciones WCAG 2.2 AA con axe-core); pendiente de prueba con claves y servicios reales.

## Autoría

Fernando Borrás Rocher (Universidad Miguel Hernández de Elche).


ORCID: Fernando Borrás Rocher [0000-0002-5519-4573](https://orcid.org/0000-0002-5519-4573)

## Cómo citar

Borrás Rocher, F. (2026). *SinapsIA* (v1.0.0) [Software]. DOI: [10.5281/zenodo.23985229](https://doi.org/10.5281/zenodo.23985229)

## Licencia

MIT. Véase [LICENSE](LICENSE).
