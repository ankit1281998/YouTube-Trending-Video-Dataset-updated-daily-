# YouTube Video Title Sentiment Analysis
YouTube Trending Video data-set which gets updated daily.

Dataset is available on Kaggle: https://www.kaggle.com/datasets/rsrishav/youtube-trending-video-dataset/data

Title Sentiment Analysis/ Tags Sentiment Analysis/ Description Sentiment Analysis: Analyze the sentiment of the video titles/ tags/ description to understand the emotional tone or sentiment expressed in the video titles. This can help categorize videos as positive, negative, or neutral.

Problem significance: 
1) It can be used for content moderation to identify and filter out videos with harmful, or inappropriate sentiments in their titles, tags, or descriptions.
2) Content creators can benefit from understanding the sentiment of their video titles, tags, and descriptions. It helps creators understand what types of emotional content are currently resonating with audiences.

Current State of the Art: 
I have seen some codes on internet related to this problem, and mostly there is Analysis done on this data. There is very limited research on sentiment analysis or on NLP to generate comments automatically for content creator. There are slangs in description which are hard to understand while doing sentiment analysis. Also, creating description takes lots of data, and sometimes content creator includes his own information (Instagram, email ID etc.), which is impossible to generate. So, only general description is possible using NLP. 
There are few research papers which talks about sentiment analysis on YouTube videos:
1) https://ieeexplore.ieee.org/abstract/document/9396049
2) https://link.springer.com/article/10.1007/s11042-023-16019-z

The first paper focuses only on United States region and does the sentiment analysis on English and Indonesian languages. So, the project in research paper 1 is not that much scalable. I have a large dataset of 11 countries varying in languages, and there are more languages on which sentiment analysis can be done in my project.

The second research paper is evaluated on YouTube trending video dataset of the United States for the year 2021. The given approach in the research paper 2 is only
generalized for a specific country for specific period of time. I am working on to make the YouTube sentiment analysis more generalize by including- 
1) more data
2) data of many years (from last couple of years to the data which is generated today)
3) data from 11 countries varying in languages of video titles/ tags/ comments

Proposed approach: 
I will clean the data first, do the EDA. Based on the amount of information available, I will do sentiment analysis for any one or all of the following categories: Title, Tags, Description. I will use NLP techniques, Word embeddings, RNN or LSTM models, and transformer models- BERT, DistilBERT or ChatGPT.

Data description: 
This problem is available on Kaggle with the dataset sizing more than 4 GB. There are 11 excel files (one for each country), and 184K data in each excel. There are json files associated with every excel file, which contains information for category_id feature. Data is getting updated everyday. 

Expected outcomes: 
Challenges: The data includes a category_id field, which varies between regions. So, for one country- category_id for 'games' is 1, and for another country, it is '15'. To retrieve the categories, I need to look it in the associated JSON files and map it with the data.
