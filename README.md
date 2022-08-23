# ff_pred2

## Data sources
- FFDatabase (historical stats)
- FFReference (historical ages)
- MyFantasyLeague API (list of current players)
- MyFantasyLeague API (ages current player)
- OurLads (posRanks current players)


## Build Model
### Scrape Historical Data
- FFDatabase & FFReference
scrape_ffDB_histStats.ipynb > weekly_xx.csv
scrape_ffRef_histAges.ipynb > ages_historical.csv
### Clean
weekly_xx.csv > clean_ffDB_histStats.ipynb > modelSource.csv
ages_historical.csv > clean_ffRef_histAges.ipynb > modelAges.csv
## Build Model
modelSource.csv > modelBuild3.ipynb > rfmodel_XX1.joblib


## Make Predictions
### Scrape and Clean Current Data
- MyFantasyLeague & OurLads
clean_currentPlayers.ipynb > toPredict.csv
## Predict
rf_model_XX1.joblib + toPredict.csv > modelPredict3.ipynb > predictionsSeason.csv & predictionsWeek.csv





