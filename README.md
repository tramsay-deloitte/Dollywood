# Dollywood
Thomas - tramsay-deloitte  
Enoch - ekwaning  
Krystal - krystalduong  
Augusth - aukoppaldeloitte  

![welcome](https://media.giphy.com/media/l0MYGb1LuZ3n7dRnO/giphy.gif) 

# ***Repo Guide***

# ***Technologies Used:***
python 3.8.5  
conda 4.12.0  
numpy 1.18.5  
pandas 1.1.3  
matplotlib 3.3.1  
seaborn 0.11.0  
scipy.stats 1.5.0  
statsmodel.api 0.12.0  

# ***Repo Contents:***

<br> A Individual Notebooks folder with data explorationa and visualization techniques done by the team.
<br> A Reccomendation Notebooks folder with specific data exploration and visualization techniques for each recommendation.
<br> .gitignore file that contains certain ignore instructions in terms of certain data sources and repositories.
<br> A Capstone Final.pdf folder that has the teams final presentation in pdf format.
<br> A final notebook that has all of the data exploration and visualization that pertains to the final deliverables for this project.
<br> A final notebook.pdf of the final notebook.
<br> A README.md file that explains the contents of this repo. 

# ***Description:***

Our client Computing Vision is looking to create a new movie studio. Due to their non-film backgrounds they need assistance on what types of films to create. The team was given several different sources of data sets. This was done in an effort to leverage the datasets for insights and courses of actions for the new movie studio. First, the team found insights on the most popular genres produced from 2010 to 2018. This allowed the team to focus on the specific demands of genres expected from the audience. Second, the team found insights on monthly seasonality in terms of film releases. This in turn helped influence the content produced.  Lastly, the team found a diminshing correlation between worldwide gross and the production budget. This allowed the team to propose that the studio look for progressive cost cutting manuevers.

###Categorical Variables: 
<br> month, months, genre, genres, release_date, release_month, movie, title, studio

###Quantitative Variables: 
<br> gross, production_budget, domestic_gross, domestic_profit, worldwide_gross, worldwide_profit, popularity, production_budgetINT, domestic_grossINT, worldwide_grossINT

![recommendation](https://media.giphy.com/media/sdjzyK11BKMRK5fw3q/giphy.gif)

###Data Importing:
<br>Step 1 - Imported tables movie_basics & movie_ratings from im.db file.
<br>Step 2 - Imported the csv file from Box Office Mojo with movie_gross info. 
<br>Step 3 - Imported the csv file from TMDB with movie_gross info.
<br>Step 4 - Imported the csv file from The Numbers with movie_budgets info.
<br>Step 5 - Imported the tsv file from Rotten Tomatoes with movie_gross info. 

###Data Cleaning
#####Movie Gross Data Cleaning
<br>Step 1 - Scale domestic and foreing gross by a million.
<br>Step 2 - Find top 10 movie gross per year from 2010-2018.
#####Popularity Data Cleaning
<br>Step 1 - Created a top 10 dataframe using the movies column dataframe.
#####Genre Data Cleaning
<br>Step 4 - Found all of the different unique genres.
<br>Step 5 - Created a dataframe of all of the genres with repeating movies to represent movies as multiple genres.
<br>Step 6 - Defined function that isolates all the movies that are a genre, then create a new column with the genre name.
<br>Step 7 - Emptied the dataframe.
<br>Step 8 - Wrote for loop that creates dataframes of all the movies that are each genre and concatenates them together, with repeating movies.
<br>Step 9 - Selected specific columns and the join the movie_gross and genres dataframes.
<br>Step 10 - Dropped null values and isolate only the needed columns.
<br>Step 11 - Found the genres that have the most domestic gross revenue over the entire time period.
<br>Step 12 - Grouped by genre and year, used mean to control for number of movies released, could also use sum.
<br>Step 13 - Created function to plot the genres and their domestic gross revenue.
<br>Step 14 - Created list of top grossing genres to plot.
#####Monthly Analysis Data Cleaning
<br>Step 1 - Converted the dollar values for the budgets into floats.
<br>Step 2 - Scaled the budget and gross by dividing by a million.
<br>Step 3 - Made release date into datetime, then create variable called release_month.
<br>Step 4 - Created domestic and worldwide profits as the gross minus the budget.
#####Budget vs. Revenue Data Cleaning
<br>Step 1 - Created a production column int column.
<br>Step 2 - Created a domestic gross int column.
<br>Step 3 - Created a woldwide gross int column.
<br>Step 4 - Removed worldwide budgets of 0.
<br>Step 5 - Scaled by one million.
#####Top Studios' Budgets Data Cleaning 
<br>Step 1 - Inner joined two datasets.
<br>Step 2 - Made release date datetime.
<br>Step 3 - Dropped one null studio row.
<br>Step 4 - Made new variable called studio to edit studio names.
<br>Step 5 - Renamed studios that are the same with different names in the dataset.
<br>Step 6 - Merged the studio variable back into dataframe.
<br>Step 7 - Isolated top 10 studios by their average movie budget and worldwide gross, sort by worldwide gross.
<br>Step 8 - Isolated top 10 studios by their total budget and revenues.

###Data Visualization

#####Type of Movie
#######Top 10 grossing movie in each year
<br>Step 1 - Plotted top 10 Grossing movies in each year from 2010-2018.
#######Top 10 Popular
<br>Step 1 - Plotted top 10 popular movies of all time.
#######Genres and Domestic Gross
<br>Step 1 - Plotted the average gross by genre from 2010-2018.
![image](https://user-images.githubusercontent.com/108957906/182440616-0913a940-4111-48b3-ade6-fb98cfb67823.png)
<br>Step 2 - Create plot and call function to graph each of the top genres.
<br>Step 3 - Plotted the Average Domestic Gross Revenue of Top Movie Genres from 2010-2018.
![image](https://user-images.githubusercontent.com/108957906/182440713-790b93e4-3805-41af-8d21-7ace88a7fad4.png)
#Recommendation 1: According to this Data a new studio should invest in establishing an action based franchise which would connect all its movies. If possible this franchise should also be superhero based as superhero movies can do a great job at encapsulating all the top genres such as Sci-Fi, Action and Animation.

#####When to Release Movie
#######Months With Most Movie Releases from 1915-2020
<br>Step 1 - Plotted the months that have the most movie releases from 1915-2020.
#######Months with the Most Profit Worldwide
<br>Step 1 - Plotted the months with the most profit worldwide by month.
#######Months with the Most Profit Worldwide
<br>Step 1 - Plotted the months with the most profit domestically by month.
#Reccomendation 2: The large amounts of profits in the summer (May - July) and winter (November - December) indicates the schedules of audience free time dedicated to recreational activities such as watching a movie with family or friends. The movie studio would be wise to line up large project or blockbuster types of movies with these high activity months as they are more prone to being exposed to the public audience.

#####Budget
#######Budget and Revenue Statistical Analysis
<br>Step 1 - Plotted distribution of production_budget INT.
<br>Step 2 - Plotted distribution of worldwide_grossINT. 
<br>Step 3 - Tested for normality of production_budget INT. 
<br>Step 4 - Tested for normality of worldwide_grossINT.
<br>Step 5 - Plotted scatterplot of budget and revenue to show relationship between the two.
<br>Step 6 - Performed a Simple Linear Regression, regressing production budget on worldwide gross to learn more about the relationship.
#######Top Studios and their Budgets
<br>Step 1 - Plotted the Top Studio's Average Revenue vs Budget per Movie, 1984-2018.
<br>Step 2 - Plotted the Top Studio's Total Revenue vs Budget Across All Movies, 1984-2018.
#Reccomendation 3: Taking into account the typical budgets of competitors and the positive relationship between production budget and worldwide gross, that also looks to have the possibility of diminishing returns, we recommend that Computing Vision keeps their movie budgets greater than 43,000,000 USD and less than 200,000,000 USD per movie.

###Conclusion
<br>In this notebook, we explored three topics of focus to help Computing Vision break into the movie industry. These topics related to which type of movie to release, when to release it, and how much should be spent on each movie.
<br>Our first recommendation is to produce movies that superhero movies; of the Sci-Fi, Action, or Adventure genres; and are part of a larger franchise that fans can follow.
<br>Our second recommendation is to release the movie in the winter or summer time to optimize profits from "summer blockbusters" and award ceremonies.
<br>Lastly, our third recommendation is to spend more than 43,000,000 USD in production on a movie, but no more than 200,000,000 USD as trends suggest possible diminishing returns.

![bye](https://media.giphy.com/media/m9eG1qVjvN56H0MXt8/giphy.gif) 
