# AI For Social Good: Suicidal Ideation Detection in Online Social Content

## Overview

The rise of social media and online communities has provided safe and anonymous platforms for individuals to share their thoughts about mental health, express their feelings, and discuss their struggles. This project aims to prevent suicide by detecting suicide-related posts and identifying users' suicidal ideation through natural language processing (NLP) methods. The project focuses on data from Reddit and Twitter, classifying users' posts into categories of potential suicide risk and non-suicidal content using machine learning and deep learning techniques.

## Project Structure

- `Dataset`: Contains all the collected and cleaned datasets.
- `Data_Collection`: Includes scripts for scraping data from Reddit and Twitter.
- `Src`: Contains all the source code for text preprocessing and building machine learning models.
- `Pretrained_Models`: Houses all the pretrained models and tokenizers.
- `Flask`: Contains code for server setup and model deployment.

## Datasets

### Reddit Dataset
- **Suicidal Ideation Samples**: 2958
- **Non-suicidal Texts**: 5381
- Data scraped from subreddits like `suicidewatch`, `depression`, `anxiety`, etc.

### Twitter Dataset
- **Total Tweets with Suicidal Ideation**: 3000
- Data collected using keywords such as `end my life`, `die`, etc.

## Feature Processing and Model Training

1. **Text Cleaning**: Removed unnecessary characters, stopwords, and performed corpus-specific preprocessing.
2. **Vectorization**: Utilized both Bag of Words and TFIDF Vectorizer for text vectorization.
3. **Model Selection**:
    - **Random Forest Classifier**: Used Grid Search CV to optimize parameters, achieving an accuracy of 96% with TFIDF.
    - **Multilayer Bidirectional LSTM**: Trained with GloVe embeddings, attaining an accuracy of 97%.

## Results

| Model        | Accuracy | Precision | Recall | F1 Score |
| ------------ | -------- | --------- | ------ | -------- |
| RF + TFIDF   | 0.96     | 0.96      | 0.96   | 0.96     |
| LSTM + GloVe | 0.97     | 0.97      | 0.97   | 0.97     |

## Usage

### Setting Up the Project

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/your-repo-name.git
    cd your-repo-name
    ```

2. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

### Running the Server

1. Navigate to the Flask directory:
    ```bash
    cd Flask
    ```

2. Start the Flask server:
    ```bash
    python app.py
    ```

3. Access the application via your local server, typically at `http://127.0.0.1:5000/`.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## Contributing

Contributions are welcome! Please fork this repository and submit a pull request with your changes.

