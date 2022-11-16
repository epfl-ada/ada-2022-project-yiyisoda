# It's a man's canvas

# Abstract: 
(A 150 word description of the project idea and goals. What’s the motivation behind your project? What story would you like to tell, and why?)

The film industry is huge nowadays and as something that reaches so many people in the world it is bound to influence our culture. On the other hand, successful movies must appease to its viewers, therefore representing a part of society. Therefore, movies take an important place in our lives. With the subject of gender gap being hotter than ever, the question of how the female representation in this industry is arises. 

With this project the inequalities between men and women on and off screen is analysed. The motivation behind it is to properly understand and grasp the problem so that it can be solved at the right place in the future. The differences across the world, between genres and over time should be shown for that. 


# Research Questions: 
(A list of research questions you would like to address during the project.)

List of research questions analysed in this project:
- 1. How can the gender gap in the movie industry be grasped?
- 2. Is there a difference of gender gap between genres?
- 3. What is the gender gap across the world and how did it evolve over time?
- 4. How will the gender gap evolve in the future and how long will it take for it to be closed?
- 5. Is there a certain toppic that correlates with one gender?
- 6. Is there a correlation with off screen inequality and on screen inequality?

# Proposed additional datasets (if any)
(List the additional dataset(s) you want to use (if any), and some ideas on how you expect to get, manage, process, and enrich it/them. Show us that you’ve read the docs and some examples, and that you have a clear idea on what to expect. Discuss data size and format if relevant. It is your responsibility to check that what you propose is feasible.)

Add:
title.crew.tsv.gz – Contains the director and writer information for all the titles in IMDb. Fields include:
tconst (string) - alphanumeric unique identifier of the title
directors (array of nconsts) - director(s) of the given title
writers (array of nconsts) – writer(s) of the given title

# Methods

Q1: Both the on and off screen inequalities have to be taken into account:
- Ratio male/ female (cast, directors, writers): Gender of cast is given, gender of director & writer has to be concluded from the name. Careful with handling of gender neutral names) 
- Age distribution male/ female of cast
- Find stereotypical gender roles based on the movie summary and tvtropes.clusters.txt with sentinel analysis. Find gender by name or pronouns (https://stanfordnlp.github.io/CoreNLP/index.html) 
- Usage of Bechtel-test data: https://www.kaggle.com/datasets/alisonyao/movie-bechdel-test-scores

Q2-Q3: The insight from question 1 has to be analysed with respect to genre, language of movie and release date. 

Q4: Build a regression based on insights of question 1.

Q5: In order to find recuring toppics for a specific gender topic modeling on genderis done to extract keywords around two genders.

Q6: create a correlation matrix with gender distribution for writer and director is done with the other features describing the gender gap.

In dept description of how to analyse movie plots for Q1 & Q5:
1. Split plot description into sentences describing female/ male character according to pronoun or name
2. Exctract verbs/ adjectives/ nouns with https://spacy.io/ or https://www.nltk.org/
3. Stemming & Lemmatizing words: reduce words to their root (e.g. “helping” and “helper” share the root “help.”) with https://www.nltk.org/
4. Categorizing extracted words according with https://github.com/Ejhfast/empath-client / or by training own model: https://radimrehurek.com/gensim/models/ldamulticore.html
5. Frequency Distribution on how often a word appears: https://www.nltk.org/ or with wordcloud: https://github.com/amueller/word_cloud

# Pipeline
![image](https://github.com/epfl-ada/ada-2022-project-yiyisoda/blob/main/pipeline.png)
# Proposed timeline
(Organization within the team: A list of internal milestones up until project Milestone P3.)

- 21.11.: Take Milestone 2 feedback into account, make necessary changes. 
- 27.11.: Compute statistics until question 4 (Besides gender representation based on characters on screen)
- 11.12.: Do plot summary analysis for question 5 and character representation
- 15.12.: Compute all necessary statistics
- 20.12.: Create story with figures and text, finilize git repository


Questions for TAs (optional): Add here any questions you have for us related to the proposed project.

by YiYiSoDa
