# **Chapter 1:** Getting Started

## Setting up Kaggle 
Kaggle provides a platform for data scientists, machine learning engineers, and other practitioners to collaborate and compete on solving complex data science problems. 

## Myth Buster
The three following myths are not required when conducting deep learning. (1) Do not need a lot of math (max. highschool math is sufficient) (2) Do not need a lot of data (we've seen record breaking results with <50 items of data) (3) Do not need a lot of expensive computers (you can get what you need for state of the art work for free).

## Deep Learning
Deep learning is a computer technique to extract and transform data by using multiple layers of neural networks. The term “deep” refers to the fact that these N.N. are typically composed of many layers, which allow the, to learn hierarchical representations of data. Each layer receives inputs from the previous layer alongside weights, to progressively refine them. 

Deep Learning has many applications, areas including physical sciences, the arts, medicine, finances, scientific research, etc. The table below summarises the various disciplines (sourced from the video). 

| Disciplines | Example Applications |
| ----- | ----- |
| Natural Language Processing (NLP) | Answering questions; speech recognition; summarizing documents; classifying documents; finding names, dates, etc. in documents; searching for articles mentioning a concept |
| Computer Vision | Satellite and drone imagery interpretation (e.g., for disaster resilience); face recognition; image captioning; reading traffic signs; locating pedestrians and vehicles in autonomous vehicles |
| Medicine | Finding anomalies in radiology images, including CT, MRI, and X-ray images; counting features in pathology slides; measuring features in ultrasounds; diagnosing diabetic retinopathy |
| Biology | Folding proteins; classifying proteins; many genomics tasks, such as tumor-normal sequencing and classifying clinically actionable genetic mutations; cell classification; analyzing protein/protein interactions |
| Image Generation | Colorizing images; increasing image resolution; removing noise from images; converting images to art in the style of famous artists 
| Recommendation Systems | Web search; product recommendations; home page layout |
| Playing Games | Chess, Go, most Atari video games, and many real-time strategy games |
| Robotics | Handling objects that are challenging to locate (e.g., transparent, shiny, lacking texture) or hard to pick up |
| Other Applications | Financial and logistical forecasting, text to speech, and much more... |

## Neural Networks
- Similar structure and function as human brain. 
- Comprise multiple hidden layers. 
- All layers contain neurons/nodes and they work as one unit to execute computational tasks. 
- Each nodes can multiple inptuts and apply mathmatical functions.
-  Output of one layers is fed into current layer's inputs. 
-  Certain layers used for feature extractions and pattern recognitions for dataset.
-  During the training process, the network adjusts the strengths of the connections between neurons to improve its ability to accurately make predictions on new, unseen data.
-  Different types of neural networks: 
    - Feedforward Neural Network
    - Convolutional Neural Network
    - Recurrent Neural Networks 

## Software Explanations
Required software: 
- PyTorch
- fastai
- Jupyter Notebook 
- timm
- fastbook 
- duckduck_go

## Machine Learning 

### What is Machine Learning?
Types of ML Models: 
- Supervised Learning: Training set contains data with labels. 
- Unsupervised Learning: Training set contains data with no labels. 
- Reinforcement Learning: Trainng an agent to learning a defined policy to optimise the result. 

###  Birds vs Forests Model
**Steps:**
<ul>
  <li> Step 1: Download images of birs and non-birds. </li>
  <ul>
    <li> search_images - grabs however many images specified (by default 200). </li>
    <li> Grab 200 examples of each of "bird" and "forest" photos and save each group ofphotoes to a different folder. </li>
  </ul>
  <li> Step 2: Train our model. </li>
  <ul>
    <li> Some photos might not download correctly which could cause our model training to fail, so we'll remove them. </li>
    <li> Use verify_images will try to open an image under hte filename. If the image can be openeed, it will return True, if the file cannot be opened, it will return False. </li>
    <li> If image cannot be opened, unlink or remove from path. </li>
    <li> To train a model, we'll need DataLoaders, which is an object that contains a training set (the images used to create a model) and a validation set (the images used to check the accuracy of a model -- not used during training). </li>
    
``` cpp
dls = DataBlock(
    blocks=(ImageBlock, CategoryBlock), 
    get_items=get_image_files, 
    splitter=RandomSplitter(valid_pct=0.2, seed=42),
    get_y=parent_label,
    item_tfms=[Resize(192, method='squish')]
).dataloaders(path)

dls.show_batch(max_n=6)
    
# blocks - The inputs to our model are images, and the outputs are categories (in this case, "bird" or "forest").
# get_items - To find all the inputs to our model, run the get_image_files function (which returns a list of all image files in a path).
# splitter - Split the data into training and validation sets randomly, using 20% of the data for the validation set.
# get_y - The labels (y values) is the name of the parent of each file (i.e. the name of the folder they're in, which will be bird or forest).
# item_tfms - resize each image to 192x192 pixels.
# Trained using `reset18`
```   
  </ul>
  <li>  Step 3: Use our model </li>
</ul>

## Video Notes
<ul>
  <li>Ran through bird vs forest model. </li>
  <li> Creating images from video prompts using DALL·E 2</li>
  <li> Google AI Blog</li>
  <li> Data Ethics</li>
  <li> Can find features in images. More images you provide the better the result will be. How neural network can acheive this. </li>
  <li> Image recoiser than be user to identify sounds. Create pictures from waveforms. Take time series and turn into pictures. </li>
  <li> Dont need math. Dont need data (we've seen record breaking results with <50 items of data). Don't need lots of expensive compiters. </li>
  <li> Using PyTorch. Tensor flow is dying in popularity nad PyToarch is growing rapidly. </li>
  <li> Using Juypter Notebook  on a cloud sever. </li>
  <li> Resize because it might take too much processing time. </li>
  <li> Fastai won't run if you dont provide a dataset.</li>
  <li> Everyhitng must be the same size. </li>  
  <li> for functions to use have a look at datablock. </li>
  <li> Segmentation. Colour in pixels for seperate entities. </li>  
  <li> Table analysis. </li>  
  <li> Collaborating filtering: Which uses use which products. And you use that to find other things similar users might like.  </li>
  <li> Valid loss = mean quare error. </li>  
  <li> A normal computer program. Program contains all the fancy stuff. A achine learning model contrains inputs weight as inputs, the model and the output is result.  An addition tot eh results is the loss which will get fed back into the model and update the weights.</li>  
  <li> Valid loss = mean quare error. </li>  
  <li> Valid loss = mean quare error. </li>    
</ul>
