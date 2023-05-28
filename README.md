# Phase 1 Project - Microsoft Studios Movie Project
#
## 1.Introduction
The global film industry revenue is estimated to be $101.22 billion in 2021.The industry comprises the technological and commercial institutions of filmmaking, i.e., film production companies, film studios, cinematography, animation, film production, screenwriting, pre-production, post production, film festivals, distribution, and actors.

Microsoft Corporation is an American multinational technology corporation headquartered in Redmond, Washington. Microsoft's best-known software products are the Windows line of operating systems, the Microsoft Office suite, and the Internet Explorer and Edge web browsers. Its flagship hardware products are the Xbox video game consoles and the Microsoft Surface lineup of touchscreen personal computers.

Ranked No. 14 in the 2022 Fortune 500 rankings of the largest United States corporations by total revenue, the corporation wishes to enter into the Movie buisness.

## 2.Business Understanding
### 2.1. Problem Statment
Microsoft corporation, is looking to set up a movie studio to create original video content, having no proir experience in the field their is need to reseach the current trends in the industry. In order to make the necessary decisions resulting in the most profitable movies, there is need to look into data from movie review sites, analyse the data and come up with the recommendations that will lead to this outcome.

From the datasets provided, answers to the following questions can be sought:

1. What are the most popular genres?
2. Movie returns in both Domestic and Worldwide markets.
3. What are the most popular film ratings?

### 2.2 Objectives
Explore the datasets to answer the Problem Statment .
Provide conclusions and recommendations from the outcomes of the analyses.

## 3. Data Understanding
The datasets provided for this analysis were collected from different movie review sites.
The datasets include:

1. bom.movie_gross [Box Office Mojo]
2. tmdb.movies [IMDB]
3. rt.movie_info [Rotten Tomatoes]
4. rt.reviews [Rotten Tomatoes]
5. tn.movie_budgets [The Numbers]

Their features are as follows:

#### 3.1. From Box Office Mojo
1. title - Name of the movie.
2. studio - The studio that produced it.
3. domestic_gross - The amount of gross earnings from its mother country.
4. foreign_gross - The amount of gross earnings from elsewhere around the world.
5. year - The year it was released.

#### 3.2. From IMDB Movies:
1. genre_ids - id for each genre of the Movie.
2. id - Unique id for each movie.
3. original_language - The original language of film.
4. popularity - The popularity of the movie in millions.
5. release_date - The date the Movie was released.
6. title - The average rating out of 10.
7. vote_average - Average Number of votes to rate the movie out of 10.
8. vote_count - Number of pepole who to rate the movie.

#### 3.3. Rotten Tomatoes Movies Information:
1. id - Unique id for each movie.
2. synopsis - A brief note on the premise of the movie.
3. rating - rate of motion picture's suitability for certain audiences based on its content.

       R :- Restricted: Under 17 requires accompanying parent or adult guardian

       PG-13 :- Some material may be inappropriate for children under 13

       PG :- Some material may not be suitable for children

       G :- All ages admitted

       NR :- Not rated

4. genre - A movie's category based on the plot.
5. director - The movie's director.
6. writer - The movie's writer.
7. theater_date - The date the movie was released in theaters.
8. dvd_date - The date the movie was released in dvd format.
9. currency - - currency used.
10. Box office - The studio returns.
11. runtime - The total length of the movie.
12. studio - The studio involved in the movie production.

#### 3.4. Rotten Tomatoes Review Information:
1. review - A review on the movie by a user.
2. rating - How a user rates the movie.
3. fresh - Rotten Tomatoes rating system,[Flesh-they liked it, rotten- the did not like it]
4. critic - Name of the person leaving the review.
5. top_critic -
6. publisher - The publisher of the review.
7. date - The date the review was written.

#### 3.5. From The Numbers:
1. id - Unique id for each movie.
2. release_date - The date the Movie was released.
3. movie - The movie name.
4. production_budget - amount of money used in the movie production.
5. domestic_gross - Dometic returns of the production.
6. worldwide_gross - worldwide returns of the production.

## 4. Data Preparation
1. import the Libraries
2. Loading the Datasets
3. Exploring the Dataframes
4. Clean the data by dealing with:
    - Duplicated rows
    - Missing values
    - Invalid data
    - Outliers
    - Merges
    - Droping unnecessary columns

## 5.Exploratory Analysis
### Question 1. What are the most popular genres?
Plot a bar graph with genres and averagerating as the variables

plt.data = imdb

x = imdb['genre']

y = imdb['averagerating'] 

![Average Rating of Different Movie Genres according to IMDB](https://github.com/Collinskanyiri/DSC-Phase-1-project/assets/86715443/809266e7-1d87-4ee5-9431-7e37cea3c22f)


### Question 2. What are the most popular film ratings?
Plot a bar graph with ratings and Number of Movies as the variables

title = 'Film Ratings'

y = 'rt_ratings.fresh count'

x = 'Rating'

![Film Ratings](https://github.com/Collinskanyiri/DSC-Phase-1-project/blob/master/img/Film%20Ratings.png?raw=true)
### Question 3. Movie returns in both Domestic and Worldwide markets.
plotting a scatter plot

title = 'Relationship between Domestic and Worldwide Gross Earnings'

y = 'tn_movie_budgets_top.worldwide_gross'

x = 'tn_movie_budgets_top.domestic_gross'

![Relationship between Domestic and Worldwide Gross Earnings](https://github.com/Collinskanyiri/DSC-Phase-1-project/blob/master/img/Relationship%20between%20Domestic%20and%20Worldwide%20Gross%20Earnings.png?raw=true)


## 6. Conclusion
The analysis done has been able to provide answers that can lead to actionable recommendations. 

From the findings, the most popular genres have been determined to be History and Documentary , while adult and Game-Shows are least popular. 

It has also been seen that a movie that does well domestically is likely to do well internationally. 

In addition to that, R rated movies have been found to be most popular.


## 7. Recommendations
The Microsoft Corporation should base their Production company to produce R-Rated, History and Documentary productions as they are the most popular and highest rated in the markets.
The should market their product in both domestic and wolrdwide markets to archive maximum profits from a single production.
