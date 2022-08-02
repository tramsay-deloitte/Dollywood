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

A .gitignore file that contains certain ignore instructions in terms of certain data sources and repositories.
A Monthly Data Analysis.ipynb that contains the best months to release content based on revenue.
A Mostpopular.ipynb that contains the grossing information of the top genres in the film industry. 
A BudgetRevenue.ipynb that compares the relationship between production budgets and revenue.

# ***Description:***

Our client Computing Vision is looking to create a new movie studio. Due to their non-film
backgrounds they need assistance on what types of films to create. The team was given 
several different sources of data sets. This was done in an effort to leverage the datasets for insights and courses
of actions for the new movie studio. First, the team found insights on monthly seasonality
in terms of film releases. This in turn helped influence the content produced. Second, the 
team found insights on the most popular genres produced from 2010 to 2018. This allowed the
team to focus on the specific demands of genres expected from the audience. Lastly, the 
team found a diminshing correlation between worldwide gross and the production budget. This 
allowed the team to propose that the studio look for progressive cost cutting manuevers.

### Categorical Variables: month, months, genre, genres, release_date, release_month, movie, title, studio

### Quantitative Variables: gross, production_budget, domestic_gross, domestic_profit, worldwide_gross, worldwide_profit, popularity, production_budgetINT, domestic_grossINT, worldwide_grossINT


![recommendation](https://media.giphy.com/media/sdjzyK11BKMRK5fw3q/giphy.gif)

# ***Recommendation 1*** Release content during summer (May - July) and winter (November - December) holidays. 

### Data Importing
Step 1 - Imported tn.movie_budgets.csv table.
### Data Cleaning
step 1 - Converted the dallar values for production_budget, domestic_gross, & worldwide_gross into a float from a string.
step 2 - Converted release_date column into desired date/time format.
step 3 - Created a new variable called release_month and set it equal to the month in release_date.
step 4 - Created a new variable called domestic_profit and set it equal to domestic_gross minus production_budget.
step 5 - Created a new variable called worldwide_profit and set it equal to worldwide_gross minus production_budget.
step 6 - Used grouby method to filter movies released by month in release_month
### Data Visualization
Step 1 - Ploted barplot with x axis months & y axis number of movies released
Graph 1 - 
Anlysis 1 - 
Step 2 - Ploted barplot with x axis months & y axis worldwide_profit (USD)
Graph 2 - 
Anlysis 2 - 
Step 3 - Ploted barplot with x axis months & y axis domestic_profit (USD)
Graph 3 - 
Anlysis 3 - 


# ***Recommendation 2*** - Movie release's should include science fiction, adventure and animation related genres.

### Data Importing
Step 1 - Imported bom.movie_gross.csv table
Step 2 - Imported tmdb.movies.csv table
Step 3 - Connected to IMDB database and select all columns from movie_basics table
### Data Cleaning
##### Movie Gross Data Cleaning
Step 1 - Set movie_gross table equal to bom_movie_gross
Step 2 - Ignored foreign_gross column because of large amount (1350) of Null/NA values
Step 3 - Made individual dataframe for each year and take the top 10 movies
##### Popularity Data Cleaning
Step 1 - Created a top 10 dataframe using the tmbd.movies.popularity csv file
Step 2 - Sorted values in tmdb.movies.release_date.csv by descending order
##### Genre Data Cleaning
Step 1 - Found all of the different unique genres in the imdb_movie_basics.genre database
<!---Created a new dataframe of all genres with repeating movie as multiple genres--->
Step 2 - Defined a function that isolates all the movies that are a genre 
Step 3 - Created a new column with the genre name
Step 4 - Emptied the genre dataframe
Step 5 - Wrote for loop that created dataframe of all movies that are each genre and concatenates them together, with repeating movies 
Step 6 - Selected specific columns and left joined the movie_gross and genres dataframes
Step 7 - Droped null values and isolated only the needed columns
Step 8 - Printed the genres that have the most domestic gross revenue over the entire time period
Step 9 - Group by genre and year, used mean to control for number of movies released, could also use sum
Step 10 - Created function to plot the genres and their domestic gross revenue
Step 11 - Created list of top grossing genres to plot
### Data Visualization
Step 1 - Ploted barplot with x axis Movie & y axis gross (in $100 million) for 2010-2018
Graph 1 - 
Anlysis 1 -
Step 2 - Ploted barplot with x axis of Movie & y axis Popularity for top 10 all time
Graph 2 - 
Anlysis 2 -
Step 3 - Ploted barplot with x axis of Genre & y axis Domestic Gross (USD) for average gross by genre from 2010 - 2018
Graph 3 - 
Anlysis 3 -
Step 4 - created call function for top genres and plot lineplot with x axis of Year & y axis Average Domestic Gross Revenue (USD) for average domestic gross revenue of top 10 movie genres from 2010-2018
Graph 4 - 
Anlysis 4 -
Step 5 - Imported from youtube?; checked the top genre combinations, ploted bar plot of top movies with x axis of Genre and y axis of Count
Graph 5 - 
Anlysis 5 -

# ***Recommendation 3*** - Understand that bloated production budgets do not guarantee maximum revenue.

### Data Importing
Step 1 - Imported tn.movie_budgets.csv file.
### Data Cleaning
Step 1 - Created a production column int column
Step 2 - Created a domestic gross int column
Step 3 - Created a worldwide gross int column
Step 4 - Removed all movies with a worldwide gross of 0 or less.
Step 5 - Imported bom.movie_gross.csv file and inner join with movie_budgets table. call new dataframe movie_studio_budget.
Step 6 - Made release date datetime
Step 7 - Dropped null rows in movie_studio_budget
Step 8 - Checked to see unique studio in movie_studio_budget.studio
Step 9 - Made new variable called studios to edit studio names
Step 10 - Renamed studios that are the same with different names in the dataset
Step 11 - Merged the studio variable back into the studios dataframe
### Data Visualization
Step 1 - Ploted scatterplot of x-axis production budget & y-axis Worldwide Gross (USD) to show diminishing return on production budget.
Graph 1 - 
Anlysis 1 -
Step 2 - Ploted displot of x-axis Production Budget (USD) & y-axis Density to show production budget distribution trends.
Graph 2 - 
Anlysis 2 -
Step 3 - Ploted displot of x-axis Worldwide Gross (USD) & y-axis Density to show worldwide gross distribution trends.
Graph 3 - 
Anlysis 3 -
##### Statistical Analysis
Step 1 - Tested for normality of production_budgetINT
Step 2 - Tested for normality of worldwide_grossINT
Step 3 - Performed OLS Regression analysis on worldwide_grossINT ~ production_budgetINT 


## Top Studio Budgets
### Data Imported
Step 1 - Displayed first 5 records of movie_studio_budget dataframe.
### Data Cleaning
Step 1 - Sorted release_date by year
Step 2 - Grouped 'studio' by mean values for production_budgetINT' & worldwide_grossINT
Step 3 - Sorted worldwide_grossINT by top 10 records.
### Data Visualization
Step 1 - Ploted barplot of x-axis Studio & y-axis Average Worldwide Gross (USD) for top studio's average revenue vs budget per movie from 1984 - 2018.
Graph 1 - 
Anlysis 1 -
Data Clean Step 4 - Grouped 'studio' by sum values for production_budgetINT & worldwide_grossINT
Step 2 - Ploted barplot of x-axis Studio & y-axis Total Worldwide Gross (USD) for top studio's total revenue vs budget per movie from 1984 - 2018.
Graph 2 - 
Anlysis 2 -

![bye](https://media.giphy.com/media/m9eG1qVjvN56H0MXt8/giphy.gif) 
