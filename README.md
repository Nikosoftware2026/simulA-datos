# simulA – datos

Condiciones vigentes de préstamos para personas en Uruguay, en un único archivo: [`catalogo.json`](catalogo.json).
Lo usa la app **simulA** (comparador de préstamos) para mantenerse al día sin necesidad de actualizar la app.

Todo el contenido proviene de **fuentes públicas**: cartillas, tarifarios y páginas web de cada institución, y
cotizaciones del Banco Central del Uruguay. Cada producto indica su fuente y la fecha del documento.

## Qué contiene

- `fecha`: última revisión de las condiciones.
- `mercado`: dólar y UI del BCU, UR, inflación y variación del dólar de los últimos 5 años.
- `productos`: por cada producto, tasas (por plazo, o en grilla por plazo, porcentaje financiado y monto),
  plazos, montos, vigencia de promociones, salvedades y fuente. `activo: false` lo retira de la app.
- `nuevos`: productos incorporados en revisiones posteriores, descritos solo con datos.
- `sinDatos`: instituciones que no publican condiciones suficientes.

## Cómo se actualiza

El día 1 de cada mes se revisan automáticamente todas las fuentes. Los cambios se proponen en un *pull request*
con un informe y se publican recién cuando se aprueban. Antes de publicar, cada versión pasa una validación de
estructura y rangos y una simulación de prueba.

## Aviso

Información orientativa recopilada de fuentes públicas; puede contener errores o haber cambiado. Las condiciones
finales las define cada institución. simulA no es un banco ni intermedia préstamos.
