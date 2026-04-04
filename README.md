# Machine Learning-Based Traffic Signal Timing Optimization for Reducing Urban Traffic Delay 

## Overview
This project aims to predict traffic delay (travel time) based on traffic conditions and signal timing features using machine learning models.  
The goal is to identify the most effective model and support signal timing optimization.

---

## Dataset
The dataset consists of hourly time-series traffic observations, where each sample represents the traffic conditions of a road segment at a specific timestamp. The data starts from 2018 to 2024 and contains 61368 samples with 30 features.

The dataset includes traffic-related features such as:

- Traffic volume
- Traffic speed
- Traffic density
- Road length
- Number of lanes
- Signal phase duration
- Time-related variables (time of day, day of week)
- Weather conditions

### Data Pipeline
- Raw data → preprocessing → cleaned dataset
- Raw dataset is in:`data/all_features_traffic_dataset.csv`
- Preprocessing is implemented in:`notebooks/Data_Preprocessing.ipynb`
- Final dataset used for modeling: `data/cleansed_traffic_monitoring.csv`


---

## Models
Three models are implemented and compared:

1. **Linear Regression (Baseline)**
2. **Support Vector Machine (SVM)**
3. **Multi-Layer Perceptron (MLP)**

- Feature scaling is applied
- Hyperparameter tuning is performed for SVM and MLP

---

## Results
Model performance is evaluated using:

- Mean Squared Error (MSE) (Primary metric for comparison)
- Mean Absolute Error (MAE)
- R² Score

The MLP model achieves the best performance and is selected as the final model.

---

## Repository Structure
```
ml-project-ece1513/
│
├── data/ # Dataset files
│ ├── all_features_traffic_dataset.csv # raw dataset
│ └── cleansed_traffic_monitoring.csv # cleaned dataset
│
├── notebooks/ # Jupyter notebooks
│ ├── Data_Preprocessing.ipynb
│ ├── Baseline_Model.ipynb
│ ├── SVM.ipynb
│ └── MLP_Model_+_Optimization.ipynb
│
├── requirements.txt # Required Python packages
└── README.md
```

---

## Usage

Run the notebooks in the following order:

1. **Data preprocessing and exploratory analysis**  
   `notebooks/Data_Preprocessing.ipynb`

2. **Model training and comparison**  
   `notebooks/Baseline_Model.ipynb`  
   `notebooks/SVM.ipynb`  
   `notebooks/MLP_Model_+_Optimization.ipynb` (model training section)

3. **Signal duration optimization**  
   `notebooks/MLP_Model_+_Optimization.ipynb` (optimization section)

**Note:** Some notebooks may take longer to run due to model training and hyperparameter tuning.

---

## Notes
- All datasets are stored locally in the `data/` folder to ensure reproducibility.
- Results in the notebooks are precomputed for convenience. Re-running all cells may take significant time.

---

## Authors
- Yixuan (Kelsy) Li  
- Wenqing(Chelsey) Liang  
- Jingwei (Zerek) Yu

---

## Contributions
- **Data preprocessing & EDA:** [Yixuan Li, Wenqing Liang]  
- **Baseline model implementation:** [Yixuan Li]  
- **SVM model and tuning:** [Jingwei Yu]  
- **MLP model and optimization:** [Wenqing Liang]  
- **Report writing & visualization:** [Yixuan Li, Wenqing Liang, Jingwei Yu]
- **Presentation design & slide preparation:** [Yixuan Li]
- **Repository management & organization:** [Jingwei Yu]
