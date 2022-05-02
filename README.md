# Adv_ML_project
NLP For Indic Renaissance

Team members: 
Tirumala Kaggundi      
Dhruv Sinha

Introduction

Over the last few decades, there has been a lot of research done in the field Natural Language Processing. We have packages and modules that are able to identify languages, tag each word with their corresponding parts of speech, summarize a given paragraph, and also create content based on a prompt. While a lot of work has been done in ‘English’, we realized that application of NLP functionalities in Indian languages is very limited. Through this project, we will leverage NLP to perform 3 main tasks, but on texts from different Indian languages. 

There are copious texts generated daily in different parts of India in the form of newspapers, movies, or social media articles. Moreover, the coverage of this content is significantly large. In India, everyone is consuming content in vernacular languages in some way or the other. Therefore, it would be interesting to test some basic functionalities of NLP on these vernacular languages. This would allow us to understand if we need to modify the way we use traditional NLP algorithms when we work on vernacular languages. However, this comes with a significant challenge as the content is not available in an aggregated format that can be used for training. Therefore, we would rely upon publicly available texts from wikipedia articles in Indian languages and certain sources on the web (e.g. BBC news Hindi) to obtain our training data. Similar approach has been taken other developers working in this area (References indicated below) 

Milestones for the project

Language Identification
Parts of Speech tagging
Paragraph generation in Hindi language

Milestone 1

Language detection task: 

In this milestone, we will be categorizing whether a given text belongs to one of the Indian languages from a set of {Hindi, Malayalam, Kannada, Tamil, Bengali}. For this we will create a Bag of Vectors for each language. Here are the steps that we aim to implement- 

Collate the dataset for each language. We will use the Hindi, Kannada, Tamil, Malayalam, and Bengali Wikipedia articles to train our model. 
Use publicly available tokenizers (or generate a new one if possible - stretch goal) to create a Bag of Words 
Create a Bag of Words classifier using linear layers
Train the Classifier 

For Language Identification, a lot of work has been done to classify and identify languages with latin as the predominant script. Some work has also been done to identify Chinese, Japanese, and Korean languages. Jauhiaihen et al has done a detailed survey on the literature that exists for Language Identification tasks. Kerwin (2006) used character frequencies as feature vectors. In a feature vector, each feature vector f has its own integer value. Raw frequency and relative frequency for each feature is calculated for each language. For our project, we will be using something very similar. 

There are several intuitive techniques that are used to classify languages- 
Position of words- Kumar et al. (2015) used the position of the current word in word-level LI. 
Dictionary of unique words: Unique word dictionaries include only those words of the language, that do not belong to the other languages targeted by the language identifier.
Discriminating words Kolkus (2009) used the most relevant words for each language


Milestone 2: 

Part of speech tagging: 

The way the part of speech works in Hindi is different from the way it works in latin based languages due to syntactic differences and morphological richness in Hindi language construction and grammar rules. However, from NN point of view, it shouldn’t be very different as we are just tagging the parts of speech based on the training data. We will attempt to develop part of speech tagging for Indian language (Hindi alone) at this milestone. This may be an intensive task if we don’t get good training data and end up generating instances for tagging. 

Milestone 3: - Stretch goal

Paragraph generation using Transformer models: 

We will attempt to generate a paragraph of text in Hindi language based on a given prompt. We would attempt to train the model based on available online speech of the Prime Minister of India (Mr Narendra Modi) and examine if the prompt is able to generate a paragraph that matches the style closely. We would also examine if the approach can be extended to some famous authors in Hindi language such as Shri Munshi Premchand. 


References

Thomas Kerwin. Classification of Natural Language Based on Character Frequency. Ohio
Supercomputer Center, 2006

Rahul Venkatesh RM Kumar, Anand M Kumar, and KP Soman. AmritaCEN NLP @ FIRE
2015 Language Identification for Indian Languages in Social Media Text. In Working
Notes of the Forum for Information Retrieval Evaluation (FIRE 2015), pages 28–30,
Gandhinagar, India, 2015.

Radim Rehurek and Milan Kolkus. Language Identification on the Web: Extending the
Dictionary Method. In Proceedings of the 10th International Conference on Intelligent
Text Processing and Computational Linguistics (CICLing-2009), pages 357–368, Mexico
City, Mexico, 2009

Tommi Jauhiainen, Marco Lui, Marcos Zampieri, Timothy Baldwin and Krister Lindén. Automatic Language Identification in Texts: A Survey. Cornell University Arxiv CS, 2018.
