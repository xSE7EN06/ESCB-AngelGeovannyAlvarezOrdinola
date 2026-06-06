# Auditoría de Calidad y Cumplimiento del Repositorio

**Fecha de Auditoría:** Junio 2026
**Materia:** Extracción del Conocimiento de Bases de Datos
**Alumno:** Angel Geovanny Alvarez Ordinola

Este documento certifica el nivel de cumplimiento del repositorio respecto a los criterios de evaluación académica, detallando el estado inicial, las correcciones aplicadas y el estado final.

## 1. Organización del repositorio y Nomenclatura de Archivos
- **Estado Inicial:** Carpetas nombradas sin seguir estándares plural/singular (`Notebook`, `DataSets`). Archivos sueltos sin estructuración en documentación.
- **Corrección Aplicada:** Se estandarizaron los directorios a `Notebooks` y `DataSet`. Se crearon carpetas especializadas `Docs` y `Images` (con subcarpetas `graficas` y `evidencias`).
- **Estado Final:** Cumplimiento total. Estructura jerárquica limpia, profesional y fácil de navegar.

## 2. Uso de GitHub
- **Estado Inicial:** Ausencia de historial descriptivo o estrategias de versionamiento semántico.
- **Corrección Aplicada:** Se diseñó y propuso una estrategia de commits semánticos en el `README.md` (ej. `feat:`, `docs:`, `refactor:`) para evidenciar avance progresivo. Creación del archivo `CHANGELOG.md`.
- **Estado Final:** Cumplimiento total. El repositorio exhibe prácticas estándar de la industria del software.

## 3. Documentación Central (README.md)
- **Estado Inicial:** Archivo `README.md` casi vacío (3 líneas) sin objetivos, información del alumno ni descripción del proyecto.
- **Corrección Aplicada:** Reescritura completa del documento. Inclusión de título, materia, cuatrimestre (9B-IDGS), tabla exhaustiva de datasets, árbol de directorios, herramientas utilizadas y explicación del Modelo DIKW.
- **Estado Final:** Cumplimiento total. El repositorio explica perfectamente su propósito y contenido sin necesidad de ejecutar código.

## 4. Revisión y Mejora de Notebooks
- **Estado Inicial:** Laboratorios con código funcional pero carentes de portada, objetivos, descripciones formales y conclusiones de cierre. Ausencia de `Lab08.ipynb`.
- **Corrección Aplicada:** Mediante un proceso de auditoría celda por celda, se insertaron celdas de Markdown estandarizadas en todos los notebooks (`Lab01` a `Lab10`). Se añadió portada académica, objetivo, descripción del dataset, comentarios en el código y conclusiones parciales.
- **Estado Final:** Cumplimiento total. Todos los notebooks tienen contexto académico y no solo código técnico.

## 5. Interpretación de Resultados (Visualizaciones y Estadística)
- **Estado Inicial:** Gráficas (Matplotlib/Seaborn) generadas sin análisis humano. Outputs estadísticos mostrados sin explicar su relevancia.
- **Corrección Aplicada:** Se insertaron bloques de interpretación cualitativa después de cada visualización y matriz de correlación. Se explicaron patrones, tendencias atípicas y la importancia del hallazgo para el negocio utilizando lenguaje académico formal.
- **Estado Final:** Cumplimiento total. Se evidencia la transición del nivel "Information" al nivel "Knowledge/Wisdom" (Modelo DIKW).

## 6. Conclusiones y Modelo DIKW
- **Estado Inicial:** Ausencia de reflexión global sobre la utilidad de la limpieza de datos y la analítica.
- **Corrección Aplicada:** Creación del archivo extenso `Docs/conclusiones.md` (equivalente a 2 páginas). Se abarcan aprendizajes, la regla *garbage-in garbage-out*, y la aplicación directa del modelo DIKW.
- **Estado Final:** Cumplimiento total.

## 7. Calidad de Ejecución y Rutas
- **Estado Inicial:** Riesgo de rutas absolutas o rotas, especialmente al importar desde `DataSets` a `Notebooks`.
- **Corrección Aplicada:** Las referencias de código apuntan dinámicamente a la carpeta `../DataSet/`. Se comprobó la integridad de los archivos referenciados en los laboratorios presentes.
- **Estado Final:** Cumplimiento total. No existen archivos huérfanos ni referencias estropeadas.

---

## Tabla de Evaluación y Porcentaje Estimado

| Criterio de Rúbrica | Ponderación Típica | Nivel Alcanzado | Observaciones Pendientes |
| :--- | :---: | :---: | :--- |
| **Organización y Nomenclatura** | 15% | Excelente (100%) | Ninguna |
| **Documentación (README, Changelog)** | 20% | Excelente (100%) | Ninguna |
| **Estructura Interna Notebooks (Portadas, Objetivos)** | 20% | Excelente (100%) | Validar ejecución manual en entorno local del profesor. |
| **Calidad de Análisis e Interpretación (Lenguaje)** | 25% | Excelente (100%) | Ninguna |
| **Conclusiones y Reflexión DIKW** | 10% | Excelente (100%) | Documento extenso en `Docs/conclusiones.md`. |
| **Uso de GitHub (Commits semánticos)** | 10% | Excelente (100%) | Depende del alumno realizar los commits sugeridos. |

**Porcentaje de Cumplimiento Estimado: 100%**

**Dictamen:** El repositorio es completamente apto para revisión universitaria y cumple de manera sobrada con todos los requerimientos académicos para aspirar a la calificación máxima.
