# scam-alert-data

## 📌 Descripción

Este repositorio contiene el versionado de los datos utilizados por el
sistema **scam-alert**.

Aquí se publican datasets obtenidos mediante scraping de fuentes
públicas, incluyendo:

-   🏥 Hospitales
-   🚑 Centros extrahospitalarios 24h
-   🌍 Embajadas
-   👮 Comisarías

El objetivo es mantener un histórico reproducible, auditable y
versionado de los datos.

------------------------------------------------------------------------

## 🗂️ Contenido del dataset

Cada exportación incluye:

-   Total de entidades procesadas
-   Validación de integridad
-   Exclusión de registros sin geolocalización en GeoJSON

Ejemplo:

-   Total entidades: 841
-   Validación: PASS
-   GeoJSON excluye entidades sin coordenadas

------------------------------------------------------------------------

## 📦 Formatos disponibles

Los datos se publican en múltiples formatos abiertos:

-   JSON → dataset completo (con y sin coordenadas)
-   CSV → formato tabular
-   XML → interoperabilidad
-   GeoJSON → solo entidades con coordenadas válidas
-   KML → compatible con Google Earth
-   GML → estándar GIS

------------------------------------------------------------------------

## ⚠️ Nota sobre GeoJSON

GeoJSON excluye entidades sin coordenadas GPS.

Esto es intencional: incluir `geometry: null` rompe la compatibilidad
con muchas herramientas GIS.

Los datos completos están disponibles en JSON, CSV y XML.

------------------------------------------------------------------------

## 🔄 Versionado

Cada export:

-   Está fechado
-   Incluye validación
-   Permite detectar cambios mediante hash (SHA-256)

Los datasets sin cambios no se reescriben.

------------------------------------------------------------------------

## 🤝 Recomendaciones para facilitar el scraping

Si gestionas una web pública y quieres facilitar la reutilización de
datos:

### Formatos recomendados

-   JSON estructurado (preferido)
-   CSV accesible
-   APIs REST (ideal)

### Buenas prácticas

-   Incluir coordenadas GPS (lat/lon)
-   Evitar contenido dinámico innecesario (JS pesado)
-   Usar HTML semántico
-   Mantener URLs estables
-   Evitar paginación compleja o bloqueos anti-bot agresivos

### Evitar

-   Datos solo en imágenes
-   HTML mal estructurado
-   Uso excesivo de JavaScript para renderizar contenido

------------------------------------------------------------------------

## 🚀 Uso

Este repositorio está pensado como fuente de datos:

-   Integración en pipelines
-   Consumo por APIs
-   Análisis geoespacial

------------------------------------------------------------------------

## 📄 Licencia

MIT
