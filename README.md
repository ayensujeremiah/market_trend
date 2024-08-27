# Market Trend Oracle

This project aims to build a "Market Oracle" that analyzes marketplace datasets (such as GitHub Marketplace, AWS Marketplace, Google Workspace, etc.) to identify fast-growing trends in various industries. The Oracle generates insights by clustering similar applications, calculating growth rates, and utilizing GPT-3.5-turbo to summarize emerging trends. 

## Objective

The business objective is to identify top market trends, providing:
- **Title of the trend**
- **Description of the trend**
- **Growth pace** (based on application installs or usage metrics)
- **Examples of applications driving these trends**

This helps in creating investment theses for companies operating under fast-growing trends.

## Features

- **Data Preprocessing:** Merging and cleaning data from multiple marketplace datasets.
- **Clustering of Trends:** Using KMeans clustering to group similar applications based on their descriptions.
- **Growth Rate Calculation:** Calculating the growth pace of each trend by comparing the number of installs over time.
- **Trend Summarization:** Utilizing OpenAI’s GPT-3.5-turbo model to generate concise summaries of each trend.
- **JSON Report Generation:** Outputting the identified trends with their respective growth rates and examples in a structured JSON format.

## Datasets

The datasets used in this project contain the following fields:
- `App Title`: The name of the application.
- `App Description`: A brief description of what the app does.
- `Marketplace`: The marketplace where the app is listed (e.g., GitHub, AWS, Google Workspace).
- `Number of installs today`: Current install count.
- `Number of installs 6 months ago`: Install count six months prior to the current date.

## Setup and Installation

### Prerequisites

Make sure you have Python 3.x installed along with the following libraries:

- `pandas`
- `scikit-learn`
- `openai`
- `dotenv`

### Installation



1. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

2. Add your OpenAI to the `.env` file:
    ```env
    OPENAI_API_KEY=your_openai_api_key_here
    ```

