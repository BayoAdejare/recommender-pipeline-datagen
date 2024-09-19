# X Data Generative AI Recommender Pipeline

This project implements an end-to-end data pipeline for a generative AI-based recommender system using X (formerly Twitter) data. The pipeline includes data collection, preprocessing, model training, and a Streamlit web application for interactive recommendations.

## Table of Contents
- [Project Overview](#project-overview)
- [Installation](#installation)
- [Usage](#usage)
- [Data Pipeline](#data-pipeline)
- [Streamlit Application](#streamlit-application)
- [GitHub Actions](#github-actions)
- [License](#license)

## Project Overview

This project aims to create a personalized content recommender system using X data and generative AI techniques. The pipeline collects user data from X, preprocesses it, trains a generative AI model, and provides recommendations through a user-friendly Streamlit interface.

Key features:
- Data collection from X API
- Data preprocessing and feature engineering
- Generative AI model training
- Streamlit web application for interactive recommendations
- Automated CI/CD pipeline using GitHub Actions
- Deployment support for AWS and Azure

## Installation

1. Clone the repository:
   ```
   git clone https://github.com/yourusername/x-data-gen-ai-recommender.git
   cd x-data-gen-ai-recommender
   ```

2. Create a virtual environment and activate it:
   ```
   python -m venv venv
   source venv/bin/activate  # On Windows, use `venv\Scripts\activate`
   ```

3. Install the required packages:
   ```
   pip install -r requirements.txt
   ```

4. Set up your X API credentials:
   - Create a `.env` file in the project root
   - Add your X API credentials:
     ```
     X_API_KEY=your_api_key
     X_API_SECRET=your_api_secret
     X_ACCESS_TOKEN=your_access_token
     X_ACCESS_TOKEN_SECRET=your_access_token_secret
     ```

## Usage

1. Run the data collection script:
   ```
   python scripts/collect_data.py
   ```

2. Preprocess the collected data:
   ```
   python scripts/preprocess_data.py
   ```

3. Train the generative AI model:
   ```
   python scripts/train_model.py
   ```

4. Launch the Streamlit application:
   ```
   streamlit run app.py
   ```

## Data Pipeline

The data pipeline consists of the following steps:

1. Data Collection: Fetch user data, tweets, and interactions from the X API.
2. Preprocessing: Clean and transform the raw data, perform feature engineering.
3. Model Training: Train a generative AI model on the preprocessed data.
4. Model Evaluation: Assess the model's performance using relevant metrics.
5. Model Deployment: Save the trained model for use in the Streamlit application.

## Streamlit Application

The Streamlit application provides an interactive interface for users to:

- Input their X username or interests
- Receive personalized content recommendations
- Explore the reasoning behind recommendations
- Provide feedback on recommendation quality

To run the Streamlit app locally:

```
streamlit run app.py
```

## GitHub Actions

This project uses GitHub Actions for continuous integration and deployment. The workflow includes:

- Automated testing on push and pull requests
- Linting and code quality checks
- Building and pushing Docker images
- Deploying to AWS or Azure

The project supports deployment to the following cloud platforms:
- Amazon Web Services (AWS)
- Microsoft Azure

Check the `.github/workflows` directory for the specific workflow configurations.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
