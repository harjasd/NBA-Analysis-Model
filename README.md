# NBA-Analysis-Model

We are using the package ‘HoopR’ to gather data for our project. HoopR is designed to return data tables with specific NBA stats. We can use it to get the standings from any past season, individual player season stats from any season, or individual player stats from specific games. Using this package, we aim to build a model that attempts to predict the season champions.

To conduct the EDA, we needed to ensure that our dataset was clean. Our dataset was mostly clean, but we did need to remove NA values from various rows and columns. To do this, we tested for unique values and NA values in the dataset as part of our data cleaning. For our goals, we also needed to further clean the data and select the columns (variables) most necessary for our EDA.

Before filtering into a subset dataframe, the HoopR dataset had over 500,000 rows with more than 50 columns. After aggregating the essential data, we now have a little over 6,000 rows and about 28 columns. The raw columns included: points_scored, field_goals_attempted, 3_pointers_scored, team_winner, turnovers, number_of_games_played, player_name, team_name, player_position, and many others that we excluded due to their irrelevance to our dataset. Our columns now consist of variables like: avg_pts, avg_blks, plus_minus, avg_mins_played, avg_3pts, avg_fga, avg_fgm and much more. These variables are extremely relevant to our questions because the bottom line of our project is to depict why winners win and what it takes for a player to earn the MVP trophy.

So far, we have conducted some preliminary EDA to determine which features are most important in predicting an NBA champion. We have gathered a list of features—Team Points per Game, Team Points Allowed per Game, Bench Points, Scoring Efficiency, and Team Rebounds +/-— that appear to play a role in predicting a winner, mvp and champion.

## Data Analysis

### Assumptions

Some assumptions we wanted to make were that we think teams who had more distributed positions would win more championships up until 2015 whereas nowadays we think teams who have higher shooting percentages win championships. Another assumption we wanted to make was that we think in season win rates correlate highly with winning the championship. Rather than just tanking the season and putting yourself in a desirable low position for playoffs. Our last assumption would be that nowadays there is a much higher ratio of three pointers taken and we think because of this the average score in games have increased by far; however, we think this is an overall league shift and has not drastically changed the reasons why teams win.

### Analysis

The first steps we took when looking at this large dataset was wonder which variables will best help us in our goal. We all sat down and discussed what makes teams and players successful and came to a conclusion the most important statistics are points per game, field goal percentage, assists per game, steals per game, blocks per game and free throw percentage.

After finding our desired list, we created a subset of the data grouped by team with the variables named before. We then visualized each statistic using a histogram and were surprised with the results. The Denver Nuggets won the championship last year and we are currently working with 2022-2023 season. From our data, the Nuggets placed in the top five in only two categories. We were shocked when we saw this as it went against all of our ideas. 

After seeing the plots (plots below), we decided to add more variables such as the total team points, field goals attempted, threes attempted, average lead, turnovers, average offensive and defensive rebounds, and more.

#### Models

1) Linear Regression

We are thinking of making a simple linear regression model to predict champion ship wins by either wins, total points or even some computed overall team score that we would create.

2) KNN

We want to use KNN to find clusters of teams and similarities between championship winners. This will help us make our linear regression and our neural network more accurate by giving better parameters.

3) Neural Network

We want to use a simple fully connected neural network to predict championship winners with a large set of parameters for a high level of accuracy. We are thinking of using parameters such as wins, players, points per game, efficiency scores. This may change depending on our KNN model and what is tells us about the underlying statistics.

#### Evaluation Approaches

1) Linear Regression:

Mean Squared Error (MSE): Calculate the MSE between the predicted championship wins and the actual championship wins. Gives a measure of how well the linear regression model is performing.

2) KNN:

Visualization: Visualize the clusters formed by KNN to see if they make sense and correspond to meaningful groupings of teams.

3) Neural Network:

Accuracy: We are going to use accuracy as a metric, which measures the proportion of correctly classified instances.

Loss Function: We are going to use a loss function, such as cross-entropy loss for classification tasks, to measure the difference between the predicted and actual values.

Validation Set Performance: Split data into training and validation sets. Monitor the performance of the neural network on the validation set to check for over fitting.

Confusion Matrix: For classification tasks, we can use a confusion matrix to see how well the neural network is classifying instances into different categories.

