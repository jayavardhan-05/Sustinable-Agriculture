# 🌱 Smart Fertilizer Recommender

An intelligent web application that recommends optimal fertilizer amounts for crops based on field conditions, environmental factors, and crop type. Built with machine learning to maximize crop yield while promoting sustainable farming practices.

## 📋 Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Technology Stack](#technology-stack)
- [Installation](#installation)
- [Usage](#usage)
- [Model Information](#model-information)
- [Project Structure](#project-structure)
- [How It Works](#how-it-works)
- [Contributing](#contributing)
- [License](#license)

## 🎯 Overview

The Smart Fertilizer Recommender uses machine learning to analyze various agricultural parameters and recommend the optimal amount of fertilizer needed for maximum crop yield. By considering factors like area, pesticide usage, rainfall, temperature, crop type, and geographical location, the system provides data-driven recommendations to farmers.

## ✨ Features

- **Intelligent Recommendations**: ML-powered fertilizer optimization based on multiple parameters
- **User-Friendly Interface**: Clean, intuitive Streamlit web interface
- **Real-Time Predictions**: Instant fertilizer recommendations with predicted yield
- **Multi-Crop Support**: Supports various crop types (Maize, Rice, Wheat, etc.)
- **Regional Adaptation**: Takes into account state-specific conditions
- **Yield Prediction**: Estimates crop yield based on recommended fertilizer amount
- **Optimization Algorithm**: Tests multiple fertilizer amounts to find the optimal solution

## 🛠️ Technology Stack

- **Python 3.x**
- **Streamlit**: Web application framework
- **Pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **Scikit-learn**: Machine learning model
- **Pickle**: Model serialization

## 📦 Installation

### Prerequisites

- Python 3.7 or higher
- pip package manager

### Step 1: Clone the Repository

```bash
git clone <repository-url>
cd sustainable
```

### Step 2: Install Dependencies

```bash
pip install streamlit pandas numpy scikit-learn
```

Or use a requirements file:

```bash
pip install -r requirements.txt
```

### Step 3: Verify Model Files

Ensure the following files are present in the project directory:
- `your_model.pkl` - Trained machine learning model
- `model_columns.pkl` - Feature names from training data
- `crop_yield.csv` - Training dataset (optional, for reference)

## 🚀 Usage

### Running the Application

1. Navigate to the project directory:
```bash
cd c:\Users\jaya vardhan\OneDrive\Desktop\sustainable
```

2. Launch the Streamlit server:
```bash
streamlit run app.py
```

3. The application will automatically open in your default web browser at `http://localhost:8501`

### Using the Application

1. **Enter Field Information**:
   - Area (in Hectares)
   - Pesticide Used (in kg)
   - Rainfall (in mm)
   - Temperature (in Celsius)

2. **Select Crop and Location**:
   - Choose your crop type from the dropdown
   - Select your state/region

3. **Get Recommendation**:
   - Click the "Get Recommendation" button
   - View the optimal fertilizer amount
   - See the predicted crop yield

## 🤖 Model Information

### Training Data

The model is trained on agricultural data containing:
- Field area measurements
- Pesticide usage records
- Rainfall patterns
- Temperature data
- Crop types
- Regional information (states)
- Historical fertilizer usage
- Actual crop yields

### Model Features

The model uses the following features:
- **Numerical Features**: Area, Pesticide, Rainfall, Temperature, Fertilizer
- **Categorical Features**: Crop Type, State (one-hot encoded)

### Optimization Process

The application uses a brute-force optimization approach:
1. Tests fertilizer amounts from 0 to 200 kg in 1 kg increments
2. Predicts yield for each fertilizer amount
3. Selects the fertilizer amount that maximizes predicted yield

## 📁 Project Structure

```
sustainable/
│
├── app.py                  # Main Streamlit application
├── your_model.pkl          # Trained ML model (140 MB)
├── model_columns.pkl       # Feature column names
├── crop_yield.csv          # Training dataset (1.6 MB)
└── README.md              # Project documentation
```

## 🔍 How It Works

1. **User Input Collection**: The application collects field and environmental parameters through an interactive web interface

2. **Data Preprocessing**: 
   - Creates a DataFrame from user inputs
   - Performs one-hot encoding on categorical variables (Crop, State)
   - Reindexes to match the model's expected feature order

3. **Optimization Loop**:
   - Iterates through fertilizer amounts (0-200 kg)
   - Predicts yield for each amount
   - Tracks the best performing fertilizer amount

4. **Recommendation Display**:
   - Shows optimal fertilizer amount
   - Displays predicted yield at that amount

## 🌾 Supported Crops

Currently supported crops include:
- Maize
- Rice
- Wheat

*Note: The crop list can be expanded by retraining the model with additional crop data*

## 📍 Supported Regions

Currently supported states:
- Assam
- Gujarat
- Maharashtra

*Note: Additional regions can be added by retraining the model with regional data*

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Areas for Improvement

- Add more crop types and regional data
- Implement soil quality parameters
- Add historical yield tracking
- Create data visualization dashboards
- Implement user authentication and data persistence
- Add export functionality for recommendations
- Integrate weather API for real-time data

## 📝 License

This project is licensed under the MIT License - see the LICENSE file for details.

## 🙏 Acknowledgments

- Agricultural data sources
- Streamlit community
- Scikit-learn contributors
- Open-source community

## 📧 Contact

For questions, suggestions, or issues, please open an issue on the repository.

---

**Made w for sustainable farming**

