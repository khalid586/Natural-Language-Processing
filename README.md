![](https://www.searchenginejournal.com/wp-content/uploads/2020/08/an-introduction-to-natural-language-processing-with-python-for-seos-5f3519eeb8368-1520x800.webp)

<h1 align = "center"> Natural Language Processing </h1>

<br>

## Types of NLP implementation
> You will find the reference [**here**](https://youtu.be/nknYY32RGXQ?si=taKCV2td8PM1luEl)


There are **three** types of techniques that are used in natural language processing (on a broader aspect).

- [Heuristics & Rules (Regular Expression)](#Regular-Expression)
- Machine Learning **(text classification or spam detection)**
- Deep Learning
    - Sentence Embedding

<br><br>

## Regular Expression
> You will find the reference [**here**](https://youtu.be/lK9gx4q_vfI?si=pUV4357oRl6Qehfl) 

<br>

**Task 1:** You are given a text (string) from a customer. You have to extract the order number from the customer's text.

Solution:

```py
import re

chat1='codebasics: Hello, I am having an issue with my order # 412889912'

pattern = 'order[^\d]*(\d*)'
matches = re.findall(pattern, chat1)
print(matches)

# output: 412889912
```

>The code above extracts the **order number** from the given text.

<br>

**Task 2:** You are given information about a person. You have to extract the date of birth of that person.

Solution:

```py

text='''
Born	Elon Reeve Musk
June 28, 1971 (age 50)
Pretoria, Transvaal, South Africa
Citizenship	
South Africa (1971–present)
Canada (1971–present)
United States (2002–present)
Education	University of Pennsylvania (BS, BA)
Title	
Founder, CEO and Chief Engineer of SpaceX
CEO and product architect of Tesla, Inc.
Founder of The Boring Company and X.com (now part of PayPal)
Co-founder of Neuralink, OpenAI, and Zip2
Spouse(s)	
Justine Wilson
​
​(m. 2000; div. 2008)​
Talulah Riley
​
​(m. 2010; div. 2012)​
​
​(m. 2013; div. 2016)
'''
def get_pattern_match(pattern , text):
    matches = re.findall(pattern, text)
    if matches:
        return matches[0]


print(get_pattern_match(r'Born.*\n(.*)\(age', text).strip())

# output: June 28, 1971
```

>The code above extracts the **date of birth** from the given text.

<br>

## Tasks performed using NLP
> You will find the reference [**here**](https://youtu.be/In7jB8TUGPA?si=3ABtO_tjCaRyiFVU) 


1. Text classification
    - Example
        - Facebook's hate speech detection 
        - Complaint severity detection in big companies
1. Text similarity
    - Example
        - Resume shortlisting
    - Technique used
        - Cosine similarity
1. Information extraction
    - Example
        - Google News
1. Information retrieval
    - Example
        - Google search engine's website listing
    - Technique used
        - TFIDF score
        - BERT
1. Chat Bot
    - Types
        - FAQ chatbot
        - Flow based bot
        - Open-ended bot
1. Machine translation
    - Example
        - Google translation
    - Technique used
        - Encoder/Decoder architecture of RNN
1. Language Modeling
    - Example
        - Auto completion of gmail
    - Techniques used
        - Statistical Model
        - Neural Model
1. Text summarization
    - Example : Scispace 
1. Topic Modeling (Retrieve topics from data)
    - Example : Google News
1. Voice assistant
    - Example : Alexa , Siri
