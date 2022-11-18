# It's a man's canvas

# Abstract 

The film industry is huge and as something that reaches so many people in the world, it is bound to influence our culture. Successful movies appease their viewers, mirroring a part of society. Therefore, movies take an important place in our lives. With the subject of the gender gap being hotter than ever, the question of how female representation in this industry arises.  We aim to analyze the inequalities between men and women on and off-screen in this project with the data from the CMU movies summary dataset. Our goal is to compare data from different genres, geographical areas, and periods and visualize any evolution. The motivation behind it is to understand and grasp the problem so that this industry can solve inequality in the future. 


# Research Questions 

List of research questions analysed in this project:
- 1. How can the gender gap in the movie industry be grasped?
- 2. Is there a difference of gender gap between genres?
- 3. What is the gender gap across the world and how did it evolve over time?
- 4. How will the gender gap evolve in the future and how long will it take for it to be closed?
- 5. Is there a certain toppic that correlates with one gender?
- 6. Is there a correlation with off screen inequality and on screen inequality?

# Proposed additional datasets 
Additional dataset: 

- 1. title.akas.tsv.gz, from IMDb https://www.imdb.com/interfaces/ that contains movie titles and tconst
- 2. name.basics.tsv.gz, from IMDb https://www.imdb.com/interfaces/ that contains writers/directors id and their names
- 3. title.crew.tsv.gz, from IMDb https://www.imdb.com/interfaces/ that contains the director and writer information for all the titles
- 4. male.txt and female.txt, from https://www.cs.cmu.edu/Groups/AI/areas/nlp/corpora/names/ to identify writers/directors gender from names
- 5. (Potential) Movie Bechdel Test Scores https://www.kaggle.com/datasets/alisonyao/movie-bechdel-test-scores, that contians IMDb movie id and if a movie pass the Bechdel Test. This dataset can be used as an indicator for the active presence of women in the movie industry. 

# Methods

Q1: Both the on and off screen inequalities have to be taken into account:
- Ratio male/ female (cast, directors, writers): Gender of cast is given, gender of director & writer has to be concluded from the name. Careful with handling of gender neutral names) 
- Age distribution male/ female of cast
- Find stereotypical gender roles based on the movie summary and tvtropes.clusters.txt with sentinel analysis. Find gender by name or pronouns (https://stanfordnlp.github.io/CoreNLP/index.html) 

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

- 25.11: 
  Take Milestone 2 feedback into account, make necessary changes. 
  Validate statistics until Q4 (Besides gender representation based on characters on screen)
- 2.12: 
  Do plot summary analysis for Q5 and character representation
- 9.12:
  Combine previous analysis for Q6
- 16.12: 
  Create story with figures and text, finilize git repository

# Organization within the team

- Yichen: Handling of CMU datasets, analysis of genres.
- Yinghui: Analysis of age distribution of cast, gender ratio of crews, common adjective and noun.
- Sophia: Handling of CMU datasets, analysis of countries/languages.
- David: Handling of IMDb datasets, extract words around pronouns.

by YiYiSoDa
