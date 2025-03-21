# End-to-End Chest Cancer Classification using MLflow & DVC

This project implements an end-to-end chest cancer classification pipeline using **MLflow** and **DVC**.

## **UI Demo**
The following is a screenshot of the web interface for the chest cancer classification system:

![Chest Cancer Classification UI](Cancer_UI.png)

Users can upload a **chest scan image**, and the model predicts whether the image is **normal** or indicates cancer.

## **Features**
- **Machine Learning Model**: Trained using CNN-based deep learning architecture.
- **Experiment Tracking**: Uses MLflow for logging and tracking experiments.
- **Data Versioning**: Managed with DVC.
- **Deployment**: Flask-based model deployment.


## Project Structure

```
End-to-End-Chest-Cancer-Classification-using-MLflow-DVC/
├── dvc/                                # DVC-related files for versioning datasets
├── github/workflows/                   # GitHub CI/CD workflows
├── config/                             # Configuration files
│   ├── __init__.py
│   └── configuration.py
├── model/                              # Model-related files (trained models, artifacts)
├── research/                           # Jupyter Notebooks for analysis and experimentation
│   ├── 01_data_ingestion.ipynb
│   ├── 02_prepare_base_model.ipynb
│   ├── 03_model_trainer.ipynb
│   ├── 04_model_evaluation_with_mlflow.ipynb
│   └── trials.ipynb
├── src/                                # Source code for CNN classifier
│   └── cnnClassifier/                  # Main package
│       ├── __init__.py
│       ├── components/                 # Pipeline components
│       │   ├── __init__.py
│       │   ├── data_ingestion.py
│       │   ├── model_trainer.py
│       │   ├── model_evaluation_mlflow.py
│       │   └── prepare_base_model.py
│       ├── config/                     # Configuration management
│       │   ├── __init__.py
│       │   └── configuration.py
│       ├── constants/                  # Constants for project settings
│       │   └── __init__.py
│       ├── entity/                     # Entity classes for structured configurations
│       │   ├── __init__.py
│       │   └── config_entity.py
│       ├── pipeline/                   # End-to-end pipeline stages
│       │   ├── __init__.py
│       │   ├── prediction.py
│       │   ├── stage_01_data_ingestion.py
│       │   ├── stage_02_prepare_base_model.py
│       │   ├── stage_03_model_trainer.py
│       │   └── stage_04_model_evaluation.py
│       └── utils/                      # Utility functions, logger, exceptions
│           ├── __init__.py
│           └── common.py
│
├── templates/                          # HTML templates for UI
│   └── index.html
│
├── .dvcignore                          # Ignore files for DVC
├── .gitignore                          # Ignore files for Git
├── Cancer_UI.png                       # Screenshot of UI
├── Dockerfile                          # Docker setup
├── LICENSE                             # License file
├── README.md                           # Project documentation
├── app.py                              # FastAPI/Flask-based application
├── dvc.lock                            # DVC dependencies lock file
├── dvc.yaml                            # DVC pipeline definition
├── inputImage.jpg                      # Example input image
├── main.py                             # Main script entry point
├── params.yaml                         # Hyperparameter settings
├── requirements.txt                    # Required dependencies
├── scores.json                         # Model evaluation scores
├── setup.py                            # Package setup script
└── template.py                         # Template script for structuring files
```
