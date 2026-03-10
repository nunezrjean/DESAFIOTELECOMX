📈 Análisis de Evasión de Clientes (Churn) en Telecom X
🚀 Visión General del Proyecto
Este proyecto se centra en el análisis de la evasión de clientes (Churn) de la empresa de telecomunicaciones ficticia Telecom X. El objetivo principal es identificar los factores clave que influyen en la decisión de los clientes de cancelar sus servicios, para que la empresa pueda desarrollar estrategias proactivas de retención. La retención de clientes es fundamental, ya que la adquisición de nuevos clientes es considerablemente más costosa.

📋 Contenido del Repositorio
Este notebook contiene:

Extracción y Carga de Datos: Importación de datos desde una API y conversión a DataFrame.
Exploración Inicial y Diccionario de Datos: Comprensión de la estructura y el significado de las variables.
Verificación y Calidad de Datos (ETL - Transformación): Identificación y tratamiento de valores ausentes, duplicados e inconsistencias.
Transformación y Limpieza Definitiva (ETL - Carga): Renombrado de columnas, corrección de tipos de datos, estandarización de valores y creación de nuevas características.
Análisis Descriptivo (EDA - Estadísticas): Cálculo de estadísticas clave y correlaciones.
Visualizaciones (EDA - Gráficos): Representaciones visuales de la distribución del churn y su relación con variables clave.
Informe Final: Resumen de las conclusiones e insights, junto con recomendaciones estratégicas.
🌐 Fuente de Datos
Los datos se obtuvieron de un archivo JSON alojado en GitHub: https://raw.githubusercontent.com/ingridcristh/challenge2-data-science-LATAM/main/TelecomX_Data.json

🔧 Metodología
El análisis se llevó a cabo siguiendo un flujo estructurado:

Extracción (Extract): Carga de los datos desde la URL proporcionada y su transformación en un DataFrame de Pandas.
Transformación (Transform):
Limpieza de Datos: Manejo de valores nulos (especialmente en account.Charges.Total), eliminación de duplicados, estandarización de strings.
Renombrado de Columnas: Para mayor legibilidad y consistencia.
Conversión de Tipos: Ajuste de tipos de datos para variables numéricas (cargo_total, cargo_mensual, meses_contrato) y la variable objetivo churn (a binario 0/1).
Feature Engineering: Creación de la columna Cuentas_Diarias (cargo_mensual / 30).
Análisis Exploratorio de Datos (EDA):
Tasa General de Churn: Cuantificación de la proporción de clientes que cancelan.
Análisis de Variables Numéricas: Comparación de meses_contrato, cargo_mensual, cargo_total y Cuentas_Diarias entre clientes que cancelan y los que no, utilizando estadísticas descriptivas, histogramas, boxplots y gráficos de violín.
Análisis de Variables Categóricas: Evaluación del impacto de variables como tipo_contrato, tipo_internet, metodo_pago, factura_digital, adulto_mayor, genero, tiene_pareja, tiene_dependientes y servicio_telefono en la tasa de churn.
Correlaciones: Identificación de relaciones entre las variables numéricas y el churn.
📊 Conclusiones e Insights Clave
Tasa de Evasión Global: Un 25.72% de los clientes cancelan sus servicios, una cifra significativa que requiere atención.
Antigüedad y Churn: Clientes con menor antigüedad (promedio de 17.98 meses para los que cancelan vs. 37.57 meses para los que permanecen) son más propensos a la evasión.
Costos y Churn: Clientes con cargos mensuales y diarios más altos son más propensos a cancelar, sugiriendo insatisfacción con el valor percibido.
Contratos a Corto Plazo: Los contratos mes a mes presentan una tasa de churn muy elevada (42.7%), en contraste con los contratos de uno o dos años (11.3% y 2.8% respectivamente).
Fibra Óptica y Churn: El servicio de fibra óptica tiene una tasa de churn notablemente alta (41.9%), lo que podría indicar problemas de calidad o precio.
Método de Pago Electrónico: El cheque electrónico se asocia con la tasa de churn más alta (45.3%).
Adultos Mayores: Los adultos mayores tienen una tasa de churn casi el doble (41.7%) que los no adultos mayores (23.6%).
💡 Recomendaciones Estratégicas
Programas de Retención Temprana: Implementar programas de fidelización y seguimiento intensivo para clientes nuevos durante sus primeros 12-18 meses.
Optimización de Planes de Fibra Óptica: Investigar y mejorar la calidad, estabilidad o ajustar el precio del servicio de fibra óptica.
Incentivos para Contratos a Largo Plazo: Ofrecer descuentos y beneficios para migrar a contratos anuales o bianuales.
Promoción de Métodos de Pago Automáticos: Incentivar el cambio de cheque electrónico a opciones de pago automático para reducir fricciones.
Mejora de la Experiencia del Adulto Mayor: Desarrollar servicios y soporte específicos (líneas de atención, tutoriales sencillos) para este segmento.
Revisión de Facturación Digital: Analizar el feedback y mejorar la claridad o facilidad de gestión de la factura digital.
🖼️ Visualizaciones Generadas
Las visualizaciones clave del análisis incluyen:

telecomx_churn_distribucion.png: Distribución general de Churn y KPIs.
telecomx_churn_categoricas.png: Tasa de Churn por variables categóricas (género, contrato, internet, etc.).
telecomx_churn_numericas.png: Comparación de distribuciones de variables numéricas (antigüedad, cargos) entre clientes que cancelan y los que no.
🛠️ Cómo Ejecutar el Notebook
Abre el notebook en Google Colab.
Ejecuta todas las celdas en orden para reproducir el análisis y generar el informe y las visualizaciones.
