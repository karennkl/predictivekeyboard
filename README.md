*Predictive Keyboard App : A Capstone Project (for Data Science Specialization)*

### About 
Inputs for this app's language model were 3 corpora of approximately 200 MB each from Twitter, news, and blogs. 
(The data comes from HC Corpora.) 80% samples were used, with 20% reserved for testing. 
Ngram models were created from these corpora using strings of 1-4 words

 A word prediction app guesses the next word you're going to type. This saves you time and effort. And it's fun.
The prototype is available on the Web for you try. 
The app is built in English, and it can easily be adapted to other languages.

### Details
You can try the app yourself at shinyapps.io. Just type a phrase into the box to get a prediction. Predictions will appear immediately.


### Files

#### Language Model Algorithm
xxx : code to generate ngrams
*  generate samples of raw training data.
*  perform text preprocessing and data cleanup
*  tokenize corpora and generate ngram model

#### Word prediction app
xxx : code to perform search using ngram model
*  Maximum Likelihood Estimate for each ngram
*  predict function to estimate the next word for an input. 
*  Performs stupid backoff from ngram-4, to ngram-3 or ngram-2 if a model yields no results.

