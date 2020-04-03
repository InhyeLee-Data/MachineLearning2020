## IMDB Movie Review NLP Supervised Learning Log

#### v1 (Resubmission. March 21 2020)
- fit_transform (training) vs transform (testing) added
- fitted_transformations array added
- Hashing Vectorizer (n_features increased to 2 ** 21)
- Text Cleaning : Movie specific words removed

#### v1 (March 6 2020)
- Text Cleaning : Lowercasing, general stop words/some formatting/punctuation removal for reducing the data.
- Hashing Vectorizer (n_features increased to 2 ** 18 to cope with text classification)/ TFIDF transformer 
- OLS removed from the model testing list (Not performing so well)
- Experimented with the alpha value a bit for regularization 
- Ridge Regression selected for this iteration for the better accuracy in the test set, over other models 
