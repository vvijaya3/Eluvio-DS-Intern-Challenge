# Eluvio-DS-Intern-Challenge
Eluvio NLP DS problem
The csv file contains 8 columns: created date, created time, up vote, down vote, title, author, over 18 and category.

After simple checking, it can be found that all the news belong to one category (world news) and the down votes are all zero. Thus, it will be interesting to explore the relationship with the up vote and other covariates.
Additionally, 85838 authors are included. Because of the large amount of the authors, here I only provided the first five authors with the highest average up votes.

author	Ave.up votes
navysealassulter	12333
seapiglet	11288
DawgsOnTopUGA	10515
Flamo_the_Idiot_Boy	10289
haunted_cheesecake	9408

However, I think there might be a strong relationship between the title and the up votes: 1) The title is related with the news content and the attractive content will obtain more up votes; 2) Interesting title will attract more readersm, which in turn will get more up votes. In order to study this relationship, we will use classify the news into two groups, one is attractive news and another is non-attractive news. This classification is based on a threshold determined by the data pattern. Also, the title will be converted to a numerical vector with the Universal Sentence Encoder.

Step 1: Data Processing
Step 2: the Universal Sentence Encoding
Step 3: Deep Neural Network Classifier
Because the data is unbalanced: attractive/nonattractive $\approx$ 3/7. So I oversample the attracive news for the training: in each batch, the sample weights for attractive/nonattractive news are 0.7/0.3, repectively.

