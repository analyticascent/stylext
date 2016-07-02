# Stylext
I began this project as a capstone for a [General Assembly course](https://generalassemb.ly/education/data-science/) I took in the spring of 2016. Work obligations (and the need to keep making minimum payments on a credit card) inhibited me from finishing the project to the level of complexity I originally intended. However, I decided to continue working on it in order to prepare myself for future data science projects/courses. It has served as useful practice for (and demonstration of) data acquisition, pre-processing, and analysis.

Anyone who is familiar with the Iris classification problem can conceptually understand how this project works. Instead of petal measurements however, average occurance of certain characters per tweet is used. More sophisticated machine learning features can be used, but simplicity is prioritized over accuracy for demonstration purposes.

I will continue improving this project by experimenting with other various machine learning models and ensemble techniques. After the course, it will now go through the following stages:

* Create a time-series model that can "fingerprint" user tweet habits (potentially giving away their time zone).
* Expand the entire model to include more training features, and the feeds of all US senators and representatives.
* Continue improving the accuracy over time while also developing ways of subverting those same techniques as well.

There are numerous ways of defining ideal accuracy and a near infinite number of ways of combining various features in various model approaches. This will be an open-ended project that I intend to continue improving until I get too occupied with other things. That likely will not be an issue until next year, maybe.

#### Stages for First Iteration:

* Acquire Tweets using a Tweepy API script
* "Fingerprint" feeds using Ipython notebook
* Use machine learning for Tweet attribution

#### Ongoing Experimentation:

* Different Twitter datasets
* Varied choice of features
* Other attribution models

The end goal with all this is a utility that can disguise the writing style of a user as well as make it more readable to a general audience. It aims to be simpler to understand than jstylo and anonymouth. The full description for this project can be [read here](https://github.com/analyticascent/stylext/blob/master/Stylometric%20Analysis%20and%20Obfuscation%20Using%20Python.mdown).
