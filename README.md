# datacuration
Data curation repo for STAT 386

### .gitignore
Has some test files that I used to assist in webscraping and XML/HTML parsing

### GameRanks.ipynb
This notebook uses webscraping and HTML parsing to get the IDs of every game that I wanted. I collected the IDs of the top 100 games of each category, as well as the top 100 overall. I also got its rank within each category.

This resulted in 751 games recorded in my data set.

### BGGData.ipynb
This notebook uses the BGG XML API to get addition information on the 751 games collected above. I collected the name, rating, overall rank, complexity, plays, owns, wants, and wishlists.

### GameRanks.csv
This is the overall csv that resulted from my data curation. I will document the columns in this section:

**Name**: The name of the board game

**Year**: Year the game was published

**ID**: The internal game id within BGG

**Rating**: A weighted average user rating for a board game on a scale from 1-10. There is also an additional 100 random 'default' ratings (with an average of 5.5) to prevent games with a low number of ratings to dominate rankings. Because of this, all games have ratings closer to 5.5 than they should. However, this effect becomes negligable if a game has a lot of ratings.

**Complexity**: The average user complexity of a board game on a scale from 1-5 with 5 being the most complex.

**Overall Rank**: Rank of a board game based on its rating. The highest rated game has rank 1.

**Plays Last Month**: The recorded number of plays in the last month. (Feb 25, 2024 - Mar 25, 2024) Plays are reported by users on BGG.

**Abstract Rank, Customizable Rank, etc.**: The rank of a board game within the category of Abstract, Customizable, Thematic, etc. Only has values through the top 100. Missing values represent games not in the category or games in the category ranked below 100.

### PersonalGames.csv

An example, 'mini' version of this data set based on my personal collection that I created a few weeks ago. May be useful if I want to compare my games to the top games.

### BGG API.webp

An image of the BGG XML API logo. Added to respect BGG's Terms of Use