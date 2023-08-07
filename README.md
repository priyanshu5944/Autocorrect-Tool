# Autocorrect tool for words
One of the features that use Natural Language Processing (NLP) is the Autocorrect function. This feature works on every smartphone keyboard regardless of the brand.

It is specially programmed to generalize all the correct words in the dictionary and looks for the words that are the most comparable to those words not in the vocabulary.

To understand how it works, we will learn a little about Natural Language Processing in this article and then we will use Python to build the autocorrect feature.

### Table of contents 
Prerequisites
Natural Language Processing (NLP)
Autocorrect feature
Building autocorrect feature
Installing libraries
Reading text file (dictionary)
Frequency and probability of dictionary words
Implement 4 edit word functions
Conclusion

### Prerequisites
To follow along with this tutorial, the reader should:

Have a prior understanding of the basics of Natural Language Processing and Machine Learning concepts.
Have a basic understanding of Python and the various python libraries used for Natural language processing.
Know how to use Pycharm or any other IDE for working with Python.
To download and install the Pycharm IDE on your PC, go to this website.

### Natural Language Processing (NLP)
Natural Language Processing (NLP) is a branch of Artificial Intelligence that allows computers to understand and process natural human language.

NLP uses a programming language that enables computers to evaluate and interpret large volumes of natural language data.

It paves the door for more interactivity and productivity in a variety of fields, like:

Search autocorrect and autocomplete.
Language translation and grammar checkers.
Chatbots and social media monitoring.
Email filtering and voice assistants.
We’ll look at how it’s employed in auto-correction systems in this tutorial.

### Autocorrect feature
The Autocorrect model is programmed to correct spellings and errors while inputting text and locating the most comparable related words.

It is completely based on NLP that compares the words in the vocabulary dictionary and the typed words on the keyboard.

If the typed word is found in the dictionary, the autocorrect feature assumes you typed the correct term. If the word does not exist, the tool identifies the most comparable words in our smartphone’s history, as it indicates.

When building this model/feature, the following steps are involved:

###### Identifying misspelled word
A word is misspelled if the text is not found on the vocabulary of the corpus (dictionary), then the autocorrect system flags out for correction.

Find strings that are N-edit-distance away from the misspelled word
Editing is an operation performed on the string to change it to another string.

The n represents the edit distance like 1, 2, 3, so on, which keeps track of the number of edit operations to be done.

Hence, the edit distance is the count of the number of operations performed on a word to edit it.

The following are examples of edits:

INSERT - a letter should be added.
DELETE - removes a letter.
SWAP - swaps two adjacent letters.
REPLACE - changes one letter to another.
NOTE: For autocorrect systems, n is usually between 1 and 3 edits.

###### Filtering suggested candidates
Only correctly spelled words from the created candidate list are considered, so that we can compare them to the words in the corpus to filter out the ones that don’t exist.

####### Order filtered candidates based on word probabilities
The probabilities of the words are calculated based on the following formula:

P(w) = C(w)/V

P(w)- the probability of a word w.
C(w) - number of times (frequency) word appears in the vocabulary dictionary.
V - the total sum of words in the dictionary.
###### Choose the most-likely candidate
When the probabilities are calculated, the actual list of words is grouped by the most likely word from the created candidates.

### Building autocorrect feature
We will need a dictionary to develop an autocorrect system where the smartphone uses history to match the typed words to see if they are correct or not.

For this tutorial, we will use a sample.txt file found in the project folder containing the 1000 most used vocabularies.

###### Installing libraries
We start by installing all the libraries general to machine learning using the pip command from the terminal.

pip install pattern
pip install pyspellchecker
pip install autocorrect
pip install textblob
pip install textdistance

### Conclusion
As we have seen, NLP plays a crucial role in enabling computers to understand and process natural human language. This is as implemented above using the autocorrect system.

You can find the full working code here.

To summarize, we have:

Learned what Natural Language Processing is and its ability to autocorrect words.
Explored the autocorrect system and the various steps taken to build it.
Implemented an autocorrect system using NLP with Python.
Happy coding.
