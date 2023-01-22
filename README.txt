########### PROJECT REQUIREMENTS & INSTALLATION

1) In the [Dataset] folder you can find the dataset used for the project
	- reviews.csv [Original dataset]
	- df_normalized_complete [Normalization]
	- df_tokenized_complete [Normalization+Tokenization]
	- df_without_stopwords [Normalization+Tokenization+Stopwords removal]
	- df_lemmatized [FULL PREPROCESSING] <---- Dataset used for Classification and Clustering

2) In the [Dataset_] + [BOW, TFIDF, W2V, BOW_bin, TFIDF_bin, W2V_bin] folders you can find the final datasets used for binary/multi classification tasks, for each representation
	- X_train_ +  [BOW, TFIDF, W2V, BOW_bin, TFIDF_bin, W2V_bin].npy -> Final train datasets
	- X_test_ +  [BOW, TFIDF, W2V, BOW_bin, TFIDF_bin, W2V_bin].npy -> Final test set 

3) Preprocessing.ipynb is the notebook with every step for Data Exploration and Preprocessing
	- You just need to change the dataset path and everything is ready to go
	- The normalization step has a pretty long computation time. It is preferable to load the already processed dataset

4) In the [Model_estimated] foled you can find, for each representation, the models estimated for the binary and multiclass classification tasks. The models are divided for tasks (Multiclass, Binary) and for Text representation (BOW,TFIDF, W2V)
	- Example: Random Forest for MULTIclass task and BOW representation: Model_estimated/Multiclass_classification/BOW/rf_gridsearch_BOW
5) In the [Results] folder you can find the results dataframe for both tasks, binary and multiclass classification and all representation.

6) Classification.ipynb is the notebook withthe step for Classification task. The notebook is divided into two main sections: 
	- Multiclass Classification
	- Binary Classification
   Within each of the sections you can find the following subsections: 
	- Loading the dataset
	- Estimation and loading of each implemented algorithm
	- Analysis of results
   If you want to execute the code, you can set the correct path where required, in particular:: 
	- Load 'df_lemmatized.csv' 
	- Run 'Classification' section
	- Example: 'Multi-label classification'and 'Bag-of-Wods' representation: 
		- Set path and load 'Dataset_BOW/X_train_BOW.npy' and 'Dataset_BOW/X_test_BOW.npy'
		- For each models: set 'path' and load 'Model_estimated/Multiclass_classification/BOW/'model'_gridsearch_BOW'
	- This procedure is valid for both tasks, all representations and all models (attention, there may be some typos)

7) Clustering.ipynb is the notebook with the step for Clustering task
	- You just need to change the dataset path and everything is ready to go
	- You have to load the df_lemmatized.csv dataset