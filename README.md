# Deduplication on Foursquare Location Matching
<div>
    <img src="https://cdn-icons-png.flaticon.com/512/3991/3991966.png"  width="200" align="left" hspace="10">
    
This repository contains the implementation of a machine learning project focused on deduplication of location data from Foursquare.<br><br>
The goal is to match different records that refer to the same physical location, improving the quality of location-based services.
</div>
<br><br><br><br>

## Table of Contents

- [Introduction](#introduction)
- [Dataset](#dataset)
- [Project Structure](#project-structure)
- [Installation](#installation)
- [Usage](#usage)
- [Models and Methods](#models-and-methods)
- [Contributing](#contributing)
- [License](#license)
<!-- - [Results](#results)
-->

## Introduction

Deduplication of location data is essential for maintaining accurate and reliable datasets, especially for applications like location-based services, recommendations, and navigation. This project aims to address the problem of identifying and merging duplicate location records in Foursquare's dataset.

## Dataset

The dataset used in this project consists of location records from Foursquare. Each record includes information such as the name, address, latitude, longitude, and other attributes of a location. The dataset has been preprocessed to remove obvious errors and standardize formats.

## Project Structure

```
.
├── data
│   ├── raw
│   ├── processed
├── notebooks
├── src
│   ├── data_preprocessing.py
│   ├── feature_engineering.py
│   ├── model.py
│   ├── evaluate.py
├── results
├── tests
├── README.md
└── requirements.txt
```

- `data`: Contains raw and processed datasets.
- `notebooks`: Jupyter notebooks for exploratory data analysis and model experimentation.
- `src`: Source code for data preprocessing, feature engineering, modeling, and evaluation.
- `results`: Directory for storing model outputs and evaluation results.
- `tests`: Unit tests for the project.
- `README.md`: Project documentation.
- `requirements.txt`: List of dependencies required to run the project.

## Installation

1. Clone this repository:
    ```sh
    git clone https://github.com/sinanazem/foursquare-deduplication.git
    cd foursquare-deduplication
    ```

2. Create and activate a virtual environment:
    ```sh
    python -m venv venv
    source venv/bin/activate
    ```

3. Install the required dependencies:
    ```sh
    pip install -r requirements.txt
    ```

## Usage

1. **Data Preprocessing**:
    ```sh
    python src/data_preprocessing.py
    ```

2. **Feature Engineering**:
    ```sh
    python src/feature_engineering.py
    ```

3. **Model Training**:
    ```sh
    python src/model.py
    ```

4. **Evaluation**:
    ```sh
    python src/evaluate.py
    ```

## Models and Methods

### Preprocessing

- **Data Cleaning**: Removal of duplicate records, handling missing values, and standardizing formats.
- **Geocoding**: Ensuring consistency in geographic coordinates.

### Feature Engineering

- **Text Features**: Tokenization, TF-IDF, and other text processing techniques for location names and addresses.
- **Geographical Features**: Distance calculations between coordinates.
- **Categorical Features**: Encoding of categorical variables.

### Model

- **Similarity-Based Methods**: Cosine similarity, Jaccard similarity, and others for text comparison.
- **Machine Learning Models**: Random Forest, Gradient Boosting, and other classifiers.
- **Deep Learning Models**: Siamese networks for learning similarity between pairs of records.

<!--
## Results

The project achieved an accuracy of X% in identifying and merging duplicate location records. Detailed results and evaluation metrics can be found in the `results` directory.
-->
## Contributing

Contributions are welcome! Please open an issue or submit a pull request for any feature requests, bug fixes, or improvements.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.
