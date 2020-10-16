# Board_games_EDA_project
**Description**: An EDA project in which a board game database is analysed to investigate what factors drive sales for these products.

# Code and Resources Used

**Python Version**: 3.7
**Packages**: pandas, numpy, datetime, scipy, sklearn, matplotlib, seaborn, BeautifulSoup, requests, re.

# 1. Data cleaning and feature engineering:

* Handled **Nan values**:
  * Columns with more than **40 %** nan values were directly **removed**.
  * For categorical variables nan values were filled with **"Unknown"**
  * For numerical variables nans were filled with the **median**, after visualy recognizing the presence of **outliers** using boxplots.
  
* Outliers were removed using the **Z-score < 3** approach.

* **Feature-engineering**:
  * A single **"num_players_recommended"** column was created by combining several other columns.
  * Using the "mechanic" column, all boardgames were classified in different group types and a new column **"type of game"** was created.
  * The "owned" and "yearpublished" columns were used to create a column **"owned by year"** which contained the information of how many new users owned each game per year.
  * Using the "averageweight" column (float) a **"weight_level"** column was created by simply changins his data type to int to round the values.
  * Finally, columns **"expansion"** and **"language_dependence"** were converted into boolean (0, 1) columns.
  
 # 2. Exploratory Data Analyses:
 I aimed to aswer the following questions:
 * What games people buy/own the most?
 
  <img src="figures/type_of_game_owners.png" width="600"/> 
  
  * What type of games most succesfull companies sell?
  
  <img src="figures/pie_chart_games.png" width="500"/> 
  
  *  What game difficulty people prefer to buy/own?
  
  <img src="figures/game_level.png" width="400"/> 
  
  * What games have been sold most times?
  
   <img src="figures/yearpub_gamessold.png" width="600"/> 
  
  
