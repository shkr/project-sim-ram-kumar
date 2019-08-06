# The Problem: Classify Wikipedia Disease Articles

We provide a sample of articles taken from Wikipedia. There are lots of different kinds of articles, and one flavor is those that describe a disease. The data are html dumps of wikipedia articles. We give you a labelled set of disease articles (positives), and non-diseases articles (negatives).

*   **Part 1:** Use this data set to create a classifier that can accurately predict whether an article describes a disease.
*   **Part 2:** Extract the name of the disease. Optionally, include as much information as you can about the disease. E.g. information to consider are symptoms, causes, prognosis, prevention, treatment, relevant drugs, human/non-human susceptibility.

**The data:** The directory contains wikipedia article html dumps. There are direct wgets of the articles, e.g. [malaria](https://en.wikipedia.org/wiki/Malaria), [autism](https://en.wikipedia.org/wiki/Autism), [Parkinson's disease](https://en.wikipedia.org/wiki/Parkinson%27s_disease). They are organized into two directories: <tt>positive/</tt> and <tt>negative/</tt>. The positive dataset is 3,693 articles about diseases, and the negative dataset is 10,000 articles.

Here is the data set: [wikipedia_diseases.zip](https://www.dropbox.com/s/9o4d5jbzrlmmih2/wikipedia_diseases.zip?dl=1)

**Edge cases:**

1.  Your classifier might misclassify drug articles as disease articles, e.g. [Penicillin](https://en.wikipedia.org/wiki/Penicillin), [Paracetamol](https://en.wikipedia.org/wiki/Paracetamol), [L-DOPA](https://en.wikipedia.org/wiki/L-DOPA), [Erythromycin](https://en.wikipedia.org/wiki/Erythromycin). Check if that is the case, and optionally try to fix that mis-classification.
2.  Exclude broad articles that talk about generic classes of diseases, e.g. [genetic disorders](https://en.wikipedia.org/wiki/Genetic_disorder), [infection](https://en.wikipedia.org/wiki/Infection), [bacteria](https://en.wikipedia.org/wiki/Bacteria), [virus](https://en.wikipedia.org/wiki/Virus), [mutation](https://en.wikipedia.org/wiki/Mutation). Fun: when you exclude these, what does your classifier do for [cancer](https://en.wikipedia.org/wiki/Cancer)?


## FAQs

**How long will this take?**  
That is yours to commit. Just get back within 7 days from the time this repository is shared with you.

**What language should I use?**  
Whatever you want. 

**Can I use X?**  
Unless the tool directly answers the question "are these disease articles?". You can use whatever you want. 

**How should I solve it?**
There are many solutions to non-convex problems. We are seeking a deep learning engineer, so deep learning models are preferrable. 

Through this we want to understand the core skills and methods you are developing as a problem solver.

**What should I deliver?**  
Your code, results, and brief instructions on how to build and run your solution. 

**What is this again?**
This is a simulation of a project that you might execute. Our goal is that by collaborating on this repo we will both learn from experience. 

**Is there an example solution?**

1. Naive Bayes Classifier - https://github.com/shkr/wikiclassifier/blob/master/wikiclassifier.pdf
