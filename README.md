This is the code to run in Google Colab

# spaCy pipelines for pretrained BERT
This code uses the spaCy library and its transformers module to apply natural language processing (NLP) techniques to a dataset of grant applications. The NLP model used is BERT, a pre-trained transformer model for language understanding.

The code first installs the necessary modules, including spacy and torch, and downloads the en_trf_bertbaseuncased_lg model. It then reads in a training dataset of grant application summaries and their corresponding disciplines, dropping any null values in the summary column. The summary and discipline data are converted to lists and the summary list is converted to a list of strings.

Next, the spacy model is loaded and applied to the summary list to create a list of documents. Word vectors are then developed from these documents, and a support vector classifier (SVC) is fit to the word vectors and discipline data.

The code then repeats these steps for a test dataset, using the trained SVC to predict the disciplines for the test summaries. A summary dataframe is created to compare the predicted and actual disciplines, and the results are printed. Finally, the summary dataframe is saved as an excel file.
