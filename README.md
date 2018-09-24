# Stylext: A Twitter Stylometry Proof of Concept
#### *Authorship Attribution and Obfuscation with Machine Learning (Scikit-Learn)*

&nbsp;

**Introduction:** The files in this repo can easily be used by anyone to learn basic text classification techniques. This is a supervised machine learning program that uses binary text classification to determine which of two Twitter users authored various posts on Twitter. No worries if that terminology sounds too complex to learn, the core concepts are straightforward:

* **Supervised Machine Learning** involves training an algorithm to tell the difference between various things by feeding in labeled examples of things in each category you wish to sort new data (text, images, etc) into. In this case, we are feeding in tweets that are known to have come from one Twitter user in addition to ones that came from another. The file read into the main Jupyter Notebook has the tweets labeled by the user they each came from.
* **Binary Text Classification** simply means using a text classifier to sort new text samples into one category or another. In the case of Stylext, it is which of two people wrote a Tweet. Essentially we are taking the same general approach that many spam filters use to sort text passages, except we are attributing the authorship of tweets.

To appreciate why machine learning is beneficial for the task Stylext was coded for, consider two scenarios - determining if a number is even versus determining which person wrote a 140-character post. In the case of prime numbers, you only need to check for the following conditions: *Is the number divisible only by itself and the number 1?*

So any programming language would simply need to take the following approach: ***If** dividing an integer by two leads to a whole number, **Then** return "Even" - **Else** return "False"*

The corresponding python code for this problem is simple for even non-programmers to follow:

```python
def is_even(n):
    if n % 2 == 0: # checks if dividing by two leads to a whole number
        return "Even"
    else:
        return "Odd"
```

This is obviously a *low-dimensional* problem, and relatively easy to code for in most programming languages. Most will allow you to solve the problem with five or fewer lines of code.

But consider a scenario involving *high-dimensional* data, such as raw text. Text can be *vectorized* - that is, quantified by things like how often unique words, or even multi-word sequences appear in a document. Those corresponding values can be used as a "statistical fingerprint" of how to distinguish text samples from each other. But as you can imagine, writing a series of "if, then, else" statements to account for every possible arrangement of words in a document.

Stylext uses a *supervised machine learning* approach to the task at hand. Rather than try to write separate conditional statements for every possible arrangement of 140 characters (this project was completed in the spring of 2016). There are literally orders of magnitude more ways of writing a tweet than there are atoms in the entire solar system (10<sup>250</sup> combinations using alphanumeric characters in English alone). It would be impractical to write a conditional statement for each of these! Machine learning on the other hand will only require that we have enough labeled examples to train a text classifier to "fingerprint" one Twitter user from another.

---

**The technical description for this project can be [read here](https://github.com/analyticascent/stylext/blob/master/Stylometric%20Analysis%20and%20Obfuscation%20Using%20Python.mdown).** 

**Context:** I began this project as a capstone for a [General Assembly course](https://generalassemb.ly/education/data-science/) I took in the spring of 2016. Work obligations (and the need to keep making minimum payments on a credit card) inhibited me from finishing the project to the level of complexity I originally intended. However, I decided to continue working on it in order to prepare myself for future data science projects/courses, and it ultimately was satisfactory enough to meet course requirements. 

It has served as useful practice for (and demonstration of) data acquisition, pre-processing, and analysis. This repository can be used to learn the basics of all three in the context of how supervised machine learning works, with respect to natural language processing in particular.

Twitter was the main target for experimental data due to the site's ease of use API, as well as to test an *assumption* online friends friends of mine had: that the 140-character post limit prevents "unique" text styles (known as *writer invariants*) from manifesting compared to more open-ended social media platforms. **This assumption turned out to be *dead* wrong.** 

The reason this hypothesis turned out to be wrong ended up being very straightforward: Due to the fact that many Twitter features thar are meant to make the most of that character limit (hashtags, emojis, retweeting, hyperlinks, etc) are *used variably* among users, the same quantity of raw text from any Twitter user can be just as distinct (if not more) than from other sites.

**Future Prospects:** The end goal with this project is a stand-alone tool that can disguise the writing style of a user while - as a possible bonus - making the text more readable to a general audience. I was inspired to develop this when pseudonymous writers in a [Freenet](https://freenetproject.org/) discussion group I frequented became aware of the work of researchers at [Drexel University on Stylometry.](https://www.cs.drexel.edu/~sa499/papers/adversarial_stylometry.pdf)

Stylext aims to be simpler to use and easier to modify than jstylo and anonymouth; both of which were the subject of complaints among those I recommended them to for not being easy to install/run/understand for laypersons. I have done my best to abide to the "don't trust what you can't comprehend" principle that some in the world of privacy tenaciously adhere to.

Anyone who is familiar with the Iris classification problem can conceptually understand how this project works. Instead of petal measurements however, average occurence of certain characters per tweet is used. More sophisticated machine learning features can be used, but simplicity is prioritized over accuracy for demonstration purposes. This should make the tool more accessible to those who intend to use it for themselves.

---

**What You Will Need to Run the Notebooks:** The bare minimum needed to run the IPython notebook (IPNB) files is the [anaconda python distribution](https://www.continuum.io/downloads) (version 3).

To work with something beyond the demo CSV files of tweets I used, you will need either the "Tweepy" python library installed or something that downloads a twitter feed in CSV form via API or web scraping (not recommended).

I will continue improving this project by experimenting with other various machine learning models and ensemble techniques. After the course, it will now go through the following stages:

* Create a time-series model that can "fingerprint" user tweet habits (potentially giving away their time zone).
* Expand the entire model to include more training features and the feeds of all US senators and representatives.
* Continue improving the accuracy over time while also developing ways of subverting those same techniques as well.

There are numerous ways of defining ideal accuracy and a nearly infinite number of ways of combining various features in various model approaches. This will be an open-ended project that I intend to continue improving until I get too occupied with other things. That likely will not be an issue until next year, maybe.

#### Stages Executed for Project Completion:

* Acquire Tweets using a Tweepy API script
* "Fingerprint" feeds using Ipython notebook
* Use machine learning for Tweet attribution

#### Ongoing Experimentation You May Want to Try:

* Different Twitter datasets
* Varied choice of features
* Other attribution models

New development from yours truly will cease altogether when (a) time put into it gives diminishing accuracy returns, and (b) other projects begin taking up the bulk of my time. Not so unusual of a set of benchmarks now is it? 
