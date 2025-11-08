
# Mortalidad Colombia 2019 - Dashboard (Actividad 4)

Aplicación Dash + Plotly para analizar mortalidad en Colombia (2019). Contiene mapas, series temporales, tablas y gráficos interactivos.




## Integrantes

 - Aldo Giuliano Zabala Ruocco
 - Johny Barbosa
 - Lucas Vélez


## Introducción

Esta aplicación explora la mortalidad en Colombia durante el año 2019. Provee visualizaciones interactivas (mapa coroplético, series temporales, barras, pastel, histogramas y tablas) que permiten inspeccionar la distribución espacial, temporal y demográfica de las defunciones registradas en el año.

El objetivo es facilitar el análisis exploratorio de los datos de mortalidad, identificar patrones por departamento, mes, sexo, grupo de edad y causas de muerte, y ofrecer una herramienta accesible para la comunidad académica y técnica.


## Objetivos

- Visualizar la distribución de muertes por departamento (mapa coroplético).

- Analizar variaciones mensuales de mortalidad (gráfico de líneas).

- Identificar las 5 ciudades más violentas considerando homicidios (cod. X9x y relacionados).

- Mostrar las 10 ciudades con menor mortalidad (gráfico circular).

- Presentar una tabla con las 10 principales causas de muerte (código, nombre, total).

- Comparar muertes por sexo en cada departamento (barras apiladas).

- Explorar la distribución por grupos de edad (histograma).


## Estructura del proyecto

mortalidad-2019-dash/
- app.py 
- requirements.txt 
- README.md 
- data/
  - NoFetal2019.xlsx 
  - Divipola.xlsx municipios
  - codigosDeMuerte.xlsx 
  - colombia_departamentos.geojson 
- assets/
  - style.css 
- .gitignore




## Requisitos

- python -- 3.12
- dash -- 2.9.3
- dash-bootstrap-components -- 1.4.1
- pandas -- 2.2.2
- numpy -- 1.26.1
- plotly -- 5.20.0
- openpyxl -- 3.1.2
- gunicorn -- 20.1.0

Instalas con:

-  pip install -r requirements.txt



## Despliegue

Pasos seguidos para desplegar la aplicación en Render:

- Crear un repositorio en GitHub y subir el proyecto completo.
- En Render, crear un nuevo Web Service conectado al repositorio.
- Configurar los siguientes parámetros:
  - Build Command: pip install -r requirements.txt
  - Start Command: gunicorn app:server --bind 0.0.0.0:$PORT
- Esperar el proceso de compilación e inicio.
- Render generará una URL pública donde estará disponible la aplicación.




## Software uUilizado

- Lenguaje: Python 3.9+
- Framework principal: Dash (Plotly)
- Librerías: Pandas, NumPy, Plotly Express, Dash Bootstrap Components
- Despliegue: Render (PaaS)
- Edición y control de versiones: Git y GitHub


## Instalación local

1. Clonar el repositorio:
  - git clone <URL_DEL_REPOSITORIO>
  - cd mortalidad-2019-dash

2. Crear entorno virtual y activarlo:
  - python3 -m venv venv
  - source venv/bin/activate # En macOS/Linux

  - venv\Scripts\activate. # En windows

3. Instalar dependencias:
  - pip install -r requirements.txt

4. Ejecutar la aplicación:
  - python3 app.py

5. Abrir en el navegador:
  - http://127.0.0.1:8050/



## Visualizaciones con explicaciones de los resultados

1. Mapa: Muertes por departamento

<img width="534" height="291" alt="Image" src="https://github.com/user-attachments/assets/8a278d97-42fb-4fc5-b4c1-5301b925b559" />

Representa la distribución total de muertes en 2019. Los departamentos con mayor población (Antioquia, Bogotá, Valle del Cauca) muestran los valores más altos.

2. Gráfico de líneas: Muertes por mes

<img width="538" height="283" alt="Image" src="https://github.com/user-attachments/assets/12545e8d-c4f2-4ba2-9020-1f30add1f346" />

Muestra la variación mensual del número de defunciones, evidenciando posibles picos estacionales o comportamientos anómalos.

3. Gráfico de barras: Ciudades más violentas

<img width="534" height="288" alt="Image" src="https://github.com/user-attachments/assets/d4fdcfd7-ae9e-4d8c-859b-cc79fed4a160" />

Visualiza las 5 ciudades con mayor número de homicidios (códigos X95 y relacionados). Permite identificar focos urbanos de violencia.

4. Gráfico circular: Ciudades con menor mortalidad

<img width="531" height="237" alt="Image" src="https://github.com/user-attachments/assets/af44be0b-62e6-4810-868a-fbf4467d672f" /> 

Destaca las 10 ciudades con menor número total de muertes. Generalmente corresponden a municipios rurales con poca población.

5. Tabla: Principales causas de muerte

<img width="532" height="239" alt="Image" src="https://github.com/user-attachments/assets/d0c7d708-ea71-409d-81e8-68139f6536e8" /> 

Lista las 10 causas más frecuentes, con su código, nombre y número de casos. Facilita la identificación de los principales problemas de salud pública.

6. Barras apiladas: Muertes por sexo y departamento

<img width="535" height="294" alt="Image" src="https://github.com/user-attachments/assets/6294434f-ac7b-4d53-8572-85c0cb9361a7" /> 

Compara la mortalidad masculina y femenina por región. Identifica diferencias demográficas y de comportamiento.

7. Histograma: Distribución por grupo de edad

<img width="532" height="270" alt="Image" src="https://github.com/user-attachments/assets/4e0892da-6941-40dc-aef8-3e041f64b886" /> 

Agrupa las muertes según GRUPO_EDAD1 para observar los patrones de mortalidad a lo largo del ciclo de vida.

