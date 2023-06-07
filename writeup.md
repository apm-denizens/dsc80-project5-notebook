# League of League of Legends Role Prediction from Post-Game Data

## Framing the Problem

-   Clearly state your prediction problem and type (classification or regression). If you are building a classifier, make sure to state whether you are performing binary classification or multiclass classification.

This is a multiclass classification problem. The role/'position' being predicted has 5 possible values ('top', 'jng', 'mid', 'bot', 'sup').

-   Report the response variable (i.e. the variable you are predicting) and why you chose it, the metric you are using to evaluate your model and why you chose it over other suitable metrics (e.g. accuracy vs. F1-score).

The response variable, as you might be able to guess, is 'position'. The reason we chose it, as you might be able to guess, is because this is the only variable that contains role information. If we're trying to predict role information, there really isn't much other choice.

The metric we have chosen to evaluate the model with is simply accuracy. Since we are not dealing with high-stakes scenarios (like medical diagnosis) where false-negatives could lead to deaths, we don't really need to consider precision & recall. For our case, false-negatives and false-positives have an equal cost. We want to maximize true-positives & true-negatives, and since we have an exactly even class distribution, we have chosen accuracy.

-   Note: Make sure to justify what information you would know at the “time of prediction” and to only train your model using those features. For instance, if we wanted to predict your final exam grade, we couldn’t use your Project 5 grade, because Project 5 is only due after the final exam!

Since we're dealing with post-game data, our "time of prediction" would be when the game has already ended. Subsequently, other than the 'position' column (what we're trying to predict), we have access to all of the other columns at prediction time.

## Baseline Model

-   Describe your model and state the features in your model, including how many are quantitative, ordinal, and nominal, and how you performed any necessary encodings. Report the performance of your model and whether or not you believe your current model is “good” and why.

-   Tip: Make sure to hit all of the points above: many projects in the past have lost points for not doing so.
