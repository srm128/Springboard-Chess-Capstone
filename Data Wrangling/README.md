Capstone Two: Data Wrangling

Data Collection:
The original data was roughly a 200 gb file covering over 90 million chess games. In order to accomplish the data collection aspect of this capstone, the data needed to be divided into more manageable pieces due to hardware/software limitations (jupyter notebook would crash if it was all done in one notebook). The data was originally presented as one giant string written as blocks of information. I looked at patterns in the raw data and defined our own function that utilizes Python's Regular expression in order to extract the needed data. The goal was to create one csv file that neatly organizes the following data: 

- game_urls
- events
- white_elos
- black_elos
- time_controls
- results
- terminations
- openings

Here you will find the code and steps used to separate out the variables and their observations. I repeated these steps several times to create individual CSV files that I would later merge:
https://github.com/srm128/Springboard-Chess-Capstone/blob/main/Data%20Wrangling/Capstone%202%20-%20chess%20data%20-%20black_elos.ipynb


Here you will find the merging of all of the data into one CSV file:
https://github.com/srm128/Springboard-Chess-Capstone/blob/main/Data%20Wrangling/Capstone%202%20-%20Data%20Collection%20-%20Merging%20All%20Data.ipynb


Data Definition / Data Cleaning 
These steps can be found here: 
https://github.com/srm128/Springboard-Chess-Capstone/blob/main/Data%20Wrangling/Capstone%202%20-%20Data%20Definition%20Cleaning.ipynb

While definitions will be provided within the notebook, here are the columns from the dataset upfront:

- Event: Event is the type of chess game. Related to time control.
- White Elo/Black Elo: Player ratings. 
- Result: Who won. 1-0 is White. 0-1 is Black. 1/2-1/2 is a draw. 
- Termination: How the game finished. Did a player resign or were they checkmated. 
- Time Control: Speaks for itself. Is in seconds and the number following the "+" is the increment if any. 
- Opening: Name of the opening players played. It is generally defined by the first few moves and it is dependent on both players' moves. 
- Game URL: Unique identifier for each game. Able to go to see them online.

In summary, we will be looking at 44332657 chess games. These chess games are Blitz games which means they are between 180 to 479 seconds.  We removed roughly 50 million games due to missing and incomplete values, different time controls, or incorrect indexing by the data source. 

