# Dollywood
Thomas - tramsay-deloitte
<br>Enoch - ekwaning
<br>Krystal - krystalduong
<br>Augusth - aukoppaldeloitte

![team logo]()Format: ![Alt Text](url) 

# ***Repo Guide***

# ***Technologies Used:***
python 3.8.5 
<br>conda 4.12.0
<br>numpy 1.18.5
<br>pandas 1.1.3
<br>matplotlib 3.3.1
<br>seaborn 0.11.0
<br>scipy.stats 1.5.0
<br>statsmodel.api 0.12.0

# ***Repo Contents:***

A .gitignore file that contains certain ignore instructions in terms of certain data sources and repositories.
A Monthly Data Analysis.ipynb that contains the best months to release content based on revenue.
A Mostpopular.ipynb that contains the grossing information of the top genres in the film industry. 
A BudgetRevenue.ipynb that compares the relationship between production budgets and revenue.

# ***Description:***

Our client Computing Vision is looking to create a new movie studio. Due to their non-film backgrounds they need assistance on what types of films to create. The team was given several different sources of data sets. This was done in an effort to leverage the datasets for insights and courses of actions for the new movie studio. First, the team found insights on monthly seasonality in terms of film releases. This in turn helped influence the content produced. Second, the team found insights on the most popular genres produced from 2010 to 2018. This allowed the team to focus on the specific demands of genres expected from the audience. Lastly, the team found a diminshing correlation between worldwide gross and the production budget. This allowed the team to propose that the studio look for progressive cost cutting manuevers.

### Categorical Variables: 
<br>month, months, genre, genres, release_date, release_month, movie, title, studio

### Quantitative Variables: 
<br>gross, production_budget, domestic_gross, domestic_profit, worldwide_gross, worldwide_profit, popularity, production_budgetINT, domestic_grossINT, worldwide_grossINT


# ***Recommendation 1*** Release content during summer (May - July) and winter (November - December) holidays. 

### Data Importing
<br>Step 1 - Imported tn.movie_budgets.csv table.
### Data Cleaning
<br>step 1 - Converted the dallar values for production_budget, domestic_gross, & worldwide_gross into a float from a string.
<br>step 2 - Converted release_date column into desired date/time format.
<br>step 3 - Created a new variable called release_month and set it equal to the month in release_date.
<br>step 4 - Created a new variable called domestic_profit and set it equal to domestic_gross minus production_budget.
<br>step 5 - Created a new variable called worldwide_profit and set it equal to worldwide_gross minus production_budget.
<br>step 6 - Used grouby method to filter movies released by month in release_month
### Data Visualization
<br>Step 1 - Ploted barplot with x axis months & y axis number of movies released
<br>Graph 1 - 
<br>Analysis 1 - 
<br>Step 2 - Ploted barplot with x axis months & y axis worldwide_profit (USD)
<br>Graph 2 - 
<br>Analysis 2 - 
<br>Step 3 - Ploted barplot with x axis months & y axis domestic_profit (USD)
<br>Graph 3 - 
<br>Analysis 3 - 


# ***Recommendation 2*** - Movie release's should include science fiction, adventure and animation related genres.

