# 🕴️ Employee Salary Prediction

An interactive web application that predicts employee salaries using a machine learning model. This tool provides data-driven insights for both employees and employers in the tech industry.

***

## 🌟 Overview

This project analyzes a dataset of technology salaries to build a predictive model. The core of the project is a Streamlit application that allows users to input job-related details and receive an estimated salary in return. The application also provides visualizations to explore salary trends across different roles, experience levels, and locations.

## ✨ Key Features

-   **🤖 ML-Powered Predictions:** Utilizes a Gradient Boosting model to predict salaries with high accuracy.
-   **💵 Currency Converter:** Instantly convert the predicted USD salary to dozens of world currencies via a live API.
-   **📊 Interactive Data Analysis:** Dynamically generated plots to visualize salary distributions by job title and company location.
-   **📈 Trend Exploration:** Sidebar visualizations offer a quick look at salary trends based on experience, company size, and more.
-   **🎨 Modern UI:** A clean, user-friendly interface built with Streamlit, optimized for both desktop and mobile use.

***

## ⚙️ How It Works

The project follows a standard machine learning workflow:

1.  **Data Loading & Preprocessing:** The `salary.csv` dataset is loaded. Unnecessary columns are dropped, and categorical abbreviations (e.g., 'FT' for 'Full-Time') are mapped to more descriptive terms.
2.  **Feature Encoding:** All categorical features (like `job_title`, `experience_level`, etc.) are converted into numerical format using `LabelEncoder`.
3.  **Model Training:** The data is split into training and testing sets. Five different regression models are trained and evaluated:
    -   Linear Regression
    -   Random Forest Regressor
    -   **Gradient Boosting Regressor (Best Performance)**
    -   Decision Tree Regressor
    -   SVR
4.  **Model Persistence:** The best model (Gradient Boosting) is saved to a file (`best_pipeline.pkl`) using `joblib` for later use in the web app.
5.  **Web Application:** The `app.py` script loads the saved model and creates a Streamlit interface where users can input data and see the model's predictions and analyses in real-time.

***

## 📂 Project Structure


.
├── 📄 app.py                   # Main Streamlit application script
├── 📓 employee salary prediction.ipynb # Jupyter Notebook for analysis and model training
├── 💾 best_pipeline.pkl        # Saved machine learning model
├── 📝 salary.csv               # The raw dataset
├── 📋 cleaned_salary_data.csv  # Processed data used by the app
├── 📜 requirements.txt         # Python dependencies
└── 📄 README.md                # This file


***

## 🚀 Getting Started

Follow these instructions to set up and run the project on your local machine.

### Prerequisites

-   Python 3.9 or higher
-   `pip` package manager

### Installation

1.  **Clone the repository to your local machine:**
    ```bash
    git clone [https://github.com/your-username/employee-salary-prediction.git](https://github.com/your-username/employee-salary-prediction.git)
    cd employee-salary-prediction
    ```

2.  **Create and activate a virtual environment (recommended):**
    ```bash
    # For Windows
    python -m venv venv
    .\venv\Scripts\activate

    # For macOS/Linux
    python3 -m venv venv
    source venv/bin/activate
    ```

3.  **Install the required libraries:**
    ```bash
    pip install -r requirements.txt
    ```

### Running the Application

1.  **Launch the Streamlit app from your terminal:**
    ```bash
    streamlit run app.py
    ```
2.  Open your web browser and navigate to the local URL provided (usually `http://localhost:8501`).

***

## 🤝 Contributing

Contributions are welcome! If you have suggestions for improvements or want to add new features, please feel free to:

1.  Fork the repository.
2.  Create a new branch (`git checkout -b feature/AmazingFeature`).
3.  Commit your changes (`git commit -m 'Add some AmazingFeature'`).
4.  Push to the branch (`git push origin feature/AmazingFeature`).
5.  Open a Pull Request.

***

## 📄 License

This project is licensed under the MIT License. See the `LICENSE` file for more details.
