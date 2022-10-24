# NFL Prediction Model
Building out different models to accurately predict various outcomes in any given NFL game


The vision of this project would be to continuously create new models and variations of existing models that predict the overall outcome of NFL games each week. A database would be used to track model parameters(features, model types, etc.) and historical predictions/outcomes. Finally a web application would also be created to clearly see which models are performing best week over week as the NFL season progresses throughout the year. 

### Prediction Outcome Ideas
- Team win/lose
- First play pass/rush
- Over/Under
- Anytime Touchdown scorer


## Installation


#### Note*: If you are using the sportsipy package, you will need to modify your constants.py file in the NFL folder with the following changes in order to pull game data for unplayed games.

Within the **BOXSCORE_SCHEME** dictionary, change the following:

FROM:
```python
'home_name': 'a[itemprop="name"]:first',
'away_name': 'a[itemprop="name"]:last',
```
TO:
```python  
'home_name': 'div[class="scorebox"] div:first div strong a',
'away_name': 'div[class="scorebox"] div:nth-child(2) div strong a',
```

There is currently an open [issue](https://github.com/roclark/sportsipy/issues/729) for this, but even the proposed solution does not account for unplayed games in the current season. The fix above will make this work.

## Documentation

## References
- Original inspiration pulled from [Active State page](https://www.activestate.com/blog/how-to-predict-nfl-winners-with-python/)
- 538 ELO Ratings from [here](https://data.fivethirtyeight.com/#nfl-elo)
- [Building A Logistic Regression in Python](https://towardsdatascience.com/building-a-logistic-regression-in-python-step-by-step-becd4d56c9c8)
