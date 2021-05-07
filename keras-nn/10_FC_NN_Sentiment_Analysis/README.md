### Sentiment Analysis.

Sentiment analysis aims to determine the attitude, or sentiment. For example, a speaker or writer with respect to a document, interaction, or event. It is a natural language processing problem in which text needs to be understood to predict the underlying intent.

The sentiment is mostly categorized into positive, negative and neutral categories. Through sentiment analysis we might want to predict, for example, a customer's opinion and attitude about a product based on a review they wrote. This technique is widely applied to things like reviews, surveys, documents and much more.

### IMDB
The IMDB sentiment classification dataset consists of 50,000 movie reviews from IMDB users that are labeled as either positive (1) or negative (0). The reviews are preprocessed and each one is encoded as a sequence of word indexes in the form of integers. The words within the reviews are indexed by their overall frequency within the dataset. For example, the integer “2” encodes the second most frequent word in the data. The 50,000 reviews are split into 25,000 for training and 25,000 for testing.

The dataset was created by researchers at Stanford University and published in a 2011 paper, where they achieved 88.89% accuracy. It was also used within the “Bag of Words Meets Bags of Popcorn” Kaggle competition in 2011.

### Data preparation.
> Now it's time to prepare our data. We will vectorize every review and fill it with zeros so it contains exactly 10,000 numbers. That means we fill every review that is shorter than 10,000 with zeros. We need to do this because the biggest review is nearly that long and every input for our neural network needs to have the `same size`. We will also transform the targets into floats.

The following function create vectors on words.

```python

def vectorize(sequences, dim=10000):
    res = np.zeros((len(sequences), dim))
    for i, seq in enumerate(sequences):
        res[i, seq] = 1
    return res  
```