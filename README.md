## Overview
This project focuses on extracting insights from product review datasets through text preprocessing and topic modeling. The goal is to process and clean the review data, followed by applying Latent Dirichlet Allocation (LDA) to identify topics, and visualizing the results to provide actionable insights. The entire process includes data cleaning, text preprocessing, lemmatization, stopword removal, and building an LDA model to extract meaningful topics from the review summaries.

## Key Features
1. **Data Preprocessing**: Cleaning and transforming product review data, including handling missing or irrelevant values, removing non-numeric characters, and processing text columns (such as 'ProductPrice', 'Discount', 'NumberofReviews', etc.).
2. **Text Cleaning**: The 'Summary' text is cleaned by removing stopwords, punctuation, and performing lemmatization.
3. **Topic Modeling**: Uses the LDA (Latent Dirichlet Allocation) algorithm to extract topics from product reviews.
4. **Visualization**: Interactive visualization of the extracted topics using pyLDAvis.
5. **Dependency Parsing**: Visualizing the syntactic dependencies of randomly selected review sentences using SpaCy.

## Technology Stack
- **Python**: The core programming language for data preprocessing and analysis.
- **Pandas**: For data manipulation and cleaning.
- **NLTK**: Used for text preprocessing tasks like tokenization, lemmatization, and stopword removal.
- **Gensim**: For implementing the LDA topic modeling algorithm.
- **SpaCy**: For dependency parsing of sentences in the review data.
- **pyLDAvis**: For interactive visualization of LDA topics.

## Steps Involved

### 1. Data Extraction and Merging
- Download CSV files containing product reviews.
- Extract the 'Summary' column and combine all files into a single master dataset (`merged_data.csv`).

### 2. Data Preprocessing
- **Price Cleaning**: The 'ProductPrice' column is cleaned by removing non-numeric characters and converting it to float values.
- **Discount Cleaning**: The 'Discount' column is processed to extract only the percentage amount.
- **Review Count Cleaning**: The 'NumberofReviews' column is converted to numeric, handling non-numeric values.
- **Rate Cleaning**: The 'Rate' column is processed to extract numerical values.

### 3. Text Cleaning
- **Preprocessing Text**: A function is defined to clean the review text by removing non-word characters, extra spaces, and numbers. It also converts text to lowercase and removes English stopwords.
- **Lemmatization**: The `lemmatize_POStag()` function lemmatizes the words based on their part-of-speech tags to reduce them to their base form.
- **Text Concatenation**: The `listtostring()` function converts lists of words into strings for easier use in NLP tasks.

### 4. Topic Modeling using LDA
- **Dictionary Creation**: A dictionary of terms is created using the tokenized reviews.
- **Document-Term Matrix**: The document-term matrix is built to represent the frequency of words in the reviews.
- **LDA Model**: The LDA model is trained using the `doc_term_matrix` and `dictionary` to extract 15 topics.
- **Coherence Score**: The coherence score of the LDA model is computed to assess the quality of the topics generated.

### 5. Visualization
- **Perplexity Calculation**: Perplexity, a measure of model performance, is calculated to evaluate the LDA model.
- **pyLDAvis**: An interactive visualization of the topics and their relationships is created using pyLDAvis.
- **Dependency Parsing**: Two sentences from the corpus are randomly selected and their syntactic dependencies are visualized using SpaCy.

## Observations and Results
- **Price and Discount Cleaning**: Non-numeric characters were removed from price and discount columns, making them easier to analyze.
- **Text Cleaning**: After preprocessing and lemmatization, the text data was ready for topic modeling.
- **Topic Extraction**: The LDA model generated meaningful topics, which were further evaluated using coherence scores.
- **Visualization**: pyLDAvis was used to visualize the topics interactively, and dependency parsing provided insights into the syntactic structure of sentences.

## 🌍 Explore More Projects  
For more exciting machine learning and AI projects, visit **[The iVision](https://theivision.wordpress.com/)** and stay updated with the latest innovations and research! 🚀  

---
