Dollywood
Thomas - tramsay-deloitte  
Enoch - ekwaning  
Krystal - krystalduong  
Augusth - aukoppaldeloitte  

![welcome](https://media.giphy.com/media/l0MYGb1LuZ3n7dRnO/giphy.gif) 

***Repo Guide***

***Technologies Used:***


python 3.8.5  
conda 4.12.0  
numpy 1.18.5  
pandas 1.1.3  
matplotlib 3.3.1  
seaborn 0.11.0  
scipy.stats 1.5.0  
statsmodel.api 0.12.0  

***Repo Contents:***
<br> A Individual Notebooks folder with data explorationa and visualization techniques done by the team.
<br> A Reccomendation Notebooks folder with specific data exploration and visualization techniques for each recommendation.
<br> .gitignore file that contains certain ignore instructions in terms of certain data sources and repositories.
<br> A Capstone Final.pdf folder that has the teams final presentation in pdf format.
<br> A final notebook that has all of the data exploration and visualization that pertains to the final deliverables for this project.
<br> A final notebook.pdf of the final notebook.
<br> A README.md file that explains the contents of this repo. 

***Description:***


Our client Computing Vision is looking to create a new movie studio. Due to their non-film backgrounds they need assistance on what types of films to create. The team was given several different sources of data sets. This was done in an effort to leverage the datasets for insights and courses of actions for the new movie studio. First, the team found insights on the most popular genres produced from 2010 to 2018. This allowed the team to focus on the specific demands of genres expected from the audience. Second, the team found insights on monthly seasonality in terms of film releases. This in turn helped influence the content produced.  Lastly, the team found a diminshing correlation between worldwide gross and the production budget. This allowed the team to propose that the studio look for progressive cost cutting manuevers.

***Categorical Variables:*** 
<br> month, months, genre, genres, release_date, release_month, movie, title, studio

***Quantitative Variables:*** 
<br> gross, production_budget, domestic_gross, domestic_profit, worldwide_gross, worldwide_profit, popularity, production_budgetINT, domestic_grossINT, worldwide_grossINT

![recommendation](https://media.giphy.com/media/sdjzyK11BKMRK5fw3q/giphy.gif)

***Data Importing:***
<br>Step 1 - Imported tables movie_basics & movie_ratings from im.db file.
<br>Step 2 - Imported the csv file from Box Office Mojo with movie_gross info. 
<br>Step 3 - Imported the csv file from TMDB with movie_gross info.
<br>Step 4 - Imported the csv file from The Numbers with movie_budgets info.
<br>Step 5 - Imported the tsv file from Rotten Tomatoes with movie_gross info. 

***Conclusion (Reccomendations):***
<br>In this notebook, we explored three topics of focus to help Computing Vision break into the movie industry. These topics related to which type of movie to release, when to release it, and how much should be spent on each movie. Our first recommendation is to produce movies that superhero movies; of the Sci-Fi, Action, or Adventure genres; and are part of a larger franchise that fans can follow. Our second recommendation is to release the movie in the winter or summer time to optimize profits from "summer blockbusters" and award ceremonies. Lastly, our third recommendation is to spend more than 43,000,000 USD in production on a movie, but no more than 200,000,000 USD as trends suggest possible diminishing returns.

![bye](https://media.giphy.com/media/m9eG1qVjvN56H0MXt8/giphy.gif) 
