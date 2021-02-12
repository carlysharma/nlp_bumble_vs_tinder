# Executive Summary 

*WARNING: The visuals in this summary and project contain vulgar language pulled from Reddit.com online communities.*

As a single person in the US hoping to get into a serious relationship, it feels impossible to know where to look. According to a [2019 study](https://news.stanford.edu/2019/08/21/online-dating-popular-way-u-s-couples-meet/) by Standford sociologist, Michael Rosenfeld, 39% of heterosexual couples reported meeting online. Phone apps are the go-to method for meeting a partner online, but how do you pick which one is best? You have limited time and don't want to waste it on an app where the majority of people are looking for something casual or just a good story. While getting a few friends' opinions can be helpful, ideally you could analyze hundreds of conversations from people using different apps.

Because recording strangers' conversations would be time-consuming, unethical, and near-impossible, you need a better way to collect and analyze large amounts of conversational data about dating apps. 

Luckily we have online communities full of discussions that are free for the public to access, specifically Reddit. By analyzing 1000 posts from each the two most popular app-specific, dating subreddits ([Tinder](https://www.reddit.com/r/Tinder/) and [Bumble](https://www.reddit.com/r/Bumble/)) we can compare which community seems to be more serious about dating vs. the other. 

First, we used natural language processing to translate these posts into a language the computer could understand. Once "translated", we used this data to build various models that analyzed the differences in title/post text between each subreddit. By doing so we could first figure out if enough differences even exist to disinguish between the two. Our dataset started with 49% Tinder posts and 50% Bumble posts so our models needed to predict whether a post was from Bumble or Tinder better than 50% of the time. After testing 6 different models through pipelines and gridsearches we found a model that was accurate 73% of the time.

After were able to verify there were distinguising elements between the two subreddits, we pulled out the most common words and patterns to analyze whether or not the conversations seem to be about finding love/getting into serious relationships or not. 

While we analyzed single most common words as well as bigrams (pairs) and trigrams(3 words), the trigrams were the most telling with regards to seriousness as you can see below.

![Bumble Top 20 Trigrams](images/Bumble_Top_20_Trigrams.png "Bumble Top 20 Trigrams")

*Mostly serious phrases like "long distance relationship" or "new online dating" (potentially indicating they are new and looking for advice).*

![Tinder Top 20 Trigrams](images/Tinder_Top_20_Trigrams.png "Tinder Top 20 Trigrams")

*The vulgar language here indicates less seriousness and looking more for hookups.* 

The length of Bumble posts were close to 4x as long as Tinder posts. 

Bumble average length: 52 words<br> 
Tinder average length: 22 words

![Distribution Word Counts](images/Dist_Word_Counts.png "Distribution of Word Counts")


Our goal was to recommend either Bumble or Tinder as an app you should invest your time in as a single person looking for a serious relationship. While there is no harm signing up for every app, we're assuming you have limited time and don't want to waste it within a commuity of people who are less likely to want something serious. Therefore, our recommendation would be to sign up for Bumble and don't sign up for Tinder.

*Additional notes: Bumble is only in the US and Tinder is international. The posts here could be from anywhere. Each demographic and location could be different for each subreddit. Specifically, I believe your age group can have a large affect on which app may have more of your peers. Many of these posts contain images of text I was unable to analyze but I believe would be very telling.*
