# Programing for Data Science - Final Project
## Group members:
1. Trần Thị Thiên Kim - 22127225
2. Lê Thanh Tâm - 22127374
3. Phạm Trần Yến Quyên - 22127357

## About the Project:
### Dataset:
- Data type: Tabular, Time-Series
- Source: UCI Archive
- Overview: Each skillshot performed is characterized by 18 features, composed of players inputs and in-game metrics, collected at different time, creating a multivariate time series.

### Data shape: 
- $19$ columns of **attributes**.
- $7191$ rows of **entries**. 

### Data structure:
The dataset has the following structure:
- **Class Labels**: A line with only 1 interger that specifies the class label for the upcoming block of data (e.g., 6).
- **Data Blocks**: Each block consists of multiple rows of numerical data followed by another class label.

#### Classes:
- There are $7$ classes, `-1` representing noise (composed of failed figures and random moves): 
    + `-1`: noise
    + `1`: ceiling shot
    + `2`: power shot
    + `3`: waving dash
    + `5`: air dribble
    + `6`: front flick
    + `7`: musty flick

### Features: There are $18$ features per class. WHERE:
- **Measurements (Continuous Variables)**: These columns represent quantitative measurements related to the ball, player, and environment:
    1. `BallAcceleration`: Acceleration of the ball.
    2. `Time`: Time elapsed.
    3. `DistanceWall`: Distance to the wall.
    4. `DistanceCeil`: Distance to the ceiling.
    5. `DistanceBall`: Distance between player and ball.
    6. `PlayerSpeed`: Speed of the player.
    7. `BallSpeed`: Speed of the ball.
- **Actions (Categorical/Binary Variables)**: These columns represent actions taken by the player, typically with binary values (0 or 1): 
    1. `up`: Action - move up. 
    2. `accelerate`: Action - accelerate. 
    3. `slow`: Action - slow. 
    4. `goal`: Action - goal attempt. 
    5. `left`: Action - move left. 
    6. `boost`: Action - boost. 
    7. `camera`: Action - camera adjustment. 
    8. `down`: Action - move down. 
    9. `right`: Action - move right. 
    10. `slide`: Action - slide. 
    11. `jump`: Action - jump.

### Data Quality and Distribution Analysis:
- Duplicates: There are 15 duplicate rows in the dataset.
- Missing Data: No missing values in any of the columns.
- Numerical Columns:
    + All columns appear to be numerical (float or int).
    + Descriptive statistics reveal the range, mean, and distribution of values for each feature.
- Data Types: All columns have appropriate data types (float64 for features, int64 for the class label).
- Class distribution: Class `5 - air dribble` is the most used move in the dataset.