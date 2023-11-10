# Natural-Language-Processing
> You will find the reference [**here**](https://youtu.be/nknYY32RGXQ?si=taKCV2td8PM1luEl)


There are **three** types of techniques that are used in natural language processing (on a broader aspect).

- [Heuristics & Rules (Regular Expression)](#Regular-Expression)
- Machine Learning **(text classification or spam detection)**
- Deep Learning
    - Sentence Embedding

<br><br>

# Regular Expression
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

// output: 412889912
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

// output: June 28, 1971
```

>The code above extracts the **date of birth** from the given text.