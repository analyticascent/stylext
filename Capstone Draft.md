# Stylometric Analysis and Obfuscation Using Python

#### Using Machine Learning to Attribute or Conceal Content Authorship

___

This is a tentative draft, exact steps and practical goal may be subject to pivot.

**Question:** *What type and quantity of information would we need to identify users on "anonymous" social media applications such as Yik Yak?*

**Summary:** *Stylometry* is the statistical analysis of variations in textual writing style between different authors, usually in order to determine authorship of unattributed passages of text. For privacy purposes, stylometry can also be used to hide the true source of any text passages by altering or diluting the author's original literary style.

*My practical goal for this project is to determine how much information is necessary to de-anonymize users of applications such as Yik Yak, which people use under the impression that postings cannot be directly attributed to them.*

___

**Stages:** This project will start by constructing a functional stylometric utility in python that makes use of natural language processing features. From there, a subset of the Enron email corpus (thirteen emails by fifty authors) will serve as a demo set to improve the performance of the script(s). My target goal is to have a statistical learning script that can accurately identify set authorship of at least 30 of the 50 former employees through statistical learning of the whole set of 650 emails.

The use of data from Twitter's API can be utilized if the Enron set proves to be an insufficient supply for a machine learning program. From there, the practical project testing begins:

 1. First, I will search Twitter using twython and the site's API in order to gather a "training" data set. This set will by people who are centered at a University and explicitly say they use Yik Yak according to their Twitter feed.
 2. From there, I will begin gathering post samples for various user handles that are visible through the app in those locations. The goal is to increase the likelihood that I am working with Yik Yak postings that are made by people I can cross-reference on Twitter as a training set.
 3. Finally I will attempt to see if authorship of posts under a Yik Yak handle can be attributed to Twitter users that go to that same University. My question is less about **if** this is possible but more about **how much** information is necessary to successfully do this.

Current research indicats that I would need at least **5,000 words** from a given user before stylometric analysis can become reliable. Below is a good overview of current research on this topic in the context of online black markets:

[![Stylometry and Undeground Markets](http://img.youtube.com/vi/xL9aam3ZUlk/0.jpg)](http://www.youtube.com/watch?v=xL9aam3ZUlkE "Stylometry and Undeground Markets")

Additional resources will be added to this file as I find and index them.

___
 
**Python Programming:** More or less what I am aiming for is a supervised machine learning program that can identify author invariances within any given 5,000 word set. Author invariances are characteristics of written passages that are measurably unique throughout much, if not *all* of what they write.

One of the reasons I chose this project in the first place is because it strongly overlaps with something similar I was already planning to work on: *readability analysis.* The same string tools that detect things like *stop words* or perform letter/syllable/word counts can also be used to detect literary styles between different writing samples. 

For example, if I wanted to count the number of syllables in a phrase I could do so in python [using letter pairs in strings](http://stackoverflow.com/questions/14541303/count-the-number-of-syllables-in-a-word). Aside from syllable count, other features the initial program could look for may include...

- **Synonyms:** There are many ways of saying the same thing in any given language, and if someone consistently uses the same choice of synonyms throughout all text, that could prove to be a predictively accurate form of author invariant to look for in training sets.
- **Punctuation:** Average sentence length can vary from author to author as well as choice of commas versus semicolons in different contexts.
- **Letter/Word Pairs:** If a pair of letters or word transitions is unique to an author throughout their writing, these should be easy to detect.

More methods to be found, and test in implementation.

