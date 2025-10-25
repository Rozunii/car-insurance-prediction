# Predicción de Reclamaciones de Seguros de Auto 🚗

## 📊 Descripción del Proyecto

Modelo de Machine Learning para predecir si un cliente hará una reclamación en su seguro de auto durante el período de la póliza. Este proyecto fue desarrollado para la compañía "On the Road" con el objetivo de identificar la característica individual que mejor predice las reclamaciones.

## 🎯 Objetivo

Identificar la **mejor característica individual** que maximice la precisión del modelo para predecir reclamaciones de seguros, permitiendo a la compañía comenzar con un modelo simple en producción.

## 🔍 Resultado Clave

El análisis reveló que **`driving_experience`** (experiencia de conducción) es la mejor característica predictora individual, logrando una **precisión del 77.71%**.

## 📁 Dataset

El dataset contiene información de 10,000 clientes con las siguientes características:

| Variable | Descripción |
|----------|-------------|
| `age` | Edad del cliente (categorizada) |
| `gender` | Género del cliente |
| `driving_experience` | Años de experiencia conduciendo |
| `education` | Nivel educativo |
| `income` | Nivel de ingresos |
| `credit_score` | Puntuación crediticia (0-1) |
| `vehicle_ownership` | Estado de propiedad del vehículo |
| `vehicle_year` | Año de registro del vehículo |
| `married` | Estado civil |
| `children` | Número de hijos |
| `postal_code` | Código postal |
| `annual_mileage` | Kilometraje anual |
| `vehicle_type` | Tipo de vehículo (Sedán/Deportivo) |
| `speeding_violations` | Violaciones de velocidad |
| `duis` | Infracciones por conducir bajo influencia |
| `past_accidents` | Accidentes previos |
| **`outcome`** | Variable objetivo: ¿Hizo reclamación? |

## 🛠️ Tecnologías Utilizadas

- **Python 3.8+**
- **pandas** - Manipulación y análisis de datos
- **numpy** - Operaciones numéricas
- **statsmodels** - Modelos de regresión logística

## 📈 Metodología

1. **Exploración de Datos (EDA)**
   - Análisis de información del dataset
   - Identificación de valores nulos
   - Estadísticas descriptivas

2. **Preprocesamiento**
   - Imputación de valores nulos con la media para:
     - `credit_score`
     - `annual_mileage`

3. **Modelado**
   - Entrenamiento de modelos de regresión logística individuales
   - Evaluación de cada característica de forma independiente
   - Cálculo de accuracy mediante matriz de confusión

4. **Selección del Mejor Modelo**
   - Comparación de precisión entre todas las características
   - Identificación de la característica óptima

## 📊 Resultados

```
Best Feature: driving_experience
Accuracy: 77.71%
```

La experiencia de conducción resultó ser el predictor más fuerte de reclamaciones de seguros, superando a características como violaciones de velocidad, accidentes previos y tipo de vehículo.

## 🚀 Cómo Ejecutar el Proyecto

### Prerrequisitos

```bash
pip install -r requirements.txt
```

### Ejecución

1. Clona este repositorio:
```bash
git clone https://github.com/tu-usuario/car-insurance-prediction.git
cd car-insurance-prediction
```

2. Asegúrate de tener el archivo `car_insurance.csv` en el directorio principal

3. Abre el notebook:
```bash
jupyter notebook Modeling_Car_Insurance_Claim_Outcomes.ipynb
```

4. Ejecuta todas las celdas

## 📂 Estructura del Proyecto

```
car-insurance-prediction/
├── Modeling_Car_Insurance_Claim_Outcomes.ipynb
├── car_insurance.csv
├── README.md
├── requirements.txt
└── .gitignore
```

## 💡 Insights y Conclusiones

- **Experiencia de conducción** es el factor más importante para predecir reclamaciones
- Los conductores con menos experiencia tienen mayor probabilidad de hacer reclamaciones
- Este insight permite a la compañía ajustar sus primas de manera más precisa
- El modelo simple basado en una sola característica es suficiente para comenzar en producción

## 🔮 Próximos Pasos

- [ ] Desarrollar un modelo multivariate para mejorar la precisión
- [ ] Implementar validación cruzada
- [ ] Analizar la interacción entre múltiples características
- [ ] Crear un dashboard interactivo para visualizar predicciones
- [ ] Desplegar el modelo en producción

## 📝 Notas Técnicas

- **Manejo de valores nulos**: Se utilizó imputación con la media para variables numéricas
- **Método de evaluación**: Accuracy calculado mediante matriz de confusión
- **Modelo utilizado**: Regresión logística (statsmodels)

## 👤 Autor

**Sebastian Sanchez Espinosa**
- 🎓 Python Data Associate - DataCamp Certified
- 📧 [Tu email]
- 💼 [Tu LinkedIn]
- 🌐 [Tu portafolio]

## 📄 Licencia

Este proyecto es parte de mi portafolio de Data Science y está disponible para fines educativos.

---

⭐ Si este proyecto te resultó útil, considera darle una estrella!
