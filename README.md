# Fake-True-News-Prediction-Classification-Model

This notebook represents building a model which helps to predict whether a news is fake or true. Here I have used nlp techniques like tokenizing, lemmatizing, stemming, and other methods to clean text data. Next I have used Term Frequency-Inverse Document frequency for converting words to vectors. and used it in the building the model.

There are two sets of datasets provided. One for fake dataset, while other for true news datasets. Both are having same features like below:<br>
    1.<b>title</b><br>
    2.<b>text</b><br>
    3.<b>subject</b><br>
    4.<b>News_Type</b><br>
    5.<b>date</b><br><br>

The main challenge which i have faced here is to handle large dataset generated after tf-idf vectorization, When using full datasets, It created a dataset of having size more than 40 GB. This have created issues in code like out of memory error while running the code. To prevent that, I have used parameters in TF-IDF method like <b>max_df</b>, which removes the most frequently word when occured in more than given number of documents (in terms of % or count). Also used <b> min_df</b> which helps to remove in-frequently words occured in less than given number of documents.

Here I have used two kinds of datasets to build the model. One text dataset, which included only text content for model building. While other dataset used in text+non-text features like as given below:<br>
1. <b>Article_Subject</b> : Feature for categorizing news<br>
2. <b>Special-Characters-Count</b>: Feature which have the count of special characters in each sentence*<br>
3. <b>Article_Content_Length</b>: Length of article content* [character-wise]<br>
4. <b>word_count</b>: Number of words present in the article content* <br>




After analyzing models build using text dataset and text+non-text data, i could see that models build on non text data performer little better than others [ by small value]











*article_content/sentence = article title + article text
