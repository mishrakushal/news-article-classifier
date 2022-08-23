# News Article Classification Model

A machine learning model that classifies news articles into various categories. Uses TF-IDF to vectorize input text and find important words. We remap the words in the articles into features. Features are the superset of words that have importance assigned to them based on the frequency of occurrence in the document and across various documents.

**TF-IDF**

- Transforms the text into a usable vector. Term frequency is the # of occurrences of a specific term in a document, it indicates how important a specific term is in a document.

- Document frequency is the # of documents containing a specific term. It indicates how common the term is.

For each article, we perform a chi-squared analysis to find the relevancy of words to a particular category. In doing so, we find the "key" words that, if occur, determine the category of the entire article.

`unigrams` array stores single word features (in increasing order of chi-squared statistical values)

`bigrams` array stores two-word features (in increasing order of chi-squared statistical values)

We only sample a subset of our data (in our case, 30%) because t-SNE is computationally expensive.

Cross-validation is performed across 5 different models:
1) Logistic Regression
2) Naive Bayes
3) Random Forest Regression
4) Decision Tree Classifier
5) K-Nearest Neighbours

We select the model which had the best mean cross-validation score, which, in this case, was Logistic Regression.


**Classifiers Tested**

- Logistic Regression (used for final model)
- Naive Bayes
- Random Forest Regression
- Decision Tree Classifier
- K-Nearest Neighbours

**Libraries Used**

- [numpy](https://numpy.org/doc/), [pandas](https://pandas.pydata.org/docs/), [matplotlib](https://matplotlib.org/), [scikit-learn](https://scikit-learn.org/)

---

**Resources**

- [TF-IDF Simplified](https://towardsdatascience.com/tf-idf-simplified-aba19d5f5530)

- [t-SNE clearly explained](https://towardsdatascience.com/t-sne-clearly-explained-d84c537f53a)

- [What is Chi-Squred Test?](https://www.simplilearn.com/tutorials/statistics-tutorial/chi-square-test)

- Dataset: [BBC News Classification | Kaggle](https://www.kaggle.com/competitions/learn-ai-bbc)


