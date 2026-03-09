---

# Telecom X LATAM – Análisis Estratégico de Deserción de Clientes
Proyecto de análisis end-to-end enfocado en identificar clientes de alto riesgo y traducir hallazgos estadísticos en decisiones estratégicas de retención.

---

## Problema de Negocio

Telecom X presenta una **tasa de churn del 26.6%**, es decir, **1 de cada 4 clientes abandona la empresa**.
En modelos de suscripción, la deserción impacta directamente en:

  - Estabilidad de ingresos
  - Eficiencia del costo de adquisición (CAC)
  - Rentabilidad a largo plazo

El objetivo del proyecto fue identificar los principales impulsores de la deserción y proponer estrategias de retención basadas en datos.

---

## Enfoque Analítico

El proyecto sigue una metodología estructurada:

  1. Extracción de datos (API en formato JSON)
  2. Limpieza y transformación
  3. Análisis Exploratorio (EDA)
  4. Análisis estadístico y correlacional
  5. Traducción de hallazgos a insights de negocio
  6. Recomendaciones estratégicas

  ---

## Hallazgos Clave

- **El Tipo de Contrato es el Predictor Más Fuerte**
   El contrato mensual concentra la mayor tasa de deserción.
   Los contratos anuales y bienales funcionan como ancla de permanencia.

- **El Ciclo de Vida Temprano es Crítico**
   Los clientes dentro de los primeros 6 meses presentan mayor riesgo.
   Superar el umbral de 12 meses reduce significativamente la probabilidad de fuga.

- **Paradoja del Cliente Premium**
   Los clientes que pagan más de $70 mensuales presentan mayor tasa de churn.
   El cliente de alto valor es más exigente y menos tolerante a fallos
   
- **Segmento Senior (+60) es el más Vulnerable**
   Presenta la tasa de deserción más alta (>40%).
   
- **Fricción en el Método de Pago**
   Los métodos manuales (Cheque Electrónico) aumentan la probabilidad de abandono.
   
- **Servicios Adicionales Reducen la Deserción**
   Soporte Técnico y Seguridad Online actúan como herramientas reales de fidelización.
  
  ---

## Indicadores Cuantitativos Destacados

- Tasa de churn: 26.6%
- Contrato mensual = mayor concentración de fuga
- Correlación negativa fuerte entre antigüedad y deserción (mientras más tiempo permanece el cliente, menor es el riesgo de fuga). 
- El ingreso acumulado depende de la retención, no del precio
- Primeros 6 meses = ventana crítica de intervención

---

## Recomendaciones Estratégicas

1. Conversión de contratos mensuales a anuales
2. Programa de retención en los primeros 6 meses
3. Programa de blindaje para clientes de alto ticket
4. Soporte especializado para segmento senior
5. Incentivo a pago automático

---

## Conclusión Final
  - La rentabilidad de Telecom X no depende de subir precios. Depende de retener más tiempo a los clientes correctos. ***El foco no es adquirir más clientes, el foco es moverlos del Mes 1 al Año 1.***
  - La prioridad no es bajar precios, sino aumentar el valor percibido de quedarse. ***Fortalecer el soporte a seniors, incentivar pagos automáticos y proteger los primeros 6 meses, hará que la empresa deje de ser un "comodity" reemplazable para convertirse en un socio esencial del hogar del cliente.***

---

## Tecnologías utilizadas

- **Python 3**
- **Pandas**: manipulación y análisis de datos.
- **NumPy**: operaciones numéricas.
- **Requests**: consumo de APIs y descarga de datos. 
- **Matplotlib**: visualización de datos estática.
- **Seaborn**: visualización de gráficos estadísticos atractivos, complejos e informativos.
- **Plotly**: visualización de datos interactiva y dinámica.
- **Scipy**: análisis estadístico descriptivo e inferencial.
- **Google Colab**: entorno de ejecución y colaboración.

---

## Datos

Los datos fueron obtenidos desde la API pública de Telecom X en formato JSON.
Incluyen información demográfica, servicios contratados y estado de churn de los clientes.  

