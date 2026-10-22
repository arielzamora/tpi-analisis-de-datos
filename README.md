# TPI – Análisis de Datos: Telco Customer Churn

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/arielzamora/tpi-analisis-de-datos/blob/main/notebooks/TPI_Analisis_de_Datos.ipynb)

Trabajo Práctico Integrador de **Introducción al Análisis de Datos** – Tecnicatura Universitaria en Programación, UTN Avellaneda.

## Problema de negocio

Una empresa de telecomunicaciones quiere reducir el **churn** (la fuga de clientes). Con el dataset público [Telco Customer Churn](https://www.kaggle.com/datasets/blastchar/telco-customer-churn) (Kaggle, 7043 clientes y 21 variables) buscamos:

1. Entender qué características (contrato, antigüedad, forma de pago, servicios, cargos) se asocian con que un cliente abandone.
2. Construir un modelo de clasificación que estime la probabilidad de churn de cada cliente.

La variable objetivo es `Churn` (`Yes` / `No`). Hipótesis de partida: el contrato mes a mes, la poca antigüedad y el pago con *electronic check* se asocian con más fuga. El detalle está en el notebook `01_prep`.

## Integrantes

| Integrante | Rol | Notebook |
|---|---|---|
| _Nombre 1_ | Ingesta & Data Prep | `01_prep.ipynb` |
| _Nombre 2_ | EDA | `02_eda.ipynb` |
| _Nombre 3_ | Modelado | `03_modelado.ipynb` |
| _Nombre 4_ | _A definir (informe ejecutivo / revisión / modelado)_ | `docs/INFORME_EJECUTIVO.pdf` |

> Completar nombres y ajustar la división de tareas.

## Stack

Python · Pandas · NumPy · Matplotlib · Seaborn · Scikit-Learn · Jupyter / Google Colab

## Estructura del repositorio

```
tpi-analisis-de-datos/
├── data/
│   ├── raw/                  # CSV original de Kaggle, sin modificar
│   └── processed/            # telco_limpio.csv (salida de 01_prep)
├── notebooks/                # notebooks de trabajo + TPI_Analisis_de_Datos.ipynb final
├── docs/                     # INFORME_EJECUTIVO.pdf
└── README.md
```

## Cómo explorar el proyecto

1. **Entender los datos limpios:** abrir `notebooks/01_prep.ipynb`. Explica cada decisión de limpieza y termina con el **contrato de datos** (columnas, tipos y valores posibles de `telco_limpio.csv`).
2. **Usar el dataset limpio** en EDA o Modelado: leer `data/processed/telco_limpio.csv` y restaurar los tipos `category` con el código de la sección 10 de `01_prep`.
3. **Ejecutar en Colab:** abrir el notebook desde el badge. Descarga el CSV desde GitHub; no hace falta subir archivos.
4. **Ejecutar en local:**

   ```bash
   python -m venv .venv
   .venv\Scripts\activate            # en macOS/Linux: source .venv/bin/activate
   pip install pandas numpy matplotlib seaborn scikit-learn jupyter
   jupyter notebook notebooks/01_prep.ipynb
   ```

## Flujo de trabajo

- Cada integrante trabaja **en su propio notebook** (`01_prep`, `02_eda`, `03_modelado`) y **en su propia branch** (por ejemplo `feat/data-prep`, `feat/eda`, `feat/modelado`).
- Los cambios llegan a `main` mediante Pull Request, revisado por al menos otra persona.
- Al validar cada etapa se **consolida** su contenido en `notebooks/TPI_Analisis_de_Datos.ipynb`, que es la entrega final.
- Convenciones de commits: `feat:` (funcionalidad/análisis), `data:` (datos), `docs:` (documentación), `chore:` (estructura y configuración).
