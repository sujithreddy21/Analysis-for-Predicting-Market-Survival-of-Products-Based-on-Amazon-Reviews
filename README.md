# Analysis-for-Predicting-Market-Survival-of-Products-Based-on-Amazon-Reviews


---

# Amazon Reviews Sentiment Analysis using NLP

This project focuses on analyzing customer reviews from Amazon to extract aspects of products and classify sentiments for each aspect. The analysis uses Natural Language Processing (NLP) techniques to process and clean the reviews, detect languages, extract aspects (features), and classify their sentiment as positive or negative.

## Project Structure

- **Data Preprocessing**: 
  - Raw customer reviews are cleaned by removing unwanted characters, HTML tags, and stopwords, followed by lemmatization.
  - Language detection is done using the `polyglot` library to ensure only English reviews are analyzed.
  - Aspect extraction is performed by identifying key nouns (aspects) in the reviews.

- **Sentiment Classification**:
  - The sentiment for each aspect is classified using a pre-trained `DeBERTa-v3` model fine-tuned for aspect-based sentiment analysis.
  - The classifier labels each aspect as positive or negative.

- **Data Visualization**:
  - Various visualizations are created to display the top aspects for products and their respective sentiment trends over time.
  
- **Aspect Sentiment Summary**:
  - The project summarizes the most liked and disliked aspects for products based on customer reviews.

## Key Steps

1. **Data Loading**: Load Amazon reviews data from a `.jsonl` file.
2. **Text Cleaning**: Implement text cleaning functions to:
   - Remove special characters, HTML tags, and contractions.
   - Remove stopwords and apply lemmatization for normalization.
3. **Aspect Extraction**: Extract product features (nouns) from cleaned text.
4. **Sentiment Classification**: Classify the sentiment for each aspect using the pre-trained DeBERTa-v3 model.
5. **Data Merging**: Merge review data with product metadata to include additional features such as average rating.
6. **Visualizations**:
   - Sentiment analysis over time.
   - Bar charts showing the most liked and disliked aspects for a product.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/yourusername/NLP-Amazon-Reviews.git
    ```

2. Install the required libraries:
    ```bash
    pip install nltk transformers polyglot pyicu pycld2 matplotlib pandas
    ```

3. Download required NLTK data:
    ```python
    import nltk
    nltk.download('stopwords')
    nltk.download('punkt')
    nltk.download('wordnet')
    ```

## How to Run

1. Open the `NLP_Project.ipynb` file in Google Colab or Jupyter Notebook.
2. Run the cells sequentially to:
    - Mount Google Drive and load data.
    - Clean the data and extract aspects.
    - Classify aspect sentiments and generate visualizations.

3. You can also use the provided scripts to process new reviews and classify their sentiments.

## Results

- **Aspect Sentiment Analysis**: Provides detailed sentiment classification for each product aspect.
- **Top Liked/Disliked Aspects**: A summary of the most frequently liked and disliked aspects of a product.
- **Trends Over Time**: Sentiment trends for specific products over different time periods.

## License

This project is licensed under the MIT License.

---
