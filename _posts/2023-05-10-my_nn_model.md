# Chapter 5: From-scratch model
## Objective
- Create a neural network. 
- Implement training loops for optimising the weights of a model. 
- Learn Sigmoid [makes binary classification easier to train]
- Metrics

### NOTE: Building from the preivous chapter.

## Cleaning Data
- Reading csv file using Pandas. 
- Prior to mulitplying each column by a coefficient, you need to check if the columns contain NULL.  
- Replacing missing values with the mode of the column values. 
- Assess statistic nature of database using `describe()`. The main thing to look for is column will have greater values because later one they will dominate the results. Looking at the histogram is also a great idea to see the distribution of the values.  
- If significant skew a way to solve it is to take the log, which squishes the large numbers and makes the distribution more reasonable. 
- Replace String (i.e., sex, names, ticket) with integer values using `get_dummies`. 
- Change big ranges to be between 0-1. 
- Create independent (predictors) and dependent (target) variables. 
 - Dependent Variables: `t_dep = tensor(df.Survived)` 
 - Independent Variables: `t_indep = tensor(df[indep_cols].values, dtype=torch.float)` 

## Creating Linear Model
- Calculating predictions and losses. 
- Set the params in the random range (-0.5, 0.5) and set hte manual seed. 
- **Predictions:** Multiplying each row by the coefficent and adding them up.
- `t_indep = t_indep / vals`: acts as if there's a separate copy of the vector for every row of the matrix, so it divides each row of the matrix by the vector.
- **Loss functions:** loss = torch.abs(preds-t_dep).mean()

## Gradient Descent Step
- `requires_grad_()` to calculate the gradient descent on coefficients.
- `backward()` to calculate wheather hte coefficents must be increased or decreased. Note: the gradients are actually added to whatever is in the .grad attribute. 

## Training Linear Model
- Create validation set to calculate metrics. 
- `RandomSplitter` returns indices that will split out data into trainign and validation sets. 
- Apply indicies to our independent and dependent variables. 

## Measuring Accuracy 
- Calculate predictions using `preds = calc_preds(coeffs, val_indep)`.
- ~78% not to bad for first run. 

## Sigmoid
- **Challenge:** Some predicted targets are >1 or <0. 
- **Solution:** Pass every prediction through the sigmoid function, which has a minimum at zero and maximum at one.

![](/images/sigmoidal.png "Sigmoidal Graph")

## Neural Network 
- Need to create coefficient for each layer. The above step produce `n_coeff` inputs and create `n_hidden` outputs. `n_hidden` can be selected by the user, although the more hidden those hte more complex the model and the harder it is to train. 
- So we need a matrix of size n_coeff by n_hidden. We'll divide these coefficients by n_hidden so that when we sum them up in the next layer we'll end up with similar magnitude numbers to what we started with.
- Then our second layer will need to take the n_hidden inputs and create a single output, so that means we need a n_hidden by 1 matrix there. The second layer will also need a constant term added.

## Deep Learning 
- Adding more multiple matrices.
- Create additional coefficients for each layer.
- Similar process as mentioned above. 
