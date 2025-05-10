# CO2 Emissions Prediction

Welcome to the **CO2 Emissions Prediction** project, a Python-based machine learning application that predicts CO2 emissions of vehicles based on their engine size, cylinders, and fuel consumption. Using linear regression, this project analyzes a dataset to model the relationship between vehicle attributes and CO2 emissions, providing insights into environmental impact. It's a great example for learning regression modeling and data analysis with Python.

## Table of Contents
- [Features](#features)
- [Installation](#installation)
- [Usage](#usage)
- [How It Works](#how-it-works)
- [Dataset](#dataset)
- [Contributing](#contributing)
- [License](#license)
- [Acknowledgements](#acknowledgements)

## Features
- **Data Visualization**: Scatter plot of engine size vs. CO2 emissions for exploratory analysis.
- **Linear Regression Model**: Predicts CO2 emissions using engine size, cylinders, city fuel consumption, and combined fuel consumption.
- **Model Evaluation**: Computes Sum of Mean Squared Error (SME) and R² score to assess model performance.
- **Prediction**: Allows prediction of CO2 emissions for new vehicle data.
- Built with popular Python libraries: NumPy, Pandas, Matplotlib, and Scikit-learn.
- Simple and reproducible code for learning and experimentation.

## Installation
To set up the **CO2 Emissions Prediction** project, follow these steps:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/co2-emissions-prediction.git
   cd co2-emissions-prediction
   ```

2. **Install Dependencies**:
   Ensure you have Python 3.6+ installed. Install the required libraries using pip:
   ```bash
   pip install numpy pandas matplotlib scikit-learn
   ```

3. **Download the Dataset**:
   The script automatically downloads the `FuelConsumption.csv` dataset from a provided URL. Ensure you have an active internet connection when running the script for the first time. Alternatively, manually download the dataset from [here](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-ML0101EN-SkillsNetwork/labs/Module%202/data/FuelConsumptionCo2.csv) and place it in the project directory.

4. **Run the Script**:
   Execute the Python script:
   ```bash
   python co2_emissions_prediction.py
   ```

## Usage
Running the script performs the following steps:
1. Downloads and loads the `FuelConsumption.csv` dataset.
2. Displays the first 10 rows of the dataset and a subset of selected columns.
3. Plots a scatter graph of engine size vs. CO2 emissions.
4. Trains a linear regression model on 80% of the data and tests on the remaining 20%.
5. Outputs the model's coefficients, intercept, Sum of Mean Squared Error (SME), and R² score.
6. Predicts CO2 emissions for a sample vehicle with specified attributes (engine size: 2, cylinders: 4, city fuel consumption: 9.9, combined fuel consumption: 8.5).

Example output:
```
SME: 0.24
r2 score: 0.88
[[199.66260384]]  # Predicted CO2 emissions for the sample vehicle
```

To modify the script (e.g., use different features or test new data), edit the input arrays or feature selection in the code.

## How It Works
The project uses a linear regression model to predict CO2 emissions based on vehicle attributes. Here's a breakdown:

### Data Preprocessing
- **Dataset**: Loads `FuelConsumption.csv` using Pandas.
- **Feature Selection**: Uses `ENGINESIZE`, `CYLINDERS`, `FUELCONSUMPTION_CITY`, and `FUELCONSUMPTION_COMB` as input features, with `CO2EMISSIONS` as the target variable.
- **Train-Test Split**: Randomly splits data into 80% training and 20% testing sets using a mask.

### Visualization
- A scatter plot of `ENGINESIZE` vs. `CO2EMISSIONS` is generated using Matplotlib to visualize the relationship.

### Model Training
- **Algorithm**: Scikit-learn's `LinearRegression` is used to fit a model on the training data.
- **Features**: The model uses four features to predict CO2 emissions.
- **Output**: Prints the model's coefficients (`m`) and intercept (`C`).

### Evaluation
- **Sum of Mean Squared Error (SME)**: Measures the average squared difference between predicted and actual CO2 emissions.
- **R² Score**: Indicates the proportion of variance in CO2 emissions explained by the model (closer to 1 is better).
- Example results: SME ≈ 0.24, R² ≈ 0.88, indicating a good fit.

### Prediction
- The model predicts CO2 emissions for a sample vehicle with given attributes, demonstrating practical application.

## Dataset
The dataset (`FuelConsumption.csv`) contains vehicle data with the following relevant columns:
- `ENGINESIZE`: Engine size in liters.
- `CYLINDERS`: Number of cylinders.
- `FUELCONSUMPTION_CITY`: Fuel consumption in city driving (L/100km).
- `FUELCONSUMPTION_COMB`: Combined fuel consumption (L/100km).
- `CO2EMISSIONS`: CO2 emissions in grams per kilometer.

Source: [IBM Developer Skills Network](https://cf-courses-data.s3.us.cloud-object-storage.appdomain.cloud/IBMDeveloperSkillsNetwork-ML0101EN-SkillsNetwork/labs/Module%202/data/FuelConsumptionCo2.csv).

## Contributing
We welcome contributions to enhance the **CO2 Emissions Prediction** project! To contribute:
1. Fork the repository.
2. Create a new branch (`git checkout -b feature/your-feature`).
3. Make your changes and commit (`git commit -m "Add your feature"`).
4. Push to the branch (`git push origin feature/your-feature`).
5. Open a pull request.

**Ideas for Contributions**:
- Add support for other regression models (e.g., polynomial regression, random forest).
- Include additional features from the dataset (e.g., fuel type).
- Implement cross-validation for more robust model evaluation.
- Add interactive input for custom predictions.
- Enhance visualizations with additional plots (e.g., residual plots).

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Acknowledgements
- Thanks to the IBM Developer Skills Network for providing the dataset.
- Built with ❤️ using Python, NumPy, Pandas, Matplotlib, and Scikit-learn.
- Appreciation to the open-source community for tools and inspiration.

---

Explore the **CO2 Emissions Prediction** project and experiment with machine learning! If you have questions, suggestions, or issues, please open an issue on GitHub. Happy coding!