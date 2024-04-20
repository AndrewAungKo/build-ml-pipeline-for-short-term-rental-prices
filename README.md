# Build an ML Pipeline for Short-Term Rental Prices in NYC

This project aims to build a machine learning pipeline to predict short-term rental prices in New York City. The pipeline is built using MLflow and the model is trained on a dataset of rental listings.

## Table of Contents

- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [Running with Python](#running-with-python)
  - [Running with MLflow](#running-with-mlflow)
- [Wandb Project](#wandb-project)
- [Contributing](#contributing)
- [License](#license)

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes.

### Prerequisites

Please ensure you have the following software installed on your system:

- Python 3.7+
- Conda

The specific Python packages required are listed in the `environment.yml` file.

### Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/AndrewAungKo/build-ml-pipeline-for-short-term-rental-prices.git
   ```

2. Navigate to the project directory:
   ```bash
   cd build-ml-pipeline-for-short-term-rental-prices
   ```

3. Create a new Conda environment:
   ```bash
   conda env create -f environment.yml
   ```

4. Activate the new environment:
   ```bash
   conda activate nyc_airbnb_dev
   ```

5. Follow the instructions in `installation.txt` to complete the setup.

## Usage

### Running with Python

To run the ML pipeline, execute the following command:

```bash
python main.py
```

### Running with MLflow

To run the ML pipeline with MLflow, first ensure that the MLflow server is running. You can start the server with the following command:

```bash
mlflow server
```

Then, you can run the pipeline with the following command:

```bash
mlflow run . -P steps=test_regression_model
```

Replace `test_regression_model` with the name of the step you want to run.

(OR)

You can run the release using ``mlflow`` without any other pre-requisite. We will
train the model on a new sample of data that is (``sample2.csv``):

```bash
mlflow run https://github.com/AndrewAungKo/build-ml-pipeline-for-short-term-rental-prices.git \
         -v 1.0.1 \
         -P hydra_options="etl.sample='sample2.csv'"
```

## Wandb Project

You can view the project on Wandb [here](https://wandb.ai/andrewaung/nyc_airbnb).

## Contributing

- see CODEOWNERS

## License

- see the [LICENSE.txt](LICENSE.txt) file for details

## Code Owners

The code owners for this repository are @udacity/active-public-content. They will be automatically requested for review when you open a pull request.
```
