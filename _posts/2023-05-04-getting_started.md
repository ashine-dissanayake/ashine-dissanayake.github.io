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
Neural networks are a type of computing system that is modeled after the structure and function of the human brain. They are composed of layers of interconnected processing nodes or "neurons" that work together to perform a specific computational task.

Each neuron in a neural network receives one or more inputs and applies a mathematical function to those inputs to produce an output. The outputs of one layer of neurons are used as inputs to the next layer, and so on, until the final output is produced.

Neural networks are often used in machine learning to learn patterns and relationships in data, such as identifying objects in images or predicting the likelihood of a particular outcome based on a set of inputs. During the training process, the network adjusts the strengths of the connections between neurons to improve its ability to accurately make predictions on new, unseen data.

There are many different types of neural networks, including feedforward neural networks, convolutional neural networks, and recurrent neural networks. Each type of network is optimized for a specific type of problem or data structure.

## Software Explanations
The table below summarises the software that will be used when conducting deep learning. 
| Software | Description |
| ----- | ----- |
| PyTorch | PyTorch is an open-source machine learning library that is primarily used for building deep neural networks. It was developed by Facebook's AI research team and is based on the Torch library, which is a scientific computing framework for Lua programming language. PyTorch provides a range of tools and modules that make it easy to build and train complex neural networks, including support for automatic differentiation, which makes it easy to compute gradients and optimize models. It also provides support for distributed computing and allows models to be run on GPUs and other accelerators. |
| fastai | Fastai is a high-level open-source deep learning library that is built on top of PyTorch. It was developed by Jeremy Howard and Sylvain Gugger, who are both well-known experts in the field of deep learning. |
| Jupyter | Jupyter is an open-source web application that allows you to create and share documents that contain live code, equations, visualizations, and narrative text. The name "Jupyter" is a combination of the three programming languages it supports: Julia, Python, and R. |

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
