# Miniproject 3 - 3 Tasks

## Task 1: Compute N-gram Counts(Extend functionality)

GOAL: Implement a version of the N-gramCount that counts all n-grams over the test data up to length N.

## Task 2: Compute Hashtag Similarity(Extend functionality)

GOAL: Extend functionality of HashtagSim to compute similariteis between any pair of hashtags that share at least 1 common word.

## Task 3: Compute Hashtag Similarity(Code optimization)

GOAL: Your extended HashtagSim program(Task 2) must finish within 90 minutes on a cluster of 5 medium instances(c1.medium) on Amazon EMR

## N-gram

In the fields of computational linguistics and probability, an n-gram is a contiguous sequence of n items from a given sequence of text or speech. The items can be phonemes, syllables, letters, words or base pairs according to the application. The n-grams typically are collected from a text or speech corpus.

An n-gram of size 1 is referred to as a "unigram"; size 2 is a "bigram" (or, less commonly, a "digram"); size 3 is a "trigram". Larger sizes are sometimes referred to by the value of n, e.g., "four-gram", "five-gram", and so on. 

![ngram1](./_resources/ngram1.jpg)

In this NgramCount application, given an input corpus, we’re interested in the count of all the n-grams.

## HashtagSim

This program analyzes the similarities between hashtags, which are used primarily in Twitter.com to label the tweets. A hashtag is denoted by a ‘#’ followed by a word. For example, a recent tweet from Barack Obama reads: “The excuses not to #ActOnClimate need to end”. In this tweet, “#ActOnClimate” is a hashtag.

Hashtags are used to categorize tweets, promote events, etc. In our program, we try to identify how similar the hashtags are. We’re using the words that co-occurred with a hashtag as its features. For example, given a tweet “#a b c”, word “b” and “c” will have both co-occurred with hashtag “#a” in the tweet for once. Given the following corpus:

    #a b c
    #a b #b 
    #b #c d e 
    #c e f

The co-occurrence counts for each hashtag, or put in another way, the features for the hashtags, will look like the following:

    #a b:2;c:1;
    #b b:1;d:1;e:1; 
    #c d:1;e:2;f:1;

Note that here we are treating hashtag “#b” and word “b” differently. Also, we’re using both the co-occurred words and the co-occurrence counts to represent a hashtag.

After calculating the feature vector for the hashtags, we can compute the similarity between hashtag pairs, using inner product of the feature vectors. The inner product of two feature vectors is calculated by picking all the common words and summing up the products of the co-occurrence value.

Taken the above result as example, the inner product between “#a” and “#b” will be 2, since they have only 1 shared word, “b”, and the product is 2*1. The inner product between “#b” and “#c” will be 3, which is result of 1*1 + 1*2. The bigger the inner product is, the more similar the two hashtags are in the given corpus.