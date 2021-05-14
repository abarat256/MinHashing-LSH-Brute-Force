# MinHasing, LSH, Brute Force

**Data**

The data for this assignment comes from the “Bag of Words” dataset at the UCI Machine Learning Repository. This dataset is actually four datasets; we’ll use the one called enron. The dataset contains nearly 40,000 internal emails from the company that were released for the public record. You can get the dataset from http://archive.ics.uci.edu/ml/machine-learning-databases/bag-of-words/. You’ll only need to look at the readme.txt ﬁle, which explains the layout, and the ﬁle docword.enron.txt which contains the actual data. Note that this ﬁle has been compressed via gzip, and so you’ll need to use the command gunzip to uncompress it. The ﬁle has already converted all words to integers. The words themselves are unnecessary for this exercise, but if you’re curious to see a list of them, they’re in vocab.enron.txt.


Task (1) - Comparing Jaccard Similarity with Minhashing
-------------------------------------------------------

The objective of this task is to compare the jaccard similarity of any two given documents from the dataset, calculated directly and by using minhashing. Write code that allows you to compute the Jaccard similarity between two particular documents of interest (as identiﬁed by their document id). You should then also write code to produce a signature matrix with a speciﬁed number of rows. Once you have produced the signature matrix, write code that
allows you to use it to estimate the Jaccard similarity between two particular documents (again identiﬁed by id).

**Questions**
1. How does the jaccard similarity estimated using minhashing vary when the number of rows is varied?
2. How much do the calculated jaccard similarity and the estimated similarity vary?


Task (2) - Finding nearest neighbors
------------------------------------

**Brute-Force Method**

Find the k nearest neighbors for a given document ID, using a simple brute-force approach of computing the exact Jaccard similarity between this document and the rest.

**LSH Method**
Implement an LSH approach for ﬁnding the k nearest neighbors for a given document ID by implementing the banding technique.

**Questions**
3. How does the performance of LSH compare to brute-force, with respect to average similarity and running time?
4. How does this vary with dataset size, k,r, and number of rows in signature matrix?

