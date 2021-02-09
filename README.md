# Character-Level-NER-using-Bidirectional-LSTM
It's a well known problem in the field of Natural Language Processing(NLP) where we need to find the Named Entities given in a sentence

Problem Statement
===============================
There are various categories of named entities in a sentence which include **B-Pers**, **B-ORG**, **B-LOC** and many others.
Given a sentence we need to identify these Named Entities.
**Eg** : New Delhi is very much polluted.
		Here the named entity is New Delhi which falls under the category of **B-LOC**.
The dataset here is taken from the Twitter Annotated Dataset which includes both English and Hindi words along with various hashtags.

Approach
===============================
We mainly approach this problem at a Character Level and for this we use **Bidirectional LSTM** i.e. 2 LSTMs one forward and one backward t preserve th context of the words.
We mark all the characters in the Named Entity using BIO where the boundaries are marked with **B** and all the characters within it are marked with **I** and the rest are marked with **O**. For out of vocabulary characters, we can use Out of Vocabulary token provided by Keras Tokenizer or we can also use our particular version using character dictionary.

Tools Used
===============================
Python, Tensorflow, Keras