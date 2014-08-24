## Preprocessing
The data consists of 160 column table with some columns with many empty, NA and '#DIV/0!' values that could not be used for training and which were separated from useful data

## Data sets
the Training and Testing data were divide as 70% and 30% respectively and since the classe outcome data was ordered these portions needed to be randomized sampled

## PCA (Data reduction)
To apply PCA, first we calculated the correlation matrix of the data and applied the svd function to obtain the set of eigenvalues, eigenvectors and diagonal matrix
Based on the Ratio of the sum of the first (k) elements of the diagonal matrix per the total sum, the minimun k which outcomes 95% of variance is chosen and this is the number of components used on the PCA transformation

## Training
The train and test sets are transformed to k PCA components and these sets used to train the class models. Namely the "A", "B", "C", "D", "E" classes each have a predictor

## Testing
The predictors are applied to the test PCA transformed set and the prevision given as true when greater than treashold 0.5 confidence
the model didn't get a good mark though, 24%

## Applying to unknown data
The unclassified data is converted to PCA components and the models applied to it
the outcome of confidence of models say which class the data belongs to, when none apply an '?' is set
