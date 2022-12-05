# Projet_Python

Our problem is to be able to train a model to best predict the number of shares of an article upon its publication.

As a first step, we have cleaned up some superfluous columns and normalised the names of the columns. Indeed, some column names had spaces in them, which is not very practical for us. We also checked if unusable values were in the database.

Then, we optimised the days and domains columns by adding them into a single one. So, we have a column day and a column domain, with the days of ther week for the first and the domains of the articles for the second (tech, business, lifecycle...).

By displaying the correlation of each variable thanks to our heatmap, we found that the features were uniformly correlated to the number of shares. They are not individually important however. Nonetheless, the number of keywords turns out to be the variable most correlated with the number of shares.

We then normalised the data to prepare it for model training.

First, we wanted to try Regression medels. We used linear regression, decision tree, logic regression, svm and neural network models. However, the results were not at all convincing (close to randomness), so we chose to take the problem in classification and not in regression. 

To do this, the models will now predict whether an article will get more shares than the average or not. So, we changed the column 'shares' to a binary one, '1' being a popular article (above average) and '2' being an unpopular one (below average). We used logistic regression, descision tree, random forest and svm models. These models gave us much more satisfaction by achieving a maximum accuracy of 0.88 for the random forest.
