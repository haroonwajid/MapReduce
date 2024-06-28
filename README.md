MapReduce in Big Data and Analytics:
Text Processing and Analysis Report
In this report, I will detail the steps involved in processing and analyzing text data from a Wikipedia dataset using Python. The process involves several steps including data cleaning, text preprocessing, and analysis using the Vector Space Model (VSM).
Data Loading and Preprocessing
We started by loading a Wikipedia dataset from a CSV file named enwiki-20170820.csv using the pandas library. The dataset contains two columns: ARTICLE_ID and SECTION_TEXT. We selected a subset of the dataset consisting of the first 5000 rows for further processing.
Next, we cleaned the text data by removing special characters, numbers, and converting the text to lowercase. This was done to ensure uniformity in the text data for subsequent analysis.
Text Preprocessing
After cleaning the text, we used the spaCy library to perform text preprocessing. This involved tokenization, lemmatization, and removing punctuation and whitespace. The preprocessing step aimed to convert the raw text into a format suitable for analysis.
Vector Space Model (VSM)
The Vector Space Model is a mathematical representation used for information retrieval and text mining tasks. It represents text documents as vectors in a high-dimensional space, where each dimension corresponds to a term in the vocabulary.
Mapper and Reducer Functions
We implemented mapper and reducer functions in Python to calculate the vocabulary, Term Frequency (TF), and Inverse Document Frequency (IDF) from the preprocessed text data.
The mapper_vocabulary function extracts the unique vocabulary words from the text data.
The mapper_tf function calculates the Term Frequency (TF) for each word in the vocabulary.
The mapper_idf function computes the Inverse Document Frequency (IDF) for each word.
These mapper functions emit key-value pairs, which are then aggregated by the reducer functions.
Findings
Vocabulary: The vocabulary output contains a list of unique words present in the text data.
Term Frequency (TF): The TF output provides the frequency of each word in each document normalized by the total number of words in the document.
Inverse Document Frequency (IDF): The IDF output shows the logarithmically scaled inverse document frequency of each word in the dataset.
Contributors:
This project exists thanks to the extraordinary people who contributed to it.
Huzaifa Rehman (i212694@nu.edu.pk)
Azeem Ahmad Khan (i21720@nu.edu.pk) 
Haroon Wajid (i211763@nu.edu.pk) 

Conclusion
In this report, we successfully processed and analyzed text data from a Wikipedia dataset using Python. We employed techniques such as data cleaning, text preprocessing, and the Vector Space Model to extract meaningful insights from the text data. The mapper and reducer functions facilitated the computation of vocabulary, Term Frequency (TF), and Inverse Document Frequency (IDF) efficiently.
The outputs generated from the analysis provide valuable information about the characteristics of the text data, which can be further utilized for tasks such as document classification, information retrieval, and text summarization.