Fuente:[API de Telecom X](https://raw.githubusercontent.com/alura-cursos/challenge2-data-science-LATAM/main/TelecomX_Data.json) 

--- 
### Diccionario de Datos

| Variable         | Descripción                              |
| ---------------- | ---------------------------------------- |
| customerID       | Identificador único del cliente          |
| Churn            | Indica si el cliente abandonó la empresa |
| gender           | Género (masculino/femenino)              |
| SeniorCitizen    | Cliente mayor o igual a 65 años          |
| Partner          | Indica si tiene pareja                   |
| Dependents       | Indica si tiene dependientes             |
| tenure           | Meses de contrato                        |
| PhoneService     | Servicio telefónico                      |
| MultipleLines    | Más de una línea telefónica              |
| InternetService  | Tipo de servicio de internet             |
| OnlineSecurity   | Seguridad en línea                       |
| OnlineBackup     | Respaldo en línea                        |
| DeviceProtection | Protección del dispositivo               |
| TechSupport      | Soporte técnico                          |
| StreamingTV      | Servicio de TV                           |
| StreamingMovies  | Servicio de películas                    |
| Contract         | Tipo de contrato                         |
| PaperlessBilling | Facturación digital                      |
| PaymentMethod    | Método de pago                           |
| Charges.Monthly  | Cargo mensual                            |
| Charges.Total    | Total gastado                            |

---

## Visualizaciones

![Gráfico del Análisis Estadístico de las Variables Numéricas](/images/Gr%C3%A1fico%20del%20An%C3%A1lisis%20Estad%C3%ADstico%20de%20las%20Variables%20Num%C3%A9ricas.png)

![Distribución de la Evasión (Churn) de los Clientes](images/Distribuci%C3%B3n%20de%20la%20Evasi%C3%B3n%20(Churn)%20de%20los%20Clientes.png)

![Recuento de la evasión por variables categóricas](images/Recuento%20de%20la%20evasi%C3%B3n%20por%20variables%20categ%C3%B3ricas.png)

![Tasa de Deserción por Perfil y Género](images/Tasa%20de%20Deserci%C3%B3n%20por%20Perfil%20y%20G%C3%A9nero.png)

![Recuento de la evasión por variables numéricas](images/Recuento%20de%20la%20evasi%C3%B3n%20por%20variables%20num%C3%A9ricas.png)

![Comparativa de Deserción: Ciclo de Vida por Contrato](images/Comparativa%20de%20Deserci%C3%B3n%20Ciclo%20de%20Vida%20por%20Contrato.png)

![Análisis de correlación entre variables](images/An%C3%A1lisis%20de%20correlaci%C3%B3n%20entre%20variables.png)

[![Explorar Visualizaciones Interactivas](https://img.shields.io/badge/Explorar-Visualizaciones%20Interactivas-2563eb?style=for-the-badge&logo=plotly&logoColor=white)](https://mellifluous-boba-bed465.netlify.app/)

**Vista Previa:**
![Captura de visualizaciones interactivas](images/Visualizaciones%20interactivas.png)

---

## Contenido del proyecto

1. **Extracción**
   - Carga de los datos desde la API (JSON).
   - Extracción de datos agrupados.
   - Análisis de la estructura de los datos

2. **Transformación**
   - **Auditoría inicial:**: revisión de tipos de datos, valores nulos y duplicados.
   - **Corrección de Tipos**: conversión de account.Charges.Total a formato numérico (float).
   - **Manejo de Valores Faltantes**: eliminación de 235 registros con datos vacíos.
   - **Traducción y Estandarización**: traducción de columnas y categorías al español.
   - **Estandarización Binaria**: transformación de variables Sí/No a 1 y 0.
   - **Ingeniería de variables**: creación de cuentas_diarias para expresar el gasto mensual en base diaria.

3. **Carga y Análisis**
   El análisis incluyó:
    - **Estadísticas descriptivas**: media, mediana, moda y desviación estándar.
    - **Distribución de Churn**: evaluación de la tasa de deserción.
    - **Análisis por variables categóricas**: tipo de contrato, método de pago, tipo de internet, género, senior (+60), pareja y dependientes.
    - **Comparación de variables numéricas**: tiempo de contrato, total cobrado, valor mensual y cuentas diarias entre clientes que cancelaron y los que permanecieron.
    - **Visualizaciones**: gráficos de barras, histogramas, dispersión y matriz de correlación para identificar patrones y relaciones clave.
  
4. **Informe Final**
   - Introducción
   - Limpieza y Tratamiento de Datos
   - Análisis Exploratorio de Datos (EDA)
   - Conclusiones e Insights
   - Recomendaciones Estratégicas para Reducir la Deserción
   - Conclusión final

---

## Cómo usar este proyecto

1. Abrir el cuaderno en **[Google Colab](https://colab.research.google.com/github/fsoaresg/Desafio_Telecom_X_Latam/blob/main/Telecom_X_Latam.ipynb)**.
2. Ejecutar las celdas paso a paso para:
    - Importar los datos desde la API.
    - Realizar limpieza y transformación.
    - Generar análisis estadístico y visualizaciones.
3. Explorar los gráficos interactivos.
4. Analizar los insights y evaluar recomendaciones estratégicas.

---

## Estructura del repositorio

├── Telecom X_Latam.ipynb

├── README.md

├── 📂 images/

├── 📂 interactive/

---

## Competencias Demostradas y Posicionamiento Profesional

Este proyecto evidencia capacidad en:

  - Análisis de datos end-to-end
  - Interpretación estadística aplicada a negocio
  - Segmentación de clientes
  - Storytelling con datos
  - Visualización estratégica
  - Traducción de análisis técnico en decisiones ejecutivas
  - Identificar variables críticas en problemas reales de negocio
  - Priorizar acciones con impacto económico
  - Conectar análisis estadístico con estrategia corporativa
  - Comunicar hallazgos técnicos a nivel ejecutivo

---

## Autor

**Fátima Soares**  
Data Analyst | Enfoque en análisis estratégico y toma de decisiones basada en datos.
Especializada en transformar métricas operativas en insights ejecutivos accionables.
[GitHub](https://github.com/fsoaresg)

---

## Licencia

Este proyecto es de **uso educativo y demostrativo**, con base en un desafío de Alura Latam.

---
