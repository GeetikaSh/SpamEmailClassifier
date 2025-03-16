# Spam Email Classifier

## Objective
To conduct a **comparative analysis** on spam email classification models.

## Dataset
- (Provide details about the dataset: source, number of samples, number of spam vs. non-spam emails, etc.)

## Process Followed

### 1. **Data Preprocessing**  
Preparing data for modeling by **cleaning** and **normalizing** text. The key steps include:

- **Cleaning the text**: Removing special characters, lowercasing, and converting digits to words using `inflect`.
- **Stopwords handling**: Data is processed in two versions:
  - **With stopwords**: Some models like **BERT** perform better when stopwords are retained.
  - **Without stopwords**: Traditional models like **Naïve Bayes** work better without stopwords, as they can act as noise.
- **Tokenization**: Converting text into a list of words.
  - Example:  
    ```
    "Congratulations! You have won a prize."  
    → ["Congratulations", "!", "You", "have", "won", "a", "prize", "."]
    ```
- **Lemmatization**: Converting words to their root forms (e.g., "running" → "run").  
  - A parameter is introduced to determine whether stopwords should be removed or retained.

### 2. **Vectorization**  
Since machine learning models work with **numeric representations**, text data is converted into numerical form using **TF-IDF (Term Frequency-Inverse Document Frequency)**.

$$
TF-IDF = TF \times IDF
$$

Where:
- **TF (Term Frequency)**: Frequency of a word in a document.
- **IDF (Inverse Document Frequency)**: How unique a word is across all documents.

### 3. **Modeling**  
The models are trained on **both datasets** (with and without stopwords):

- **Naïve Bayes**  
- **Support Vector Machine (SVM)**  
- **(Other models, if any, should be listed here)**  

Each model is evaluated for **accuracy, precision, recall, and F1-score**.

## Observations
- (Summarize key findings from model performance)
- (Compare accuracy and effectiveness of models)

## Deployment
- The final model is **deployed** using **(Flask, FastAPI, or any cloud service)**
- A **web or API interface** is created for real-time spam detection.
