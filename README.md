
# OVOS Datasets

All datasets released under the Creative Commons Attribution-ShareAlike 4.0 International (CC BY-SA 4.0) license. 

* [utterance_tags_v0.1.csv](#utterance-tags-v01csv)
  + [Description](#description)
  + [Labels](#labels)
  + [Samples](#samples)
* [corefiob_v0.1.txt](#corefiob-v01txt)
  + [Description](#description-1)
  + [Labels](#labels-1)
  + [Samples](#samples-1)


## utterance_tags_v0.1.csv

### Description

This dataset contains 1187 labeled utterances that fall into three categories: COMMAND, QUESTION, and SENTENCE. 
Each label has sub-labels that describe the type of utterance, such as ACTION, DENIAL, QUERY, and REQUEST. 

The purpose of this dataset is to provide labeled examples of various types of commands, questions, and sentences that can be used for training natural language processing (NLP) models.


### Labels

- COMMAND: This label refers to statements that give instructions or orders. These can be further divided into sub-labels ACTION and DENIAL.
  - ACTION: This sub-label refers to commands that instruct the listener to perform an action.
  - DENIAL: This sub-label refers to commands that instruct the listener to refrain from performing an action.
- QUESTION: This label refers to statements that ask for information. These can be further divided into sub-labels QUERY, YESNO and REQUEST.
  - QUERY: This sub-label refers to questions that ask for information or definitions.
  - REQUEST: This sub-label refers to questions that make a request.
  - YESNO: This sub-label refers to questions that can be answered with a simple "yes" or "no"
- SENTENCE: This label refers to statements that do not fit into either of the above categories.
  - EXCLAMATION: This sub-label refers to sentences that express strong emotions such as excitement, surprise, or admiration.
  - SOCIAL: This sub-label refers to sentences that are used in social situations to express well-wishes or greetings.
  - STATEMENT: This sub-label refers to sentences that make a statement or convey information.
    

### Samples
```
COMMAND:ACTION,Boil some water
COMMAND:ACTION,Bring me a glass of water
COMMAND:ACTION,Brush your teeth
COMMAND:ACTION,Call John
COMMAND:DENIAL,Don't eat that, it's spoiled
COMMAND:DENIAL,It is prohibited to smoke in this building
COMMAND:DENIAL,Smoking is strictly prohibited in this area
COMMAND:DENIAL,Stay away from the edge
COMMAND:DENIAL,Stop running right now
COMMAND:DENIAL,You are not allowed to go outside
COMMAND:DENIAL,You are not allowed to smoke in this area
QUESTION:QUERY,How many people are in the room
QUESTION:QUERY,How much does it cost
QUESTION:QUERY,What are the office hours
QUESTION:QUERY,What can we speak
QUESTION:QUERY,What day is Christmas
QUESTION:REQUEST,Would you mind passing me a napkin
QUESTION:REQUEST,Would you mind passing me a tissue
QUESTION:REQUEST,Would you mind passing me the salt
QUESTION:REQUEST,Would you mind passing me the salt, please
QUESTION:YESNO,Are Spanish and German different languages
QUESTION:YESNO,Are airplanes flown inside
QUESTION:YESNO,Are all dogs friendly
QUESTION:YESNO,Are ants strong
SENTENCE:EXCLAMATION,What an amazing experience
SENTENCE:EXCLAMATION,What an impressive accomplishment
SENTENCE:EXCLAMATION,What an impressive performance by the dancers
SENTENCE:SOCIAL,Congratulations on your promotion
SENTENCE:SOCIAL,Enjoy your weekend
SENTENCE:SOCIAL,Get well soon
SENTENCE:SOCIAL,Good luck on your exam
SENTENCE:SOCIAL,Good luck with your interview
SENTENCE:SOCIAL,Good morning
SENTENCE:STATEMENT,The sky is so blue today
SENTENCE:STATEMENT,The sun is a star that is located at the center of our solar system
SENTENCE:STATEMENT,The sun rises in the east and sets in the west
```


## corefiob_v0.1.txt


### Description

This is a dataset for coreference resolution consisting of 123 sentences in CoNNL format. 
The dataset has been manually annotated to include coreference mentions of masculine, feminine, and inanimate entities. 
Additional entries have been included to expand the variety of coreference cases present in the dataset.

Each line of the dataset represents a token and its corresponding part-of-speech tag and entity tag. 
The entity tags denote the start and end of an entity mention, and whether it is a masculine, feminine, or inanimate entity, and if it is the coreference mention, using the BIO scheme.

The dataset is suitable for training feature extractors for coreference resolution models.

### Labels

The annotations follow the following scheme:

- B-ENTITY-MALE: Beginning of a male entity mention
- I-ENTITY-MALE: Inside of a male entity mention
- B-ENTITY-FEMALE: Beginning of a female entity mention
- I-ENTITY-FEMALE: Inside of a female entity mention
- B-ENTITY-INANIMATE: Beginning of an inanimate entity mention
- I-ENTITY-INANIMATE: Inside of an inanimate entity mention
- B-ENTITY-PLURAL: Beginning of a plural entity mention
- I-ENTITY-PLURAL: Inside of a plural entity mention
- B-COREF-MALE: Beginning of a coreference mention of a male entity
- I-COREF-MALE: Inside of a coreference mention of a male entity
- B-COREF-FEMALE: Beginning of a coreference mention of a female entity
- I-COREF-FEMALE: Inside of a coreference mention of a female entity
- B-COREF-INANIMATE: Beginning of a coreference mention of an inanimate entity
- I-COREF-INANIMATE: Inside of a coreference mention of an inanimate entity
- B-COREF-PLURAL: Beginning of a coreference mention of a plural entity
- I-COREF-PLURAL: Inside of a coreference mention of a plural entity

### Samples

```
Korgoth	PROPN	B-ENTITY-MALE
of	ADP	I-ENTITY-MALE
Barbaria	PROPN	I-ENTITY-MALE
is	AUX	O
here	ADV	O
,	PUNCT	O
He	PRON	B-COREF-MALE
is	AUX	O
a	DET	O
savage	NOUN	O
!	PUNCT	O

Here	ADV	O
is	AUX	O
the	DET	B-ENTITY-INANIMATE
book	NOUN	I-ENTITY-INANIMATE
now	ADV	O
take	VERB	O
it	PRON	B-COREF-INANIMATE
```