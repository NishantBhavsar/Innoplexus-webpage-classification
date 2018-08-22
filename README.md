# Innoplexus-webpage-classification
Solution for this competition hosted on Analytics Vidhya.
[competition link](https://datahack.analyticsvidhya.com/contest/innoplexus-online-hiring-hackathon-ai-challenge/#problem_statement)
#### Simple Linear SVM model for webpage classification. Weighted F1 score of ~0.75.
#### ony TFIDF vectors of webpage content are used in the model.
#### Requierements:
- nltk
- beautifulsoup4
- pandas
- sklearn
- scipy

### Problem statement:
-  Classify given webpage to its category (Tag) like news, profile, publication etc.

### Data:
- In Train dataset wbepage domain name, url, webpage content in HTML form and, category (Tag) are available.
- In test dataset wbepage domain name, url and, webpage content in HTML form are available.
- 6.75 GB of webpages content data.
- Based on these data we have to tag every webpage.

### Solution approach:
- Beacuse webpage content data is in HTML format we have to first remove all HTML tags, css and javascript from this dataset.
- For that we can use beautifulsoup. This will give us content of webpage without HTML.
- Now, convert this data to TfIdf vectors using sklearn.
- I have only used these vectors for training simple Linear SVM model.
- Linear SVM model takes too less amount of time for training. So, hyperparameter optimization can be done fast.
