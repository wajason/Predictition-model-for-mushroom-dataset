Mushroom Classification Project 🍄
📖 Overview
This project, "Predictition model for mushroom dataset", is a collaborative effort by HW_Group1 to develop and compare machine learning and deep learning models for classifying mushrooms as poisonous or edible based on various features. The dataset used in this project is sourced from a primary mushroom dataset, which we preprocess and analyze extensively to build robust predictive models. The project includes data preprocessing, exploratory data analysis (EDA), model training, and hyperparameter optimization, culminating in a detailed report.
Our goal is to provide a comprehensive analysis of different classification models, including Logistic Regression, Random Forest, XGBoost, LightGBM, and Deep Neural Networks (DNN), to determine the best approach for mushroom classification. The project is documented in a Quarto Markdown (.qmd) file, which is also rendered as a PDF for easy reading.

🚀 Features

Data Preprocessing: Handling missing values, encoding categorical variables, and applying PCA for dimensionality reduction.
Exploratory Data Analysis (EDA): Visualizations like class distribution, GGpairs for numerical features, and frequency plots for categorical features.
Model Training: Comparison of multiple models, including:
Logistic Regression (basic and advanced)
Random Forest (basic and advanced)
XGBoost
LightGBM
Deep Neural Network (DNN) with various architectures


Hyperparameter Optimization: Using Optuna to fine-tune model parameters (code included but commented out).
Cross-Validation: Extensive use of k-fold cross-validation to ensure model robustness.
Detailed Reporting: A comprehensive report generated using Quarto, available in both .qmd and PDF formats.


📂 Repository Structure
Mushroom-Classification-Project/
│
├── Predictition_model_for_mushroom_dataset_on_github.qmd  # Main Quarto Markdown file
├── Predictition_model_for_mushroom_dataset_on_github.pdf  # Rendered PDF report
├── processed_data1.csv                                    # Preprocessed dataset
├── primary_data.csv                                       # Raw dataset
├── primary_data_cleaned.csv                               # Cleaned raw dataset
├── mushroom.png                                           # Image used in the report
├── README.md                                              # This file



🛠️ Installation
To run this project locally, follow these steps:
Prerequisites

R: Install R (version 4.0 or higher) from CRAN.
Python: Install Python (version 3.8 or higher) from Python.org or via Anaconda.
Quarto: Install Quarto from Quarto.org to render the .qmd file.
LaTeX: Install a LaTeX distribution (e.g., MiKTeX or TeX Live) to render the PDF with Chinese fonts.

Steps

Clone the Repository:
git clone https://github.com/your-username/Mushroom-Classification-Project.git
cd Mushroom-Classification-Project


Install R Dependencies:Open R and run the following to install required packages:
install.packages(c("reticulate", "Hmisc", "ggplot2", "tableone", "GGally", "caret", "randomForest", "xgboost", "MASS", "detectseparation", "table1", "brglm2"))


Install Python Dependencies:Create a virtual environment (optional) and install the required Python packages:
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
pip install -r requirements.txt


Set Up Python Path in R:Ensure reticulate in R points to the correct Python environment. Edit the .qmd file if needed:
library(reticulate)
use_python("path/to/your/python", required = TRUE)  # Update the path as needed


Install Fonts for PDF Rendering:The PDF uses the Microsoft JhengHei font for Chinese characters. Ensure this font is installed on your system, or modify the include-in-header section of the .qmd file to use a different font available on your system.



📖 Usage
Reading the Report

PDF Version (Predictition_model_for_mushroom_dataset_on_github.pdf):

Open the PDF in any PDF viewer to read the complete report, including visualizations, tables, and model results.
This is the easiest way to view the project without running any code.


Quarto Markdown Version (Predictition_model_for_mushroom_dataset_on_github.qmd):

Open the .qmd file in a text editor (e.g., VS Code with the Quarto extension) to view the raw source code and documentation.
To render the .qmd file into a PDF or HTML:
Ensure Quarto is installed.
Run the following command in your terminal:quarto render Predictition_model_for_mushroom_dataset_on_github.qmd --to pdf


The rendered output will be generated in the same directory.





Running the Code

Interactive Exploration:

Open the .qmd file in an editor that supports Quarto (e.g., RStudio or VS Code).
Run individual code chunks to explore the data preprocessing, visualizations, or model training interactively.


Reproducing Results:

Ensure all dependencies are installed as described in the Installation section.
Run the entire .qmd file using Quarto to reproduce the full analysis:quarto render Predictition_model_for_mushroom_dataset_on_github.qmd


Note: Some paths (e.g., C:/Users/user/Downloads/primary_data.csv) are hardcoded in the .qmd file. Update these paths to match the location of the datasets on your machine.


Model Training:

The .qmd file includes code for training various models (Logistic Regression, Random Forest, XGBoost, LightGBM, and DNN).
To experiment with different models or hyperparameters, modify the relevant code chunks in the .qmd file and re-run them.


Hyperparameter Optimization:

The Optuna section is commented out in the .qmd file. Uncomment and run it to perform hyperparameter tuning for the models:import optuna
# ... rest of the Optuna code ...


Note: Optuna tuning can be computationally expensive. Adjust n_trials as needed.




📊 Key Findings

Best Performing Model: The XGBoost model achieved the highest accuracy (77.14%) on the test set with 5-fold cross-validation.
Deep Learning: The DNN model, after improvements, achieved a test accuracy of around 50.41% (as per the latest results), indicating potential overfitting issues that need further tuning.
Feature Importance: Features like gill-attachment, habitat, and numerical features (cap-diameter, stem-height, stem-width) were critical for classification.
Challenges:
Small dataset size (173 samples) led to overfitting in some models, especially the DNN.
Class imbalance (96 poisonous vs. 77 edible) was addressed using class weights and SMOTE.



For detailed results, refer to the PDF or .qmd file.

🤝 Contributing
Contributions are welcome! If you'd like to contribute:

Fork the repository.
Create a new branch (git checkout -b feature/your-feature).
Make your changes and commit them (git commit -m "Add your feature").
Push to your branch (git push origin feature/your-feature).
Open a Pull Request.

Please ensure your code follows the existing style and includes appropriate comments.

📜 License
This project is licensed under the MIT License. See the LICENSE file for details.

📧 Contact
For questions or suggestions, please contact:

Jason (Project Lead): your-email@example.com
GitHub Issues: Feel free to open an issue in this repository.


🙏 Acknowledgments

The mushroom dataset used in this project is sourced from publicly available data.
Thanks to the Quarto team for their amazing documentation tool.
Libraries used: pandas, scikit-learn, tensorflow, xgboost, lightgbm, caret, randomForest, and more.


Happy classifying! 🍄
