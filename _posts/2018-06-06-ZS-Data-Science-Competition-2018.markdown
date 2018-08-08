---
layout:     post
title:      ZS Data Science Challenge 2018
date:       2018-08-08 12:34:56
summary:    All India competition on data science
categories: competition
---
I had just reached campus from home. I have been in 3 different cities in the last 6 days and I just wanted to sleep. A friend of mine told me about a forth-coming competition for final year students and how cool it was. To be honest, I wasn't inclined to go for it. Later, when I was scrolling through our campus' online notice board, I found the link to the competition, it hit my curiosity spot. When I went through their page, I decided to take it.

The problem statement was interestingly different (though I had seen only one competition before this ;-)). We were given following features-
>S_No of a weekly sale
>year
>Month
>week of sale Data
>Product_ID
>Country of sale
>Sale value that week

Apart from that, expenses on a product and country was given in a separate file. We were also given data of Holidays in various countries. The weird part was that expense data, and test data was monthwise while the train data was weekwise.

It was immediately obvious that the whole data will have to be in month form. I converted the data and made it consistent. Then I conjoined the expense data. It was important to maintain consistency as well as to fill correct values in correct rows on merging and slicing.

The final train data had only 3 columns-
>Horizon (indicating cumulative month)
>expense
>sale value

However, I had 11 of these train datasets and 11 test datasets. Finally, it was also needed to concatenate all 11 test datasets into one and submit only that. Phew, it was a mind-wrenching task.

On each dataset, I used ensemble of different algorithms such as XGBoost, ARIMA and even Linear Regression. After a bit of parameter tuning, I reached at my first submission. The competition used mean squared error as evaluation criteria. My rank on the public leaderboard was 71. I was disheartened. However, I knew that if I overfitted the data, noise will lead to a high bias and my score will reduce. Instead of what others were doing, I decided to draw more statistical inferences for each dataset and finally arrived at an optimum submission. My rank was still around 50. I had lost all hope by now, and submitted with half heart. Only if I had more confidence, I would have worked more on what I was doing.

After few days, my friend came to my room with a picture opened in his phone. My rank on final leaderboard was 12. I had made it to the top 40. This meant I was going to ZS Pune office for the final round and interview. In fact 7 of us from IIT Roorkee were going to Pune.

Few days later, we reached Dehradun Airport and boarded the flight to Pune. Our stay was arranged at Hotel Hyatt. It was my first stay in a 5 star hotel and I must say I was quite intrigued by their hospitality. The next day, we reached World Trade Center, where ZS Pune office is situated. It is a marvelous building. We checked in, and were given a new problem statement after an introductory session. This problem statement was even more difficult. It was a multiclass classification problem. Quite similar to a Netflix Recommendation problem. After banging our heads for 10 hours straight, we made the final submission. I was quite confident with my approach. Also, after reaching our hotel rooms, we were expected to make a presentation of our approach. I inserted a few good looking graphs and went to sleep. It had been a long day.

The next day, we had an individual interview with senior officers. My interviewer was a stern man. Previous interviewee had told me that he is being brutal. I remembered lord Hanumana, and went in. I explained my approach with full confidence to him. To my surprise, he was not being brutal at all. In fact, he was listening to me very patiently and asking questions when I wasn't clear. At last, he asked me a few questions about my resume and set me off with a big smile. I assumed this could either mean that he was so sure that he didn't want me in, or he did really like me. Anyways, right now, all of us were very tired and just wanted to go back to our places. When the result came out, I was not in the top 3. But I didn't care, I just wanted to sleep. After a long flight, we reached back.

Just yesterday, another friend came running to my room. We were awarded Pre placement interviews in ZS Associates. It was a huge thing for me. Looking forward to interacting with them again.

Signing off.
