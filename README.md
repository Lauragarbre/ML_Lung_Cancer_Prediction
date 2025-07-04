# ML_Lung_Cancer_Prediction
Project Break Machine Learning Repository

## Problema a resolver
Ese proyecto de Machine Learning está enfocado a precedir el grado del daño (leve, medio, alto)  en el cáncer de pulmón en función de una serie de hábitos y síntomas que presentan una serie de pacientes.

## Dataset
El Dataset escogido para la realización de dicho proyecto se ha extarido de la página Kaggle:https://www.kaggle.com/datasets/thedevastator/cancer-patients-and-air-pollution-a-new-link
El Dataset consta de 26 columnas y 1000 filas.
A continuación se expone la información de dichas columnas:
* Edad: Edad del paciente. (Numérico)
* Género: Sexo del paciente. (Categórico)
* Contaminación atmosférica: Nivel de exposición del paciente a la contaminación atmosférica. (Categórico)
* Consumo de alcohol: Nivel de consumo de alcohol del paciente. (Categórico)
* Alergia al polvo: Nivel de alergia al polvo del paciente. (Categórico)
* Riesgos laborales: Nivel de riesgos laborales del paciente. (Categórico)
* Riesgo genético: Nivel de riesgo genético del paciente. (Categórico)
* Enfermedad pulmonar crónica: Nivel de enfermedad pulmonar crónica del paciente. (Categórico)
* Dieta equilibrada: Nivel de dieta equilibrada del paciente. (Categórico)
* Obesidad: Nivel de obesidad del paciente. (Categórico)
* Tabaquismo: Nivel de tabaquismo del paciente. (Categórico)
* Fumador pasivo: Nivel de tabaquismo pasivo del paciente. (Categórico)
* Dolor torácico: Nivel de dolor torácico del paciente. (Categórico)
* Tos con sangre: Nivel de tos con sangre del paciente. (Categórico)
* Fatiga: Nivel de fatiga del paciente. (Categórico)
* Pérdida de peso: Nivel de pérdida de peso del paciente. (Categórico)
* Dificultad para respirar: Nivel de dificultad para respirar del paciente. (Categórico)
* Sibilancias: Nivel de sibilancias del paciente. (Categórico)
* Dificultad para tragar: Nivel de dificultad para tragar del paciente. (Categórico)
* Uñas en palillo de tambor: Nivel de uñas en palillo de tambor del paciente. (Categórico)

## Desarrollo del proyecto
Los pasos seguidos en este proyecto son:
- Importar librerías a utilizar (Python, Pandas, Sklearn, Scipy, Matplotlib, Seaborn, Lightgbm, Catboost, Pickle,...)
- Cargar el Dataset.
- Exploración y primera limpieza.
- Train/ Test Split.
- MiniEDA.
- Selección de Features (selección visual, estadística, mutual information, RFE, SFS,...)
- Baseline de modelos y Validación cruzada ( Random Forest Classifier, Deccision Tree Classifier, LGBM Classifier, Catboost Classifier, Logistic Regressor,...)
- Optimización de Hiperparámetros.
- Evaluación contra test.
- Primeras Conclusiones.
- Extra.
- Conclusiones finales.
- Conclusiones Personales.

## Estructura de los directorios
El notebook principal del trabajo es el que pone `main.ipynb` (versión en español) o `main_english.ipynb` (versión en inglés).
El archivo Presentación Proyecto Machine Learning.pdf es el documento en el que expongo el desarrollo y resultado del proyecto de una manera menos técnica.
El resto de notebooks, ubicados en la carpeta con el mismo nombre,son las pruebas que he realizado hasta llegar a las conclusiones del proyecto.
El orden de lectura o visualización de los diferentes notebooks sería el siguiente:
- `Dataset_celulas_cancerigenas.ipynb`
- `Dataset_celulas_cancerigenas_accuracy_1.ipynb`
- `Dataset_celulas_cancerigenas_accuracy_menor_1.ipynb`
- `Dataset_celulas_cancerigenas_accuracy_menor_1_PCA.ipynb`
- `Dataset_celulas_cancerigenas_accuracy_menor_1_features.ipynb`
- `Dataset_celulas_cancerigenas_target_ordinal.ipynb` (prueba para ver si los resultados eran similares categorizando ordinalmente la target)
- `Dataset_celulas_cancerigenas_clustering.ipynb` (prueba de realización de clustering, sin resultados satisfactorios)
- `Dataset_celulas_cancerigenas_accuracy_main.ipynb` (previo al main)

En la carpeta img están las imágenes utilizadas en la presentación del proyecto.
Carpeta models están guardados los modelos escogidos como mejores (tanto en versión español como inglés).
La carpeta data_sample contiene el dataset en formato csv.
La carpeta utils en mi caso está vacía ya que no he utilizado ningún recuso extra.
Todas estas carpetas están a su vez dentro de la carpeta src.

## Solución y Conclusiones
Los resultaos de diferentes modelos dán unas métricas perfectas, con un avg. recall de 1. 
Tras la realización de investigaciones y pruebas posteriores, me doy cuenta de que es un dataset sintético o preparado.
De hecho en el extra compruebo que se pueden sacar unas métricas muy buenas usando únicamente dos features de las 24 iniciales.

