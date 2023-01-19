########### PROJECT REQUIREMENTS & INSTALLATION

1) In the [Dataset] folder you can find the dataset used for the project
	- reviews.csv [Original dataset]
	- df_normalized_complete [Normalization]
	- df_tokenized_complete [Normalization+Tokenization]
	- df_without_stopwords [Normalization+Tokenization+Stopwords removal]
	- df_lemmatized [FULL PREPROCESSING] <---- Dataset used for Classification and Clustering

2) Preprocessing.ipynb is the notebook with every step for Data Exploration and Preprocessing
	- You just need to change the dataset path and everything is ready to go
	- The normalization step has a prettu long computation time. It is preferable to load the already processed dataset

3) 

4) Clustering.ipynb is the notebook with the step for Clustering task
	- You just need to change the dataset path and everything is ready to go
	- You have to load the df_lemmatized.csv dataset