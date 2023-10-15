# Microsoft Movie Analysis

**Author**: Maree Marinelis

## Overview

Microsoft, a global tech giant, are preparing to create a new movie studio and into the realm of original video content creation. As Microsoft currently lacks expertise in-house film production expertise and industry-knowledge relating to films.

Two datasets were mainly used to determine overall profitability of films, in the domestic and global markets, assessing both gross and net revenue. Aditionally, the release date for movies that indicated highest popularity have been analysed, and as has the relationship between the popularity of a film and its net revenue. According to the data, films which typically have a higher production budget, tend to have a higher total revenue. Additionally, upon analysing the release dates of each film, we can conclude that films released in December, November, July and August tend to be the most popular. This is likely due to the northern hemisphere's school holidays, as well as the end of year festive season. Lastly, the relationship between popularity and net worldwide revenue was reviewed and investigated also.

## Business Problem

Microsoft, a prominent player in the technology industry, is preparing to enter the domain of original video contentand launching a new film studio. As Microsoft currently lacks experience in this space, this endeavor will work to provide some indutry related key insights to reduce the financial risk

Additionally, as there are many established players in the movie industry, entering into the market poss a significant financial risk and may be more challenging.

To answer that question both Domestic and Foreign Sales data was analysed to see the most financially successful genres, along with the average rating given and number of votes for each type or genre of movie to see how popularity compared with financial success.

---

## Data

The data, extrapolated from various datasets, encompasses sources from The Movie Database, which encapsulate details, popularity, and ratings of various movies. The subsequent datasets in this analysis contain data related to movie budgets and gross earnings, providing a financial perspective to the cinematic overview.

---

## Methods

For my first insight, I calculated profitability using the financial data in tn.movie_budgets.csv.gz. I did this by first checking to see whether there were any null values, and if the data types were appropriate to treat as integers or float. The columns that I focused on were'domestic_gross', 'worldwide_gross' and 'production_budget'. As the name 'worldwide_gross' was ambiguous and unclear whether it contained only foreign_gross data or total gross, I subtracted domestic_gross from worldwide_gross to generate foreign_gross_est (estimated foreign gross). I then merged this dataset with another which contained financial data also and compared data to ensure that my new column 'foreign_gross_est' had similar values to foreign_gross in the other dataset.

Once I was comfortable with using this data, I calculated the 'net_worldwide_revenue' and used this as the basis for the remainder of my analysis. I largely used this figure as I believe it provided a more realistic approach to present actual potential earnings and global data to the Microsoft team. The first insight I visualised was the correlation between 'net_worldwide_revenue' and 'production_budget_num' to determine whether a higher production budget was linked to a higher net revenue.

Secondly, I reviewed the release dates of films as well as their mean popularity to determine if there was any significance with between releasing movies at specific months of the year, in case this could be an indicator into what could make a film successful.

Note: I tried to avoid making changes to the columns themselves and created new columns with num after I'd made changes to them, including converting them to integer or float.

After conducting a profitability analysis as well as investigated the most popular time to relase films, I joined another dataset to it on 'title' and 'movie' to analyse whether the popularity of a film equated to a higher overall worldwide net revenue. I conducted another correlation analysis and presented the data with a line of best fit to properly illustrate the relationship.

---

## Results

A moderate positive correlation indicates that films with higher production budgets often realize higher net worldwide revenues. This could suggest that larger investments in production might be associated with higher returns globally, although it’s important to note that a higher budget does not guarantee higher revenue. Additionally, as net_domestic_revenue is made up of multiple inputs ('worldwide_gross', 'domestic_gross', 'production_budget'), any change in these variable could impact the relationship.

Movies released in December, July, and August tend to be more popular, indicating that releasing films during holiday seasons or summer might attract larger audiences. Microsoft may benefit from releasing movies during months that historically show high popularity (e.g., December or summer months in the northern hemisphere) to maximize audience turnout.

Lastly, the correlation between the 'vote_average', 'popularity' and 'net_worldwide_revenue' had any relationship with each other. Overall, this shows that there is a moderate-strong positive correlation between the popularity of a film and it's net worldwide revenue, which is what was visualised. This shows us that a film is likely to be more financially viable if it is also popular.

Popularity of a film can be generated through a myriad of ways including marketing, a star cast or director and understanding audience segmentation. The vote_average however (which was not visualised in the presentation) does not correlate with popularity nor does it correlate with net worldwide revenue. This may be because it only includes one type of data (votes), and popularity may be based off multiple factors. Since vote_averages (which may be from critics only) does not strongly correlate with financial metrics, it might be beneficial to diversify production portfolios to include both critically-oriented and mass-appeal projects.

To improve confidence in the results next time I would:-

Additional Financial Review:
Budget Segmentation: Group movies into different budget segments (low, medium, high) and analyze which segment tends to generate the highest net revenue. This can help in risk management by understanding the potential returns in each budget category.
Seasonality & Revenue: Link the popularity of releasing movies during the more popular months with profitability metrics like revenue.
Clearer breakdown of domestic, foreign and worldwide gross and net figures.

Genre analysis: Link 'genres' with financials to provided recommendations for which genres were more profitable.
Genre Popularity: Investigate if certain genres tend to be more popular during specific months or seasons. For example, romance movies might be more popular around February (Valentine's Day).

Director Analysis: Review which directors generated the most profitable, popular and highly-acclaimed films to suggest Microsoft collaborate with them.
Competitor Analysis: Analyse the performance of other studios' films (Warner Brother, Sony, etc), their genre preferences, and release strategies could uncover gaps in the market that Microsoft could take advantage of.

The analysis may not fully address other vital aspects like genre-specific trends, directorial impact, and competitor strategies which significantly influence movie success.

## Conclusions

This analysis leads to three recommendations regarding types of movies that are successful:-

Higher production budget is positively correlated with higher net revenue globally
Release movies towards the end of the year in July, August and December.
Films that are more popular tend to generate higher net revenue worldwide.

Profitability, popularity, and strategic release timing may assist Microsoft in entering in to the market by understanding how Microsoft can reach audiences and carve out a niche in a competitive market.

---

## Repository Structure

Describe the structure of your repository and its contents, for example:

```
├── README.md                           <- The top-level README for reviewers of this project
├── Movie_Analysis-1.ipynb              <- Narrative documentation of analysis in Jupyter notebook
├── Maree Marinelis_Project_Presentation Microsoft.pdf       <- PDF version of project presentation
├── zippedData                          <- Both sourced externally and generated from code
├── Movie_Analysis-1-PDF                <- PDF Version
└── Draft_Analysis-1                    <- Code generated in my first few drafts and exploration of this project

```
