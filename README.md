***Genres & Sales***

**Dataset Description**
This dataset is download from Kaggle, the link to the dataset: https://www.kaggle.com/datasets/ulrikthygepedersen/video-games-sales. This dataset contain the number of units sold (Main region sales and global sales, measurement unit is million), revenue generated, and other key metrics, such as game publishers, platforms, release year, ect.

**Data Cleaning:**
The dataset is organized with a high level of cleanliness. To ensure its integrity, it's necessary to address unknown values and eliminate duplicates. The primary emphasis of data collection spans from 1980 to 2020, the dataset has fewer games post-2016. To maintain the consistency of our analysis, I have opted to exclude data recorded after 2016.

**Research Question:**
What is the relationship between regional and global game sales, and how do genres impact on global sales?

Relationship between regional sales and global sales:
To answer this question, the first thing is to have an overview of global sales and sales in different regions. I have created a bar plot to visualize this situation. From here, we can notice that North America is the main contributor to the global game market, followed by Europe. Japan is the third-largest market, but it has different popular game trends compared to the first two regions. Then, I have created a heatmap to test the correlation and validate the interpretation. Atfer that, I have done literature review to find the reason why have this phenomenon. 
The three primary video game markets consist of economically developed regions, enabling a significant portion of the population to afford gaming consoles, PCs, and video games, thereby contributing to robust sales. Notably, both North America and many European countries share English as a dominant language and possess similar cultural backgrounds. This shared language facilitates the distribution of games with minimal localization efforts. Furthermore, the cultural similarities between these regions lead to shared preferences for specific genres, gaming platforms, gameplay styles, and storytelling themes.In contrast, Japanese video games often incorporate cultural elements and storytelling styles more tailored to a Japanese audience. Language differences serve as a potential barrier, as Japanese players may prefer game versions and platforms in their native language, influencing the correlation between the Japanese video game market and other regions.

How different genre influence the global sales:
To address this question, I created a bar plot to identify which genre of games had a significant influence on global sales during this time span. By comparing the total game count, total game sales, and average game sales, I inferred that action games have been popular in the recent two decades. However, the genre with the highest sales is platform games. To understand the reasons behind this, I drew a line plot to trace the development of these two types of games in this time frame. Before 2000, platform game sales were higher than action games. The main reason for this was Nintendo's release of a series of successful platform games, such as Super Mario Bros, which attracted a large number of loyal fans. The easy mechanics made it accessible to players of all ages. After 2000, with the advancement of technology and the introduction of 3D graphics, there was a shift towards more immersive action games that incorporated cinematic storytelling elements, engaging players in compelling narratives. However, the proliferation of available games led to a saturated market with intense competition. In such a competitive landscape, individual games faced challenges in standing out and achieving high sales figures. Nevertheless, after 2000, the most popular game genre is action.

**Significance Test**
I conducted a Kruskal-Wallis Test to assess the impact of game genre on global game sales and investigated the effect size. The Kruskal-Wallis test is a non-parametric statistical method designed for comparing differences among three or more groups, particularly in situations where the data deviates from a normal distribution or demonstrates variance heterogeneity. This test is applied to determine whether significant differences exist among different groups. In my analysis, I utilized sales figures from different game genres and global sales. The results indicated a significant impact of game genre on global sales, with an effect size of 0.033.

**Future work:**
In future work, I aim to precisely determine the effect size of various game genres on global sales. However, this aspect remains unfinished at the moment. Challenges encountered include the non-normal distribution of my dataset and the unequal row counts between game genre sales and global sales, rendering the application of the Spearman correlation test unfeasible. Despite attempts with alternative tests, none have proven successful thus far. Further exploration and refinement of methodologies will be crucial to overcoming these challenges and obtaining a comprehensive understanding of the effect sizes associated with different game genres on global sales.

**Limitations**
The dataset lacks comprehensive documentation from its author, leaving uncertainty regarding how game genres were determined. The absence of clarity raises questions about potential genre overlaps, such as between action and adventure games.
The dataset's temporal scope spans 1980-2016, presenting a limitation in reflecting recent developments. Given the rapidly evolving nature of the gaming industry, the dataset may not capture the latest trends and changes in recent years.
Acknowledging a limited proficiency in data science, the analysis strives for depth but may be constrained by a shallower understanding. Recognizing this limitation, continuous improvement is anticipated in future analyses.


***Genres & Platforms***

**Dataset Description**
This dataset is download from Kaggle, the link to the dataset: https://www.kaggle.com/datasets/matheusfonsecachaves/popular-video-games. This dataset contain release_date,platforms, genres, and other key metrics, such as developers, rating, reviews, wishlists, ect. This is a relatively new dataset. It includes the video games from 1970 - 2023. 

