**Cyber security: Common Vulnerabilities and Exposures (CVE)**
 
A PROJECT BY TEAM ALGORITHM
 
 
**CONTRIBUTORS**

<li> Nafs Ahmad
<li> Owusu Samuel
<li> Bolarinwa Aishat	
<li> Temitope Omotosho	
<li> Raji Gbenga	
<li> Imah Gift
<li> Isaac Ayotamuno	
<li> Oluwatimilehin Folarin	
<li> Tobechukwu Okamkpa
<li> David Ekpo
<li> Igbokwe Success
<li> Obaloluwa Gbadegesin
<li> Stanley Okparaji
<li> Ibrahim Bilal
<li> Omoniyi Akinpelumi
<li> Oluwatobi Elegbede
 
**PROBLEM STATEMENT:**
 
Every year comes with numerous cases of software vulnerabilities. Software companies need to provide remedies to high vulnerabilities first and promptly. Hence, cybersecurity solutions are traditionally static and signature-based. Investigating all the alerts to priority threats may take more time and resources due to the higher possibility of false positives with traditional intrusion detection. 
Furthermore, traditional solutions are binary with limited advantages compared to predictive models that could predict the degree of attacks or risky actions based on data analysis techniques. It is critical to assess the severity of the vulnerability rapidly, as the severity score are obtained from the severity metrics. 


**PROJECT WORKFLOW**
 

**Data Sourcing** 
 
The dataset for this project was sourced from Kaggle and contains cyber security threats and their significance from NIST.

**Data Preparation**

 The following steps were taken for the data preparation:
<li>	Data collection: The process of data preparation starts with gathering data of interest from relevant sources. Most datasets at this stage are liable to contain some element of unwanted noise.
<li>	Data discovery and profiling: The CVE dataset consists of four associated csv files. Some missing values were observed at this stage.
<li>	Data Cleaning: The rows having missing values and duplicate values as observed in the dataset were dropped from the dataset. The features(columns) were also correctly renamed. 
<li>	Data Structuring: The csv files been cleaned and free of irregularities were merged using the “cve_id” as the primary key. It was stored as a comma-separated values file. The shape of the merged dataset is (241979,15). This means it has 241,979 rows and 15 columns. Some of the features of the dataset include cve_id, cve_name, summary, etc.
<li>	Data Transformation: The data transformation involves adding a feature that helps in understanding the behaviour of the dataset better. Transformations such as:
<li> Data Visualization: This final step was done to aid our understanding of the prepared dataset through plots like pie charts, bar plots, word clouds, and count plots.

**MODEL TRAINING, MODEL EVALUATION AND MODEL ARCHITECTURE**

**A.	Model Training:**
 
Traditional Machine Learning models, LSTM(Long short-term memory), Bidirectional LSTM were trained to perform a multi-class multi-output  model.
<li>	Tokenization, stopwords and lemmentization were performed on the input text and the words were vectorized with one hot encoding by generating the index of the word.
<li>	The generated vectors were trained on the KNN, Random forest, Logistic regression, XGboost, LSTM and Bidirectional models. They were evaluated by their performance on each target variable.
<li>	In addition, a Bidirectional Encoder Representations from Transformers (BERT) model was trained. Embedding of each statement was generated using BERT pre-trained weights.
<li>	The BERT model was fine-tuned to train a multi-class multi-output model using a drop  out of 0.1and the model was evaluated.

**B.	Model Evaluation:**
 
The multiclass classification model evaluations were done using the F1_score metrics in the scikit-learn documentation. The F1_score ranges from 0 to 1. When F1_score is close to 1, the model is well-performing and vice versa. According to our multiclass classification models in this study, the best performing model was the BERT Transformer. Also the regression model evaluations were done using the regression metrics in the scikit-learn official documentation. Some of the metrics include: Mean Absolute Error(MAE), Root Mean Square Error(RMSE), R-square, etc. The R-square was our main evaluation metric for the various regression models used for training the data. The RandomForest Regressor was the best-performing model amongst other regression models in this study.   
 
**C.	Model Architecture**
 
Model Deployment: 
The model was saved using joblib library and a web app was created using streamlit to show the use case in production. 