![target_distribution](https://github.com/user-attachments/assets/970f121a-baab-433e-99a5-da13435edf18)
![Alcohol_vs_target](https://github.com/user-attachments/assets/6e419459-47ed-40d2-bf7a-01a9ae53dd02)
![output](https://github.com/user-attachments/assets/8985c51e-cd0f-4906-a7da-0e17e0d652e6)
![Matrices_de_confusion_train](https://github.com/user-attachments/assets/c662e536-f3e9-4dc3-aea6-56360d8347ce)
![matrices_de_confusion_test](https://github.com/user-attachments/assets/d65ea5a8-8668-4469-b6b0-ab3545d3dc4a)




# ML_Lung_Cancer_Prediction (English version)
Project Break Machine Learning Repository

## Problem to solve
This machine learning project is focused on predicting the degree of damage (low, medium, high) in lung cancer based on a series of habits and symptoms presented by a group of patients.

## Dataset
The dataset chosen for this project was extracted from the Kaggle website: https://www.kaggle.com/datasets/thedevastator/cancer-patients-and-air-pollution-a-new-link
The dataset consists of 26 columns and 1,000 rows.
The information for these columns is presented below:
* Age: The age of the patient. (Numeric)
* Gender: The gender of the patient. (Categorical)
* Air Pollution: The level of air pollution exposure of the patient. (Categorical)
* Alcohol use: The level of alcohol use of the patient. (Categorical)
* Dust Allergy: The level of dust allergy of the patient. (Categorical)
* OccuPational Hazards: The level of occupational hazards of the patient. (Categorical)
* Genetic Risk: The level of genetic risk of the patient. (Categorical)
* Chronic Lung Disease: The level of chronic lung disease of the patient. (Categorical)
* Balanced Diet: The level of balanced diet of the patient. (Categorical)
* Obesity: The level of obesity of the patient. (Categorical)
* Smoking: The level of smoking of the patient. (Categorical)
* Passive Smoker: The level of passive smoker of the patient. (Categorical)
* Chest Pain: The level of chest pain of the patient. (Categorical)
* Coughing of Blood: The level of coughing of blood of the patient. (Categorical)
* Fatigue: The level of fatigue of the patient. (Categorical)
* Weight Loss: The level of weight loss of the patient. (Categorical)
* Shortness of Breath: The level of shortness of breath of the patient. (Categorical)
* Wheezing: The level of wheezing of the patient. (Categorical)
* Swallowing Difficulty: The level of swallowing difficulty of the patient. (Categorical)
* Clubbing of Finger Nails: The level of clubbing of finger nails of the patient. (Categorical)

## Project development
The steps followed in this project are:
- Import libraries to be used (Python, Pandas, Sklearn, Scipy, Matplotlib, Seaborn, Lightgbm, Catboost, Pickle, etc.)
- Load the dataset.
- Exploration and initial cleaning.
- Train/Test Split.
- MiniEDA.
- Feature selection (visual selection, statistics, mutual information, RFE, SFS, etc.)
- Model baseline and cross-validation (Random Forest Classifier, Decision Tree Classifier, LGBM Classifier, Catboost Classifier, Logistic Regressor, etc.)
- Hyperparameter optimization.
- Test evaluation.
- Initial conclusions.
- Extras.
- Final conclusions.
- Personal conclusions.

## Directory structure
The main work notebook is the one labeled `main.ipynb` (Spanish version) or `main_english.ipynb` (English version).
The Presentacion Proyecto machine Learning.pdf file is the document in which I present the development and results of the project in a less technical manner.
The other notebooks, located in the folder of the same name, are the tests I performed until reaching the project's conclusions.
The reading or viewing order for the different notebooks would be as follows:
- `Dataset_celulas_cancerigenas.ipynb`
- `Dataset_celulas_cancerigenas_accuracy_1.ipynb`
- `Dataset_celulas_cancerigenas_accuracy_menor_1.ipynb`
- `Dataset_celulas_cancerigenas_accuracy_menor_1_PCA.ipynb`
- `Dataset_celulas_cancerigenas_accuracy_menor_1_features.ipynb`
- `Dataset_celulas_cancerigenas_target_ordinal.ipynb` (test to see if the results were similar by ordinally categorizing the target)
- `Dataset_celulas_cancerigenas_clustering.ipynb` (clustering test, without satisfactory results)
- `Dataset_celulas_cancerigenas_accuracy_main.ipynb` (prior to main)

The img folder contains the images used in the project presentation.
The models folder contains the best models (both in Spanish and English).
The data_sample folder contains the dataset in CSV format.
The utils folder is empty in my case because I didn't use any additional resources.
All these folders are in the src folder.

## Solution and Conclusions
The results of different models yield perfect metrics, with an average recall of 1.
After further investigation and testing, I realize it's a synthetic or prepared dataset.
In fact, in the extra, I find that very good metrics can be obtained using only two of the initial 24 features.

![target_distribution](https://github.com/user-attachments/assets/970f121a-baab-433e-99a5-da13435edf18)
![Alcohol_vs_target](https://github.com/user-attachments/assets/6e419459-47ed-40d2-bf7a-01a9ae53dd02)
![output](https://github.com/user-attachments/assets/8985c51e-cd0f-4906-a7da-0e17e0d652e6)
![Matrices_de_confusion_train](https://github.com/user-attachments/assets/c662e536-f3e9-4dc3-aea6-56360d8347ce)
![matrices_de_confusion_test](https://github.com/user-attachments/assets/d65ea5a8-8668-4469-b6b0-ab3545d3dc4a)


