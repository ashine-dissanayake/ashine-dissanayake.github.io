# Chapter 3: Neural net foundations

## Assessming Model Performance
**timm** provides pretrained computer vision models. Note that it is similar to HuggingFace, except provides CV models not NPL model. 

## Inference Results from a Pre-trained Model

<img src="../images/inference.png" alt="drawing" width="750"/>

Observations: 
<ul>
  <li> resnet34 ~ 74% </li>
  <li> levit is highperforming </li>
</ul>

## Extra Notes about fastai
<ul>
  <li> In fastai, data categories are stored in learn.dls vocab obejct. </li>
  <li> After attempting to classify an image, a dictionary of hte probability of each categorises is retrieved. zip and map can be used to create tuples of categories and prob. </li>
</ul>

## Neural Net 101
Notes from watch recording: 
<ul>
  <li> Basic functionality: (1) Multiplies each input by a number of values. These values are known as parameters (2) Adds them up for each group of values and (3) Replaces the negative numbers with zeros. </li>
  <li> The aforementioned funtionality comprise one layer. </li>
  <li> In order for the function to learn, the parameters can be changed to be made better. Referred to as gradient descent. </li>
  <li> The recording goes through gradient descent and uses a quadrative formular to teach it. </li>
</ul>

## Automating gradient descent [using mean absolute error]
If the gradient of our mae() function with respect to our parameters, a, b, and c, then adjusting those values will be easy. Adjust our parameters a bit in the opposite direction to the sign of the gradient.GOAL: to make that cost function as small as possible. 

## Rectified linear function (ReLU)
...

## Building Linear Regression Model
<ul>
  <li> Matrix multiplication </li>
  <li> Require fields and target.  </li>
  <li> Create inital params randomly. (i.e., RAND() - 0.5)  </li>
  <li> Since in the titanic example, fare >> other feild values, it skews the results. Need to ensure than everything is between 0 - 1/. </li>
  <li> Linear value is calculated by SUMPRODUCT data and params. </li>    
  <li> Apply RelU function. All negative values set to 0, otherwise retain value. </li>
  <li> Preduict is the sum of ReLU. </li>
  <li> Loss = (predict - actual)^2 </li>  
</ul>
