# Portafolio · Minería de Datos (IEI097)

Laboratorios y actividades del curso de **Minería de Datos**, Ingeniería en Informática, Santo Tomás. Autor: Miguel Chura ([@MikiDu88](https://github.com/MikiDu88)).

## Laboratorios

| Actividad | Tema | Técnicas | Notebook |
|---|---|---|---|
| 2.10 | Clustering | K-means, clustering jerárquico aglomerativo | [`clustering-kmeans-jerarquico`](clustering-kmeans-jerarquico/Actividad_2_10_clustering.ipynb) |

> Si tienes más actividades en este repositorio, agrega una fila por cada una con el mismo formato.

---

## Actividad 2.10 · Clustering: K-means y jerárquico

Notebook de Google Colab con dos ejercicios, ejecutado de principio a fin con las salidas visibles.

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/MikiDu88/1.9/blob/main/clustering-kmeans-jerarquico/Actividad_2_10_clustering.ipynb)

### Ejercicio 1 · K-means: segmentación de clientes
- **Datos:** [Mall Customer Segmentation](https://www.kaggle.com/datasets/vjchoudhary7/customer-segmentation-tutorial-in-python) (200 clientes).
- **Variables del modelo:** ingreso anual y puntaje de gasto, estandarizadas.
- **Elección de k:** inercia (codo), silueta y estabilidad entre semillas (ARI).
- **Resultado:** perfiles por segmento en unidades originales, nombre de cada segmento y una acción propuesta.

### Ejercicio 2 · Clustering jerárquico: ¿con qué países se parece Chile?
- **Datos:** [Unsupervised Learning on Country Data](https://www.kaggle.com/datasets/rohan0301/unsupervised-learning-on-country-data) (subconjunto de ~30 países que incluye a Chile).
- **Método:** dendrogramas con enlaces `average` y `ward`, con y sin estandarizar.
- **Resultado:** corte justificado con línea sobre el dendrograma, países de cada grupo y comparación con K-means (tabla de contingencia e ARI).

### Cómo reproducirlo
1. Abre el notebook en Colab con el botón de arriba.
2. En **Secretos** de Colab, agrega `KAGGLE_USERNAME` y `KAGGLE_KEY` con acceso al notebook.
3. Ejecuta **Entorno de ejecución → Reiniciar sesión y ejecutar todo**.

> Nunca subas tu token de Kaggle ni `kaggle.json` al repositorio.

### Librerías
`pandas`, `numpy`, `matplotlib`, `seaborn`, `scikit-learn`, `scipy`, `kagglehub`.

### Nota de interpretación
Un grupo no es un ranking ni una verdad oculta en los datos: solo vale bajo las variables, la estandarización y la distancia elegidas.
