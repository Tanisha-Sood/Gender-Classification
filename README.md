# Gender-Classification

Objective  
The primary goal of this project is to predict the gender (Male or Female) associated with a given name using Natural Language Processing (NLP) and Machine Learning (ML) techniques.


Dataset :[ kaggle](https://www.kaggle.com/datasets/ananysharma/indian-names-dataset)
The dataset consists of Indian names labeled with their corresponding genders. The data was preprocessed and explored to ensure quality and balance. Key attributes include:  
- Name: The name of the individual.  
- Gender: The target attribute, represented as `M` (Male) and `F` (Female).  

Exploratory Data Analysis (EDA)  
1. Data Overview:  
   - Checked for missing values and ensured data integrity.  
   - Analyzed the distribution of male and female names.  

2. Visualizations:  
   - Gender distribution using a count plot.  
   - Frequency analysis of starting and ending alphabets of names.  
   - Word cloud showcasing the most common names in the dataset.  


Feature Engineering  
- Label Encoding: Converted gender labels (`M`, `F`) into numerical values (`0` for Male, `1` for Female).  
- Vectorization: Used character-level `CountVectorizer` to convert names into numerical feature arrays suitable for ML models.  

---

Machine Learning Models  
1. Logistic Regression:  
   - A linear model used for binary classification tasks.  
   - Trained on the vectorized names to predict gender.  

2. Naive Bayes:  
   - A probabilistic model assuming feature independence.  
   - Suitable for text-based classification.  

3. XGBoost:  
   - An advanced gradient-boosting algorithm optimized for performance.  
   - Implemented using the `XGBClassifier`.  

4. LSTM (Long Short-Term Memory):  
   - A type of Recurrent Neural Network (RNN) designed for sequential data.  
   - Layers:  
     - Embedding Layer: Converts names into dense representations.  
     - LSTM Layer: Captures sequential patterns in the names.  
     - Dense and Dropout Layers: These are for feature extraction and regularization.  
   - Trained over 100 epochs using `binary_crossentropy` loss and `adam` optimizer.  

Model Evaluation 
- Metrics Used:  
   - Confusion Matrix  
   - Accuracy  
   - Precision, Recall, F1-Score (Classification Report)  

- Performance:  
   - Logistic Regression, Naive Bayes, and XGBoost achieved competitive results.  
   - LSTM demonstrated robust learning due to its ability to handle sequential data effectively.  

Results  
- All models showed promising accuracy in predicting gender based on names.  
- LSTM was particularly effective due to its deep learning architecture, which can capture complex patterns.

