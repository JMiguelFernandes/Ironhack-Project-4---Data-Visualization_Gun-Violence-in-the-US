# Ironhack-Project-4---Data-Visualization_Gun-Violence-in-the-US  
  

  
The goal of this project was to practice data visualization with Tableau using a dataset of my choice. 


### Sourcing the data

I chose a dataset from Kaggle containing information about incidents involving guns in the United States between 2013-2018 (available [here](https://www.kaggle.com/jameslko/gun-violence-data)). 

I also needed population data by state across this time period, which was available from the [US Census Bureau](http://www2.census.gov/programs-surveys/popest/datasets/2010-2019/national/totals/nst-est2019-alldata.csv?#).

I also found a third dataset with information regarding background checks for every state in this time period. However, after cleaning it, I ended up deciding against using it for the analysis in Tableau because the data is not comparable between states (due to different legislations and reporting procedures). I left it in the repo anyway, in case anybody else wants to use it. It was sourced from [here](https://github.com/BuzzFeedNews/nics-firearm-background-checks/blob/master/data).

### Preparing the data

The main dataset required some cleaning/wrangling. It included columns with information that I didn't need, which I removed, and it also included some columns that contained multiple values (info regarding several participants in an incident, or regarding several guns involved, for example). I expanded and joined those columns into dataframes that I saved as separate datasets in a tidy format for easier manipulation in Tableau. 
The code can be found in [notebook 1](https://github.com/JMiguelFernandes/Ironhack-Project-4---Data-Visualization_Gun-Violence-in-the-US/blob/master/1_Cleaning%20and%20preparing%20the%20kaggle%20dataset.ipynb).

In addition, the population dataset also contained information that I didn't need, so I trimmed it and saved it to a new csv file. 
The code can be found in [notebook 2](https://github.com/JMiguelFernandes/Ironhack-Project-4---Data-Visualization_Gun-Violence-in-the-US/blob/master/2.%20Preparing%20state%20population%20dataset.ipynb).

I also included the code used for cleaning up the background check dataset, even though I ended up not using it. It is available in [notebook 3](https://github.com/JMiguelFernandes/Ironhack-Project-4---Data-Visualization_Gun-Violence-in-the-US/blob/master/3.%20Preparing%20background%20checks%20dataset.ipynb)

### Visualization in Tableau

My visualizations can be found in Tableau Public [here](https://public.tableau.com/profile/jo.o.fernandes3414#!/vizhome/Project4-GunViolenceintheUS/Story1?publish=yes)

I included the following in my story:

1. Line graphs shoing the year-on-year and month-on-month growth of the number of incidents involving guns in the US
2. Pie charts showing the gender distribution of both the victims and the perpetrators of those incidents
3. A scatter plot showing the correlation between the state populations and the number of gun incidents
4. A treemap showing the average number of deaths per incident for each state
5. A map of the US depicting the number of incidents per 1000 inhabitants and per capita income for each state.
