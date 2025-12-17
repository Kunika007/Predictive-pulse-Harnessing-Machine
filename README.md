# Predictive Pulse: Machine Learning for Blood Pressure Analysis

## Overview
A comprehensive machine learning project that predicts hypertension stages using patient medical data. This project implements multiple classification algorithms and provides a Flask web application for interactive predictions.

## Project Objectives
- Analyze patient blood pressure data and hypertension patterns
- Build and compare multiple ML models for hypertension stage classification
- Identify key risk factors and patterns in hypertension
- Develop a user-friendly web application for predictions
- Provide actionable insights for healthcare professionals

## Dataset
- **Total Records:** 1,827 patient records
- **Features:** 14 attributes including demographics, symptoms, and medical history
- **Target Variable:** Hypertension Stages (Normal, Stage-1, Stage-2, Hypertensive Crisis)

### Key Features
- Gender, Age Group, Family History
- Medication Status, Symptom Indicators
- Blood Pressure Measurements (Systolic & Diastolic)
- Severity Classification, Diet Control Status

## Project Structure
```
github_repo/
├── notebooks/
│   ├── 01_Data_Preparation.ipynb
│   ├── 02_EDA.ipynb
│   └── 03_Model_Building.ipynb
├── data/
│   ├── patient_data.csv
│   └── processed_data.csv
├── app/
│   ├── app.py
│   ├── templates/
│   │   ├── index.html
│   │   ├── prediction.html
│   │   └── visualization.html
│   ├── static/
│   │   ├── css/
│   │   │   └── style.css
│   │   └── js/
│   │       └── script.js
│   └── utils.py
├── models/
│   ├── best_model.pkl
│   ├── scaler.pkl
│   ├── encoders.pkl
│   └── model_info.json
├── docs/
│   ├── INSTALLATION.md
│   ├── USAGE.md
│   ├── API_DOCUMENTATION.md
│   └── PROJECT_REPORT.md
├── requirements.txt
├── .gitignore
└── README.md
```

## Installation

### Prerequisites
- Python 3.8 or higher
- pip (Python package manager)
- Virtual environment (recommended)

### Setup Steps

1. **Clone the repository**
   ```bash
   git clone https://github.com/yourusername/predictive-pulse.git
   cd predictive-pulse
   ```

2. **Create and activate virtual environment**
   ```bash
   # Windows
   python -m venv venv
   venv\Scripts\activate
   
   # macOS/Linux
   python3 -m venv venv
   source venv/bin/activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run data preparation**
   ```bash
   jupyter notebook notebooks/01_Data_Preparation.ipynb
   ```

5. **Start the Flask web application**
   ```bash
   python app/app.py
   ```
   
   The application will be available at `http://localhost:5000`

## Usage

### Web Application
1. Navigate to the application homepage
2. Enter patient information in the prediction form
3. Click "Predict" to get the hypertension stage classification
4. View detailed analysis and visualizations

### Jupyter Notebooks
1. **01_Data_Preparation.ipynb** - Data loading, cleaning, and preprocessing
2. **02_EDA.ipynb** - Exploratory data analysis and visualization
3. **03_Model_Building.ipynb** - Model training, comparison, and evaluation

## Models Implemented

### Classification Algorithms
1. **Logistic Regression** - Baseline linear classifier
2. **Decision Tree** - Tree-based classification
3. **Random Forest** - Ensemble method (Best Model)
4. **Support Vector Machine (SVM)** - Kernel-based classifier
5. **K-Nearest Neighbors (KNN)** - Instance-based learning
6. **Ridge Classifier** - Regularized linear classifier
7. **Gaussian Naive Bayes** - Probabilistic classifier

### Best Model Performance
- **Selected Model:** Random Forest
- **Accuracy:** ~96% on test set
- **Key Strengths:** High accuracy, feature importance ranking, robust predictions

## Results & Insights

### Key Findings
- Systolic and Diastolic pressure are the strongest predictors
- Family history significantly impacts hypertension risk
- Age group shows correlation with hypertension stages
- Medication compliance improves outcomes

### Performance Metrics
- Precision: High across all hypertension stages
- Recall: Balanced across classes
- F1-Score: ~0.96 average

## Technologies Used

### Data Analysis & ML
- **pandas** - Data manipulation
- **numpy** - Numerical computing
- **scikit-learn** - Machine learning algorithms
- **matplotlib** - Static visualizations
- **seaborn** - Statistical visualizations

### Web Application
- **Flask** - Web framework
- **Jinja2** - Template engine
- **Bootstrap** - UI framework
- **Plotly** - Interactive visualizations

### Development Tools
- **Jupyter** - Interactive notebooks
- **Git** - Version control

## Features

### Data Analysis
✓ Comprehensive EDA with visualizations
✓ Statistical analysis and correlations
✓ Feature importance analysis
✓ Distribution analysis across demographics

### Machine Learning
✓ Multiple algorithm comparison
✓ Hyperparameter tuning
✓ Model validation and testing
✓ Confusion matrix analysis
✓ Classification reports

### Web Application
✓ User-friendly interface
✓ Real-time predictions
✓ Interactive visualizations
✓ Patient history tracking
✓ Detailed prediction reports
✓ Admin dashboard

## API Endpoints

### Flask API
```
POST /predict
  - Input: Patient data (JSON)
  - Output: Hypertension stage prediction with confidence

GET /api/statistics
  - Output: Dataset statistics and insights

GET /api/models
  - Output: Available models and performance metrics
```

## File Descriptions

### Data Files
- `patient_data.csv` - Raw dataset with 1,827 patient records
- `processed_data.csv` - Cleaned and processed data ready for ML

### Model Files
- `best_model.pkl` - Trained Random Forest model
- `scaler.pkl` - StandardScaler for feature normalization
- `encoders.pkl` - LabelEncoders for categorical features
- `model_info.json` - Model metadata and performance metrics

### Application Files
- `app.py` - Flask application entry point
- `utils.py` - Helper functions for predictions and data processing
- `templates/` - HTML templates for web interface
- `static/` - CSS and JavaScript files

## Contributing
1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit changes (`git commit -m 'Add AmazingFeature'`)
4. Push to branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Authors
- **Kunika Ahirwar** - Project Lead

## Acknowledgments
- Medical insights and domain expertise
- Dataset from healthcare analytics initiative
- Open-source ML community
- Contributors and reviewers

## Contact
For questions or suggestions, please open an issue on GitHub or contact the project maintainers.

## Citation
If you use this project, please cite:
```
@software{predictive_pulse,
  title={Predictive Pulse: Machine Learning for Blood Pressure Analysis},
  author={Ahirwar, Kunika},
  year={2025}
}
```

## Roadmap
- [ ] Add more advanced models (XGBoost, LightGBM)
- [ ] Implement patient database
- [ ] Add data export functionality
- [ ] Create mobile app
- [ ] Integrate wearable device data
- [ ] Add real-time monitoring dashboard

## Troubleshooting

### Common Issues
1. **Module not found errors** - Run `pip install -r requirements.txt`
2. **Port already in use** - Change port in app.py or kill the process
3. **Prediction errors** - Ensure input data is properly formatted

For more help, see [INSTALLATION.md](docs/INSTALLATION.md)
