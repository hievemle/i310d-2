# i310d-2
Assignment 2

In this perspective API exploration, I test my hypothesis of whether this API has a bias towards sex as it pertains to identifying toxicity scores of comments within the data set. I want to see if anti-female comments receive higher marked toxicity scores versus anti-male comments, despite being equally as demeaning or toxic, might receive a lower toxicity score, showing a bias within the API. 
To explore the dataset, we can conduct some data parsing to find the most common words used in comments where toxicity or abuse was present. Without my hypothesis in mind, the purpose of this code is to understand and see the behavior of the API. 

Against my hypothesis, I do not find a threshold of .5 as conclusive enough to determine whether a comment is toxic or not. So, I would use the threshold of .7 at which I would consider the comment to be toxic. 

Using the original dataframe, I created two dataframes that contain equivalent phrases, both toxic and non-toxic towards females and males.

My hypothesis is that the API will give lower toxicity scores towards anti-male comments versus anti-female comments. 

H0 = The perspective will deduce anti-female comments as MORE toxic than anti-male comments meaning the toxicity score will be GREATER THAN 0.7 and the anti-female scores will be GREATER THAN THE EQUIVALENT ANTI-MALE COMMENT'S TOXICITY SCORE.

H1 = The perspective will dedice anti-female comments as LESS THAN OR EQUALLY toxic than anti-male comments meaning the toxicity square will be EQUAL TO OR LESS THAN 0.7 and the anti-female scores will be LESS THAN OR EQUAL TO THE EQUIVALENT ANTI-MALE COMMENT'S TOXICITY SCORE.

The tests that I ran support my H0: Anti-female comments will earn higher toxicity scores than the equivalent anti-male comments. With my first five tests, I combined hate comments and obscenities which earned higher toxicity ratings and had a smaller range between the scores. 

Findings

1) With test 2, though it includes hate speech and an obscenity, only the female phrase is deemed toxic and has the second largest range out of the first four tests. In my opion, if it is the exact same phrase and the only thing that changes is the noun/gender, it should be deemed equally toxic. 

2) The ranges between the scores span from .009 - .15. 

The next five tests do not include obscenities. 

3) Test 2 and Test 10 are similar, but test 2 contains an obscenity. However, the API generated the same toxicity scores for both of them. This confuses me because I know the obscenity should raise the toxicity score, but in this case it doesn't. 

4) The ranges span from .07 - .25 (a greater range than the tests with obscenities).

5) I definitely do think the API has a bias towards scoring anti-women comments higher than anti-male, meaning there is a sex/gender based bias.

6) As to why there is this apparent bias, I believe it may be a societal norm that men are less discriminated against, thus leading to less data for male hate, thus the API is less trained to recognize or score as high in comparison to the more abundant women-geared hate comments. 

