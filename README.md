# I. About of the project

1. Purpose 
    - This is intended to be a ML model with the purpose of prediction Counter written in Python using Co-Pilot support
    - ***TBU graphs and diagrams***
2. Subjectives 
    - By feeding the program a standardized formatted txt file of each tournament. We will use 3 different algorithms: ***Logistic Regression, Random Forest and XGBoost(Gradient Boosting)*** to output different outcomes and compare them to actual
    - Source of data: is collected from HLTV match data since i dont have money for Liquidpedia API (200 a month is genuinely beyond robbery) limited to the
3. Parameters 
    - Tournament name: Team names, their rank, global rank, maps played, players’ names and their KDA as tuples (each tournaments), (maybe ELO points but not as significant), the month/year
    - We can also gives each tournament an index of importance since the Major has a different way of calculating points) and the size of their teams ranking in general (rank A dominant tournaments have greater indices than B-ranked teams dominant as for different brackets)
    - 

# II. Data structures and Algorithms

1. Features of the program: 
    - Map win rates:
    - Player rating aggregates: average HLTV rating
    - Head-to-head stats
    - Roster Stability:
2. Data structure: 
    - Input txt file: {[Tournament name], [Teams], [Index], [Month-Year], [Place]}}
        - Where Teams are fomatted as {Team Name, (Player name, ELO ranking, Personal KDA, Tournament KDA ), [(Map played with win-lose ratio)] Bracket, HLTV ranking, Tournament Ranking, Tournament MVP}
    - Mainly use a linked list to store information
3. Algorithms
    1. ***Logistic Regression***: simple and interpretable that predicts the probability of team A winning: 
        - Fast and easy to understand (personal learning purpose)
        - Good baseline 
        - Works well with ELO, map win rates and player ratings 
    2. Random Forest: tree-based ensemble model that handle nonlinear relationships 
        - Complex patterns since it is resistant to overfitting 
        - Good for tabular esports data 
    3. XGBoost: most common and strongest performer for most esports prediction tasks 
        - High accuracy 
        - Handles missing data and has the ability to learn subtle interaction between features