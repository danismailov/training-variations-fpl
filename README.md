# fpl-with-fml

## Current features
-> A list of gameweeks, with opponent team merged on, which is then used to make a Simple Moving Average for _n_ gameweeks. _(Note that n gameweeks isn't the same as n games, as you can have double gameweeks, which I'm sure I haven't handled well in the training data and its current form...)_
-> Initially, I've tried 5, 3 or 2 previous gameweeks, with the latter two performing better, albeit capped at around ~65% accuracy.
-> Due to me not actually having a good intuitive sense of what the regression evalation metrics mean in context, I'm erring on the side of using classification as the problem type, as at least this gives me a nice, simple, understandable accuracy number. _(This still doesn't avoid the fact that I'm clueless when it comes to any variation in the balanced_accuracy or mcc metrics for classification that AutoGluon provides...)_

## TODO of new features

### Evaluation
-> I need to better understand both classification and regression evaluation metrics, perhaps by (a) using the xP metric that FPL provide themselves as a benchmark, and seeing whether I can improve on that; and (b) seeing what the resulting metrics from other FPL machine learning projects on github have been, and trying to aim for those 

### Features
-> Cleaning the data, or filtering to only include players who have played more than X minutes. Currently, the vast majority of stats are 0 or NaN which can't be helping.
-> Adding more features specifically about the player themselves. E.g. raw features from previous few gameweeks, as well as simple or weighted/exponential moving averages.
-> Adding more features about the opposing team. Currently, I'm literally just providing their name, which likely doesn't do much.
-> Adding more features about the team's recent performance.
