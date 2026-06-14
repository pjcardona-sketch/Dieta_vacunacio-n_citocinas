# Dieta_vacunacion_Citocinas

Análisis de perfiles inmunológicos mediante visualización jerárquica de citocinas y quimiocinas obtenidas mediante tecnología Luminex.

## Objetivo

Evaluar el efecto combinado de:

- Dieta (ND vs HFD)
- Vacunación (Sham vs BCG)
- Estado de infección (LDA vs MCI)

sobre la respuesta inmunológica medida mediante múltiples citocinas y quimiocinas.

La visualización propuesta sustituye los gráficos de dispersión originales por un heatmap jerárquico acompañado de clustering jerárquico, permitiendo identificar patrones globales de respuesta inmunológica.

---

## Estructura del repositorio

```text
Dieta_vacunacion_Citocinas/
│
├── Dieta_vacunacion_Citocinas_seaborn.ipynb
├── Dieta_vacunacion_citocinas.xlsx
|-- heatmap_luminex_clustermap_okabe_ito.html
├── heatmap_luminex_altair_anotado_integrativo.html
|-- heatmap_luminex_clustermap_okabe_ito
├── heatmap_luminex_clustermap_okabe_ito.pdf
├── heatmap_luminex_clustermap_okabe_ito.png
|-- README.md
```

---

## Datos

Los datos originales fueron transformados a formato tidy siguiendo los principios de Wickham.

Cada observación contiene:

- Dieta
- Estado de infección
- Estado de vacunación
- Analito
- Concentración

---

## Metodología

### Limpieza de datos

- Eliminación de valores ausentes.
- Conversión de variables numéricas.
- Estandarización de etiquetas categóricas.

### Transformación

- Transformación log10 de concentraciones.
- Estandarización mediante z-score por analito.

### Visualización

Se implementa un heatmap utilizando Altair/Vega-Lite:

- Filas = analitos.
- Columnas = grupos experimentales.
- Color = z-score.

Además, se calcula clustering jerárquico mediante:

- Distancia euclídea.
- Enlace promedio (average linkage).

---

## Reproducibilidad

El notebook puede ejecutarse íntegramente en Google Colab.

Los datos se cargan automáticamente desde este repositorio GitHub, por lo que no es necesario subir archivos manualmente.

---

## Tecnologías

- Python
- Pandas
- NumPy
- SciPy
- Altair (Vega-Lite)
- Matplotlib

---
# Ejecutar el proyecto

## Google Colab

https://colab.research.google.com/github/pjcardona-sketch/Dieta_vacunacio-n_Citocinas/blob/main/Dieta_vacunacion_Citocinas_seaborn.ipynb

## Repositorio GitHub

https://github.com/pjcardona-sketch/Dieta_vacunacio-n_Citocinas

## Visualización HTML

https://pjcardona-sketch.github.io/Dieta_vacunacio-n_Citocinas/heatmap_luminex_clustermap_okabe_ito.html

## Visualización HTML integrativo

https://pjcardona-sketch.github.io/Dieta_vacunacio-n_Citocinas/heatmap_luminex_altair_anotado_integrativo.html

## Autor

Pere-Joan Cardona
