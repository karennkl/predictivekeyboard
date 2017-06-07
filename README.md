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

The application uses a sample of approximately 60,000 Tweets, news articles, and blog entries. The original algorithm pruned the sample once it was divided into 4, 3, 2, and one-grams but it was not necessary for speed and space purposes and drove down the accuracy. Thus the pruning was removed.


The model utilizes the maximum likelihood estimation (MLE) to estimate N-gram probabilities. To estimate probabilities MLE uses the relative frequency ratio:

\Large{ P \left( w_n|w_{n-1} \right) = \frac{C(w_{n-1}w_n)}{C(w_{n-1})} }

To simplify predictions where the N-gram which was input by the user is not found in the data sample, the model also utilizes the Stupid Backoff algorithm. Stupid Backoff works under the assumption that "if a higher order N-gram has a zero count, we simply backoff to a lower order N-gram, weighted by a fixed weight (lambda)." The fixed weight the model uses for lambda is .4 which has been known to work well for this algorithm.

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

### Links

The exploratory analysis of the dataset performed earlier in the project can be found at: 
https://rpubs.com/nkl/ExploratoryAnalysisCapstone
