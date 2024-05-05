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
I used a Gradient Boosting Regressor


## Performance

|           Model       |      mse      |     rmse     |     mae      |     r2       |
|----------------------|---------------|--------------|--------------|--------------|
|           GBR        |   13.245066   |   3.639377   |   3.064864   |   0.047022   |

Give a summary graph or metrics of how the model performs. Remember to include how you are measuring the performance and what data you analysed it on. 

## Limitations

My dataset only contains horse races (and the results thereof) for races that took place in Hong Kong in 1997-2005. This means that any of my results are limited to predicting a small subset of horse races, with restricted applicability to other countries, and more recent races.

## Trade-offs

The hyperparamter tuning of my model take a long time to run, as does the general fitting. This means it wouldn't be great if we needed to update, say, bettings odds on the fly during a race due to updated data. A repercussion of this is also that if we were to expand the dataset to be more diverse, the computation time would be even higher.

Whilst the Mean Absolute Error suggest accuracy within 3 places, the r-squared value is low, suggesting 

Outline any trade-offs of your model, such as any circumstances where the model exhibits performance issues. 
