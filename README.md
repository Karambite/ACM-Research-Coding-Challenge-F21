# ACM Research Coding Challenge (Fall 2021)

## [](https://github.com/ACM-Research/Coding-Challenge-F21#no-collaboration-policy)No Collaboration Policy

**You may not collaborate with anyone on this challenge.**  You  _are_  allowed to use Internet documentation. If you  _do_  use existing code (either from Github, Stack Overflow, or other sources),  **please cite your sources in the README**.

## [](https://github.com/ACM-Research/Coding-Challenge-F21#submission-procedure)Submission Procedure

Please follow the below instructions on how to submit your answers.

1.  Create a  **public**  fork of this repo and name it  `ACM-Research-Coding-Challenge-F21`. To fork this repo, click the button on the top right and click the "Fork" button.

2.  Clone the fork of the repo to your computer using  `git clone [the URL of your clone]`. You may need to install Git for this (Google it).

3.  Complete the Challenge based on the instructions below.

4.  Submit your solution by filling out this [form](https://acmutd.typeform.com/to/zF1IcBGR).

## Assessment Criteria 

Submissions will be evaluated holistically and based on a combination of effort, validity of approach, analysis, adherence to the prompt, use of outside resources (encouraged), promptness of your submission, and other factors. Your approach and explanation (detailed below) is the most weighted criteria, and partial solutions are accepted. 

## [](https://github.com/ACM-Research/Coding-Challenge-S21#question-one)Question One

[Sentiment analysis](https://en.wikipedia.org/wiki/Sentiment_analysis) is a natural language processing technique that computes a sentiment score for a body of text. This sentiment score can quantify how positive, negative, or neutral the text is. The following dataset in  `input.txt`  contains a relatively large body of text.

**Determine an overall sentiment score of the text in this file, explain what this score means, and contrast this score with what you expected.**  If your solution also provides different metrics about the text (magnitude, individual sentence score, etc.), feel free to add it to your explanation.   

**You may use any programming language you feel most comfortable. We recommend Python because it is the easiest to implement. You're allowed to use any library/API you want to implement this**, just document which ones you used in this README file. Try to complete this as soon as possible as submissions are evaluated on a rolling basis.

Regardless if you can or cannot answer the question, provide a short explanation of how you got your solution or how you think it can be solved in your README.md file. However, we highly recommend giving the challenge a try, you just might learn something new!

## []Solution

This code utilizes the two most popular models for sentiment analysis - NLTK’s VADER and TextBlob. Vader was mainly utilized to analyze the text and provide a sentiment score for each sentence individually and a score for the entire passage holistically. TextBlob was mainly utilized to further analyze the text and each sentence by calculating a numerical value for how subjective the phrase is.

The result this program returns are the sentiment score and the subjectivity score. The sentiment score is the sum of the positive, negative, and neutral scores normalized between -1 (extremely negative) and +1 (extremely positive), known as the compound. I decided to only display the compound score as it presents a simpler and holistic evaluation of the text. The subjectivity score gives insight into how emotional or factual the text is. This score ranges from 0(highly objective) to 1(highly subjective). A more subjective passage can correlate to a higher sentiment score.

The sentiment score the program gave the input text was a .99, which seems to contrast the sentence-by-sentence analysis. A sentiment score of .99 implies it is extremely positive, however, the data table of sentences shows plenty of neutral and extremely negative sentences. An expected score or a more appropriate score, in my opinion, would range between .65 - .75, indicating it’s mostly positive, but also acknowledging the negative and neutral sentences. The subjective score provided by the program is .5 which means it’s nearly split between objective and subjective statements. This, in my opinion is to be expected as the beginning of the text seemed to be objective but towards the end, the text consisted of emotional statements.

## [] Sources

https://github.com/Ankit152/IMDB-sentiment-analysis/blob/master/imdbSentimentAnalysis.ipynb - ideas for how to filter text

https://medium.com/@rahulvaish/textblob-and-sentiment-analysis-python-a687e9fabe96 - Understanding TextBlob

https://textblob.readthedocs.io/en/dev/ - TextBlob Documentation

https://docs.python.org/3/library/re.html#writing-a-tokenizer - re library Documentation

https://www.nltk.org/ - nltk Documentation


