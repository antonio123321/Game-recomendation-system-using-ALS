# Game-recomendation-system-using-ALS

I used  Apache Spark and its Python API, PySpark in databricks enviroment to implement this project.
The data derive from a csv file named steam-200k.csv. It provides details on the games different members have purchased and played, along with the number of hours they have played each game. It contains four columns:

The first column contains a unique identifier for each member

The second column contains the name of the game they purchased or played

The third column contains details of the member's behavior, either ‘purchase’ or ‘play’. Because a game has to be purchased before it can be played there will be two entries for the same game/member combination in some instances

The fourth is set to 1 for rows where the behavior is ‘purchase’. For rows where the behavior is ‘play’ the value in the fourth column corresponds to the number of hours of play

Initially, I perform some EDA showing the 10 bestselling games, and among those, the ones that were played for the longest time. Subsequently, I trained 4 different models using Alternative Least Squares. The first model was trained with the whole dataset, while from the second model onward, the models were trained using a dataset that didn't include outliers.

Grid search was employed for hyperparameter tuning, and RMSE metrics were used to evaluate the different models
