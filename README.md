# Práctica en Colab: Análisis Predictivo

## Caso de estudio: ventas mensuales de una empresa de calzado (2020 – 2024)


| | |
|---|---|
| **Estudiante** | Hansel Andres Parra Enciso |
| **Programa** | Especialización en Analítica y Ciencia de Datos – Universidad de Cundinamarca |
| **CAI** | BUSSINES ANALYTICS |
| **Actividad** | Práctica en Colab: Análisis Predictivo – Taller de Analítica Predictiva Empresarial |
| **Fecha** | Octubre de 2026 |

## Descripción

Notebook de Google Colab que aplica **análisis predictivo** a las ventas mensuales de una empresa de calzado. A partir de 60 meses de datos históricos se construyen y comparan tres modelos que responden preguntas de negocio distintas, y con los modelos finales se proyectan las ventas de 2025 en tres escenarios de inversión.

| Pregunta | Técnica | Resultado principal (datos de prueba) |
|---|---|---|
| P1 – ¿Cómo afecta el presupuesto de marketing a las ventas? | Regresión lineal | R² = 0.945 · RMSE ≈ 318 · cada unidad invertida ≈ 1.58 unidades de ventas |
| P2 – ¿Qué factores determinan que se cumpla la meta de ventas? | Regresión logística | Accuracy = 94.4 % · AUC = 0.988 · factor clave: presupuesto |
| P3 – ¿Las ventas serán bajas, medias o altas? | Árbol de decisión | Accuracy = 88.9 % · importancia del presupuesto ≈ 96 % |
| P4 – ¿Qué modelo usar y cuándo? | Comparación de modelos | Regresión lineal como modelo principal; logística y árbol como apoyo |
| P5 – ¿Cuánto se podría vender en 2025? | Proyección por escenarios | Base ≈ 93,300 · Expansión (+10 %) ≈ 102,500 · Conservador (−10 %) ≈ 84,100 |

![Proyección 2025](img/proyeccion_2025.png)

## Contenido del notebook

1. Marco conceptual: análisis predictivo, diferencias con el descriptivo, proceso, técnicas y elementos clave de un modelo
2. Objetivos y preguntas de negocio
3. Preparación del entorno
4. Carga de datos
5. Exploración inicial
6. Limpieza y preparación de los datos
7. Análisis exploratorio (tendencia central, dispersión y correlaciones)
8. Selección de variables relevantes
9. Modelo 1 – Regresión lineal
10. Modelo 2 – Regresión logística
11. Modelo 3 – Árbol de decisión
12. Comparación de modelos
13. Proyección de escenarios para 2025
14. Síntesis de resultados
15. Conclusiones
16. Referencias (APA 7)

## Estructura del repositorio

```
analitica-predictiva-zapatos/
├── notebooks/
│   └── Analisis_Predictivo_Zapatos.ipynb   # Notebook documentado y ejecutado
├── datos/
│   └── S12_dataset_ventas_zapatos.xlsx     # Dataset del taller (60 meses)
├── img/
│   └── proyeccion_2025.png                 # Gráfico de la proyección
├── requirements.txt                        # Librerías para ejecutar fuera de Colab
└── README.md
```

## Cómo ejecutarlo

**En Google Colab (recomendado):** haz clic en el botón *Abrir en Colab* y luego en *Entorno de ejecución → Ejecutar todas*. El notebook lee el dataset directamente desde la carpeta `datos/` de este repositorio.

**En un equipo local:**

```bash
pip install -r requirements.txt
jupyter notebook notebooks/Analisis_Predictivo_Zapatos.ipynb
```

## Dataset

| Variable | Rol | Descripción |
|---|---|---|
| `Año`, `Mes` | Identificación temporal | Periodo del registro |
| `Ventas_mensuales` | Dependiente | Ventas totales del mes |
| `Presupuesto_marketing` | Independiente | Inversión mensual en marketing |
| `Nuevos_clientes` | Independiente | Clientes nuevos captados en el mes |
| `Promociones_aplicadas` | Independiente | 1 = hubo promociones, 0 = no hubo |
| `Opinion_clientes` | Independiente | Calificación de los clientes (1 a 5) |

Dataset sintético entregado con la guía del taller. Los años de los últimos 12 registros venían como 2068 – 2079 y se corrigieron a 2024 en el notebook (sección 6).

## Referencias

## 16. Referencias

Google Cloud. (s.f.). *¿Qué es el análisis predictivo?* Recuperado el 27 de octubre de 2026, de https://cloud.google.com/learn/what-is-predictive-analytics?hl=es

lemrei2025-ai. (2026). *Taller-BigData---ETL: Taller práctico ETL con Python y Power BI* [Repositorio de GitHub]. GitHub. https://github.com/lemrei2025-ai/Taller-BigData---ETL

Universidad de Cundinamarca. (2024). *Diferencias entre el análisis descriptivo, predictivo y prescriptivo* [Guía Analítica Empresarial, material de clase]. Especialización en Analítica y Ciencia de Datos.

Universidad de Cundinamarca. (2026). *Taller – Práctica de analítica predictiva empresarial* [Guía de actividad y dataset S12_dataset_ventas_zapatos.xlsx]. Especialización en Analítica y Ciencia de Datos.
