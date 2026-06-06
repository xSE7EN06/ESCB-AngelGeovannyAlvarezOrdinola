# Extracción del Conocimiento de Bases de Datos

Este repositorio contiene las prácticas, laboratorios y proyectos desarrollados durante el curso de Extracción del Conocimiento de Bases de Datos. Todo el código, la documentación y los análisis estadísticos han sido diseñados siguiendo altos estándares académicos y metodologías formales de la Ciencia de Datos.

## 🎓 Información Académica

- **Alumno:** Angel Geovanny Alvarez Ordinola
- **Materia:** Extracción del Conocimiento de Bases de Datos
- **Cuatrimestre:** 9B - IDGS (Ingeniería en Desarrollo y Gestión de Software)

## 🎯 Objetivo General
Aplicar técnicas de minería de datos, limpieza, transformación y análisis exploratorio (EDA) utilizando Python y sus librerías científicas. El objetivo es identificar patrones ocultos en grandes volúmenes de datos y traducir estos descubrimientos matemáticos en conocimiento accionable para la toma de decisiones empresariales.

## 📁 Estructura del Repositorio

```text
ESCB-AngelGeovannyAlvarezOrdinola/
│
├── Notebooks/               # Contiene los Jupyter Notebooks con el análisis paso a paso
│   ├── Lab01.ipynb          # Práctica introductoria
│   ├── Lab02.ipynb          # Fundamentos de Pandas
│   ├── Lab03.ipynb          # Limpieza de datos avanzada
│   ├── Lab04.ipynb          # Análisis descriptivo y modelo DIKW
│   ├── Lab05.ipynb          # Visualización de datos (Matplotlib & Seaborn)
│   ├── Lab06.ipynb          # Extracción de características
│   ├── Lab07.ipynb          # Práctica de repaso
│   ├── Lab09.ipynb          # Inferencia estadística
│   └── Lab10.ipynb          # Proyecto integrador
│
├── DataSet/                 # Archivos CSV crudos y procesados
│   ├── Data_Limpio_Factura.csv
│   ├── dataset_sucio_practica.csv
│   ├── netflix_titles.csv
│   ├── test.csv
│   └── ventas-por-factura.csv
│
├── Images/                  # Recursos visuales y evidencias
│   ├── graficas/            # Exportación de las gráficas más relevantes
│   └── evidencias/          # Capturas de pantalla de ejecución
│
├── Docs/                    # Documentación analítica extensa
│   └── conclusiones.md      # Reflexión final de la materia
│
├── CHANGELOG.md             # Registro de cambios y mejoras implementadas
├── AUDITORIA_REPOSITORIO.md # Cumplimiento estricto de la rúbrica de evaluación
└── README.md                # Este archivo
```

## 🧠 Aplicación del Modelo DIKW
A lo largo de este repositorio se evidencia la transformación de la materia prima hacia el valor empresarial utilizando la pirámide **DIKW**:
- **Data (Datos):** Ingesta de los archivos `.csv` en su forma original y desestructurada.
- **Information (Información):** Procesos exhaustivos de limpieza de datos (Data Wrangling), eliminación de duplicados e imputación de valores nulos para estructurar la información con Pandas.
- **Knowledge (Conocimiento):** Aplicación de análisis estadístico y visualización de datos (gráficas de dispersión, diagramas de caja) para reconocer tendencias, anomalías y correlaciones.
- **Wisdom (Sabiduría):** Interpretación cualitativa de cada gráfica en los notebooks, culminando en conclusiones formales orientadas a la estrategia de negocio y la toma de decisiones informada.

## 🗄️ Datasets Utilizados

| Nombre del Archivo | Descripción Principal | Uso Principal |
| :--- | :--- | :--- |
| `netflix_titles.csv` | Catálogo completo de películas y series en la plataforma Netflix, incluyendo directores, cast, país de origen, año y clasificación. | Análisis exploratorio de tendencias de contenido de streaming. |
| `dataset_sucio_practica.csv` | Archivo con múltiples inconsistencias (nulos, formatos incorrectos, duplicados). | Laboratorio exhaustivo de limpieza de datos (Data Cleansing). |
| `ventas-por-factura.csv` | Registro transaccional de ventas, precios, unidades y fechas de una compañía de retail. | Análisis de facturación, ingresos temporales y comportamiento de clientes. |
| `Data_Limpio_Factura.csv` | Versión procesada, limpia y estructurada de los datos de facturación. | Punto de partida para inferencia estadística avanzada y Machine Learning. |
| `test.csv` | Archivo secundario utilizado para pruebas de validación de carga y concatenación en Pandas. | Demostraciones de manipulación de DataFrames. |

## 🛠️ Herramientas Tecnológicas

* **Python 3.x:** Lenguaje principal de análisis.
* **Pandas:** Estructuración, limpieza y manipulación de DataFrames.
* **NumPy:** Computación numérica y álgebra lineal.
* **Matplotlib:** Visualización de datos y creación de gráficas estáticas 2D.
* **Seaborn:** Visualización estadística avanzada con interfaces atractivas.
* **Jupyter Notebook:** Entorno interactivo de desarrollo y documentación.

## 🚀 Instrucciones de Ejecución

1. **Clonar el repositorio:**
   ```bash
   git clone https://github.com/TuUsuario/ESCB-AngelGeovannyAlvarezOrdinola.git
   cd ESCB-AngelGeovannyAlvarezOrdinola
   ```
2. **Crear entorno virtual (Recomendado):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # En Windows: venv\Scripts\activate
   ```
3. **Instalar dependencias necesarias:**
   ```bash
   pip install pandas numpy matplotlib seaborn jupyter
   ```
4. **Ejecutar el servidor de Jupyter:**
   ```bash
   jupyter notebook
   ```
5. Navega a la carpeta `Notebooks/` en tu navegador y ejecuta las celdas secuencialmente (Shift + Enter).

## 📊 Principales Hallazgos y Capturas
*Las capturas de ejecución y las gráficas resultantes más importantes se encuentran debidamente alojadas en `Images/graficas` y documentadas exhaustivamente dentro de cada Jupyter Notebook en la sección de "Interpretación de Resultados".*

## 💡 Historial de Commits Sugerido
Para evidenciar la metodología de trabajo progresiva e iterativa recomendada por buenas prácticas de ingeniería, se sugiere seguir esta convención de versionamiento:
- `docs: update README with DIKW model and academic objectives`
- `refactor: reorganize project structure and rename folders to standard conventions`
- `feat: audit and implement descriptive analysis in Lab01-Lab05 notebooks`
- `style: add academic interpretation and markdown documentation to Lab06-Lab10`
- `docs: generate final conclusions and changelog`
