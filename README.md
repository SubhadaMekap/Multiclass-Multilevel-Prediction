# Multiclass-Multilevel-Prediction
Given text for Questions , predict tags associated with them
**Programming Language** : Python using nltk & Keras

**Model Architecture** : Deep Learning using Recurrent Neural Network (RNN)

**About Data Set** 

Dataset has text of questions, answers and thier corresponding tags from the Stack Overflow programming Q&A website.

This is organized as three files:

1. Questions contains the title, body, creation date, closed date (if applicable), score, and owner ID for all non-deleted Stack Overflow questions.

2. Tags contains the tags on each of these questions.

3. Answers contains the body, creation date, score, and owner ID for each of the answers to these questions. The ParentId column links back to the Questions table. *We don't use this file as we want to predict Tags given a question*

**Data Pre-Processing**

>Questions File
*Code* : Stackoverflow Clean Questions.ipynb

1. Read Questions File
2. Drop All columns except Id,Title and Body
3. Now the text in the Body column seem to have many html tags in the text. We use Regular Expressions and Clean the Body column text by removing the html tags
```python