**Data Cleaning:**
The dataset is organized with a high level of cleanliness. To ensure its integrity, it's necessary to address unknown values and eliminate duplicates. To 
improve completeness and visualisation, we selected the data from 1980 to 2022 in it. Some of the columns’ type in the dataset are ‘list’. During 
analysis, the lists needed to be split into multiple lines of ‘str’ type and eliminate extra punctuation.

**Research Question:**
The trend of genres and platforms over years. What is the relationship between them?

Platforms Trend:
The evolution of the Windows PC is very obvious. It emerged around 1988 and grew rapidly. In 1997, it entered a steady development period. In 2011, it grew faster again with a sharp increase. The second platform which shows very fast grow speed is Nintendo Switch. It started around 2012, and run very fast to reach its peak around 2017. Now the second most influential platform
Mac was the second largest platform between 2013 and 2017, but has since declined rapidly. I assume this is due to the fact that the Mac's user profile is towards professional use and the users are mainly laptops. Laptops are characterized by being thin and light, which doesn't quite match the computer configuration requirements for big games. This led to a lot of people trying to make games on Mac systems during the rise of the Mac. However, due to the mismatch between the orientation as well as the system, it gradually declined, leading to a relatively short boom period for Mac games.

Genres Trend:
Indie and adventure are the two categories that currently hold the most market share. Adventure has a distinct development since 1995. Both of AVG and Indie has a sharp increase around 2012. The third important genre is RPG, who has held the position of the third most important genre since 2012.

Relationship between platform and genre:
We can see that PC games has a very similar trend to Indie and adventure games. So is there an interaction between them? To find out it, I started with a heat map, and with the correlation coefficients we can see that PC does have a higher correlation for Indie and AVG than any other platform. And then, I divided the whole period into three time periods according to the three important periods of PC development history, and observed the development trend of PC games and Indie and AVG in different periods. In order to avoid the bias caused by the different total number of games in different years, I uniformly used the ratio of the number of games in each category in each year, as the Y-axis. From the box plot, it can be seen that in 1988-1996, the percentage of games for PC is less than AVG, and Indie doesn't even appear. But within 1997-2010, PC's share has surpassed AVG's, while AVG's have risen slightly and Indie has started to appear. In 2011-2022, PC and Indie show significant growth, with the median share of PC reaching 77%, the median share of Indie even approaching 50%, and AVG also increasing significantly. From the graph we can see that the development of PC games does have an impact on Indie and AVG, and it seems to have a greater impact after 2011.

**Significance Test**
Since the distribution of genres and platforms' data is not normal diatribution, I chose the Spearman correlation. Spearman does not require that the data distribution belongs to a specific type and is valid for small sample data as well. In my analysis, I test the whole period data of AVG VS PC/NS/PS4, Indie VS PC/NS/Mac, and extract data of each pair of samples after 2011 compared to the entire period. The results indicated a significant impact of PC and NS to AVG and Indie either the whole period or after 2011. The impact of NS on Indie and AVG is significantly enhanced after 2011. However, the impact of PC for Indie is elevated after 2011, while the degree of impact for AVG decreases.Additionally, Mac's impact on Indie and PS4's impact on AVG are significantly correlated throughout the whole period, but lose correlation after 2011. 
So taking adventure games and indie games as examples, we can see that there is truly a correlation between different game platforms and game genres.But the impact is changing. In the case of adventure and indie games, although the line graph shows that PC is rising very rapidly, and there is a strong similarity to the rising trend of AVG and Indie. But the extent to which it has influenced each game genre has changed at different times.


**Future work:**
In future work, I plan to work on the reasons behind the changes in different gaming platforms and game genres and the changes in the correlation coefficients after 2011. My current guess is that it is related to hardware, software and device upgrades, as well as the business strategies of the platform providers. This will require more literature review and support from other datasets. So I plan to do this as a future research direction. And I would like to look for more data related to the evolution of hardware devices like computers, as well as game practitioners, in order to study the impact of the emergence of real computer devices and hardware and software updates, as well as the composition of game practitioners on the development of the game industry.

**Limitations**
First, the incomplete segmentation of the dataset's game genres. Cause games can be divided into more categories, Likes action, turn-based, real-time, etc. In my dataset, the author seems to combine many types into one large category. If there are more genres, the result will be more interesting.
Second, the platform data in the dataset only reflects the relationship between games released on that platform and the game genres. It cannot represent the relationship between the hardware devices and game genres.
Last, with limited capabilities in data science, there's a lot I want to do, but relatively little I can do. So in the future, there is a need to keep improving my skills.

