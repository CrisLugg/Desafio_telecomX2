# Desafío Telecom X2

Este repositorio contiene el archivo **Desafio_telecomX2.ipynb**, donde se realiza un análisis exploratorio y preprocesamiento de datos para un problema de churn (abandono de clientes) en telecomunicaciones.

## Descripción

El notebook incluye los siguientes pasos principales:

- **Carga de datos**: Se utiliza pandas para cargar el archivo `datos_tratados.csv` en un DataFrame.
- **Visualización inicial**: Inspección de las primeras filas para conocer la estructura y el contenido de los datos.
- **Limpieza de datos**: Eliminación de columnas irrelevantes, como el identificador (ID).
- **Codificación de variables**: Transformación de variables categóricas en variables dummy utilizando `pd.get_dummies`, facilitando así el uso de modelos de machine learning.
- **Preparación para modelado**: El dataset resultante está listo para ser usado en algoritmos de predicción y análisis.

## Estructura de los datos

El dataset contiene información relevante sobre clientes de una empresa de telecomunicaciones, con variables como:

- **Churn**: Si el cliente abandonó la empresa.
- **Datos demográficos**: Género, edad, dependientes, etc.
- **Servicios contratados**: Internet, teléfono, soporte técnico, etc.
- **Facturación**: Cargo mensual, total y diario.
- **Método de pago** y tipo de contrato.

## Uso

Para ejecutar este notebook:

1. Sube el archivo `datos_tratados.csv` al entorno donde vas a ejecutar el notebook (por ejemplo, Google Colab).
2. Ejecuta las celdas paso a paso para reproducir el preprocesamiento y la exploración de los datos.
3. Utiliza el DataFrame preprocesado (`data_encoded`) como entrada para tus modelos de machine learning.

## Requisitos

- Python 3.x
- Pandas

Puedes instalar pandas ejecutando:
```bash
pip install pandas
```

## Ejemplo de uso

```python
import pandas as pd

# Cargar datos
file_path = '/content/datos_tratados.csv'
data = pd.read_csv(file_path)

# Preprocesamiento (eliminación de columnas no útiles)
data_cleaned = data.drop(columns=['ID'])

# Codificación
data_encoded = pd.get_dummies(data_cleaned, drop_first=True)

# Ahora puedes utilizar data_encoded para tus modelos
```

## Autor

[CrisLugg](https://github.com/CrisLugg)

---

> ¡No dudes en contribuir con mejoras o ideas adicionales!