### Data Importing
<br>Step 1 - Imported bom.movie_gross.csv table
<br>Step 2 - Imported tmdb.movies.csv table
<br>Step 3 - Connected to IMDB database and select all columns from movie_basics table
### Data Cleaning
##### Movie Gross Data Cleaning
<br>Step 1 - Set movie_gross table equal to bom_movie_gross
<br>Step 2 - Ignored foreign_gross column because of large amount (1350) of Null/NA values
<br>Step 3 - Made individual dataframe for each year and take the top 10 movies
##### Popularity Data Cleaning
<br>Step 1 - Created a top 10 dataframe using the tmbd.movies.popularity csv file
<br>Step 2 - Sorted values in tmdb.movies.release_date.csv by descending order
##### Genre Data Cleaning
<br>Step 1 - Found all of the different unique genres in the imdb_movie_basics.genre database
<br><!---Created a new dataframe of all genres with repeating movie as multiple genres--->
<br>Step 2 - Defined a function that isolates all the movies that are a genre 
<br>Step 3 - Created a new column with the genre name
<br>Step 4 - Emptied the genre dataframe
<br>Step 5 - Wrote for loop that created dataframe of all movies that are each genre and concatenates them together, with repeating movies 
<br>Step 6 - Selected specific columns and left joined the movie_gross and genres dataframes
<br>Step 7 - Droped null values and isolated only the needed columns
<br>Step 8 - Printed the genres that have the most domestic gross revenue over the entire time period
<br>Step 9 - Group by genre and year, used mean to control for number of movies released, could also use sum
<br>Step 10 - Created function to plot the genres and their domestic gross revenue
<br>Step 11 - Created list of top grossing genres to plot
### Data Visualization
<br>Step 1 - Ploted barplot with x axis Movie & y axis gross (in $100 million) for 2010-2018
<br>Graph 1 - 
<br>Analysis 1 -
<br>Step 2 - Ploted barplot with x axis of Movie & y axis Popularity for top 10 all time
<br>Graph 2 - 
<br>Analysis 2 -
<br>Step 3 - Ploted barplot with x axis of Genre & y axis Domestic Gross (USD) for average gross by genre from 2010 - 2018
<br>Graph 3 - 
<br>Analysis 3 -
<br>Step 4 - created call function for top genres and plot lineplot with x axis of Year & y axis Average Domestic Gross Revenue (USD) for average domestic gross revenue of top 10 movie genres from 2010-2018
<br>Graph 4 - 
<br>Analysis 4 -
<br>Step 5 - Imported from youtube?; checked the top genre combinations, ploted bar plot of top movies with x axis of Genre and y axis of Count
<br>Graph 5 - 
<br>Analysis 5 -

# ***Recommendation 3*** - Understand that bloated production budgets do not guarantee maximum revenue.

### Data Importing
<br>Step 1 - Imported tn.movie_budgets.csv file.
### Data Cleaning
<br>Step 1 - Created a production column int column
<br>Step 2 - Created a domestic gross int column
<br>Step 3 - Created a worldwide gross int column
<br>Step 4 - Removed all movies with a worldwide gross of 0 or less.
<br>Step 5 - Imported bom.movie_gross.csv file and inner join with movie_budgets table. call new dataframe movie_studio_budget.
<br>Step 6 - Made release date datetime
<br>Step 7 - Dropped null rows in movie_studio_budget
<br>Step 8 - Checked to see unique studio in movie_studio_budget.studio
<br>Step 9 - Made new variable called studios to edit studio names
<br>Step 10 - Renamed studios that are the same with different names in the dataset
<br>Step 11 - Merged the studio variable back into the studios dataframe
### Data Visualization
<br>Step 1 - Ploted scatterplot of x-axis production budget & y-axis Worldwide Gross (USD) to show diminishing return on production budget.
<br>Graph 1 - 
<br>Analysis 1 -
<br>Step 2 - Ploted displot of x-axis Production Budget (USD) & y-axis Density to show production budget distribution trends.
<br>Graph 2 - 
<br>Analysis 2 -
<br>Step 3 - Ploted displot of x-axis Worldwide Gross (USD) & y-axis Density to show worldwide gross distribution trends.
<br>Graph 3 - 
<br>Analysis 3 -
##### Statistical Analysis
<br>Step 1 - Tested for normality of production_budgetINT
<br>Step 2 - Tested for normality of worldwide_grossINT
<br>Step 3 - Performed OLS Regression analysis on worldwide_grossINT ~ production_budgetINT 


## Top Studio Budgets
### Data Imported
<br>Step 1 - Displayed first 5 records of movie_studio_budget dataframe.
### Data Cleaning
<br>Step 1 - Sorted release_date by year
<br>Step 2 - Grouped 'studio' by mean values for production_budgetINT' & worldwide_grossINT
<br>Step 3 - Sorted worldwide_grossINT by top 10 records.
### Data Visualization
<br>Step 1 - Ploted barplot of x-axis Studio & y-axis Average Worldwide Gross (USD) for top studio's average revenue vs budget per movie from 1984 - 2018.
<br>Graph 1 - 
<br>Analysis 1 -
<br>Data Clean Step 4 - Grouped 'studio' by sum values for production_budgetINT & worldwide_grossINT
<br>Step 2 - Ploted barplot of x-axis Studio & y-axis Total Worldwide Gross (USD) for top studio's total revenue vs budget per movie from 1984 - 2018.
<br>Graph 2 - 
<br>Analysis 2 -


