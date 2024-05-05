# Model Card

## Model Description

**Input:** Inputs were selected from the data based upon interpretability and ease of processing.
- venue - a 2-character string, representing the course this race took place at: ST = Shatin, HV = Happy Valley.
- surface - a number representing the type of race track surface: 1 = dirt, 0 = turf.
- distance - distance of the race, in metres.
- going - the condition of the race track.
- race_class - a number representing the class of the race
- horse_age - the age of the horse at the time of the race
- horse_country - the origin country of the horse
- horse_type - the sex of the horse
- horse_rating - the HKJC rating assigned to this horse at the time of the race.
- declared_weight - the declared combined weight of the horse and jockey, in lbs.
- actual_weight - the weight carried by the horse, in lbs.
- trainer_id - unique identifier given to the trainer of the horse.
- jockey_id - unique identifier given to the jockey riding the horse

**Output:** 
- result - a horse's finishing position in a given race

**Model Architecture:** 

I used a Gradient Boosting Regressor, with tuned hyperparameters:
- n_estimators: The number of trees in the forest
- learning_rate: The step-size shrinkage
- max_depth: Controls the tree depth
- min_samples_split: The minimum number of samples required to split an internal node


## Performance

I used Mean Squared Error (MSE), Root Mean Squared Error (RMSE), Mean Absolute Error (MAE) and R-Squared (R2) metrics to measure the performance of my model, with the below final results.

|           Model       |      mse      |     rmse     |     mae      |     r2       |
|----------------------|---------------|--------------|--------------|--------------|
|           GBR        |   13.245066   |   3.639377   |   3.064864   |   0.047022   |


## Limitations

My dataset only contains horse races (and the results thereof) for races that took place in Hong Kong in 1997-2005. This means that any of my results are limited to predicting a small subset of horse races, with restricted applicability to other countries, and more recent races.

## Trade-offs

The hyperparamter tuning of my model took a long time to run, as did the general fitting. This means it wouldn't be great if we needed to update, say, betting odds on the fly during a race due to updated data. A repercussion of this is also that if we were to expand the dataset to be more diverse, the computation time would be even higher.

Whilst the Mean Absolute Error suggests accuracy within 3 places, the r-squared value is low, suggesting poor fit overall.
