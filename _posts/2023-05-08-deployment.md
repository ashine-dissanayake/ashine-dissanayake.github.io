# **Chapter 2:** Deployment

## Objective
This chapter addresses the following topics: 
<ul>
  <li> Designing a machine learning project. </li>
  <li> Creating dataset. </li>
  <li> Training model. </li>
  <li> Supporting Software: Hugging Face Space with Gradio. </li>
</ul>


## Considerations Before Starting a Project
<ul>
  <li> The six lines that are mentioned in the previous exercise are not going to be effective for every deep learning problem. "Underestimating the constrainsts and overestimating hte capabilities" could yield poor results.</li>
  <li> Similarly "over estimating the constraints and underestimating the capablity" won't work either. </li>
  <li> Be optimistic about the approach. Even if you do not have enough data, you may expect to see some results.  </li>
  <li> An important consideration is data availibilty. The goal is not to find the perfect dataset or project, but just get started with what you have and assess the outcome. </li>
  <li> Iterate end-to-end instead of tedious focusing on certain parts of the project. Will be able to identify trickiest parts in the project. </li>
</ul>


## State of Deep Learning 
### Computer Visions
The concept that computers can detect items in images better tahn humans. This concept is known as object recoginition. Computer vision has the potential fo detecting items and classifying them correctly in the image. This action is referred to as object detection. Determining what the pixel is apart of (segmentation). Note that a deep learning algorithm is not effective image recognition. A singificant challenge in object detecting is labelling images, which can be slow and expensive. Data augmentation and creating synthetic images can quicken that process.  

## Drivetrain Approach 
1. Defined Objectives
2. Levers
3. Data
4. Models

# Creating Model
1. **Gathering data:** Down the images from the web using a fastai function `download_image`. It will download all the URLs for each of out search terms. Put each classifer into seperate folders. 
2. **Clean:** Need to verify that the images downloaded are not corrupt. Identifying corrupted images by using `verify_images` function an deleting those images using `unlink`. 
3. **Data -> DataLoader:** To turn the data into a `DataLoader` need to address the following: (1) Type of data (2) Retrieve list of items (3) Label items and (4) Create validation set. Aftewr hte DataLoader is created, the validation set can be seen, all iamges can be resized or cropped. **Data Augmentation:** using exisitng images, resizeing, rotating, cropping, flipping, brightness change, contrast change or perspective change. There is a function is fastai called `aug_transform` to complete data augmentation. 
4. **Training Model:** Train using `vision_learner` to create a `Learner   object adn fine tuning. Can see the performance using a confusion matrix, assessing the top losses. 
5. **Cleaning Dataset using Trained Model:** Assses hte top losses to see hte images with the highest loss in our dataset. The probability is the confidence level (0-1). Using `ImageClassiferCleaner` to keep or delete images with the highest loss values. 
6.  **Export Model:** Use `export` function to create a .pkl file. 


## Questionnaire
1. **Provide an example of where the bear classification model might work poorly in production, due to structural or style differences in the training data.** Occlusions, low resollution images, not enough variation in the image. 
1. **Where do text models currently have a major deficiency?** Struggle to create factually correct responses. 
1. **What are possible negative societal implications of text generation models?** Ingesting inforamtion that is bias towards a certain agenda, meaning that the result can be potentaially damaging. 
1. **In situations where a model might make mistakes, and those mistakes could be harmful, what is a good alternative to automating a process?** Having a two part system that involed human checking to ensure that the output is correct and if any changes need to be made to the existing model (similar to cleaning data). 
1. **What kind of tabular data is deep learning particularly good at?** Data rich datasets that have categorical attributes. 
1. **What's a key downside of directly using a deep learning model for recommendation systems?** Not informative outputs(?)
1. **What are the steps of the Drivetrain Approach?** 1. Defined Objectives 2. Levers 3. Data 4. Models.
1. **How do the steps of the Drivetrain Approach map to a recommendation system?** TBC  
1. **Create an image recognition model using data you curate, and deploy it on the web.** TBC
1. **What is `DataLoaders`?** Containing training set, validation set, training type. 
1. **What four things do we need to tell fastai to create `DataLoaders`?** (1) Type of data (2) Retrieve list of items (3) Label items and (4) Create validation set. 
1. **What does the `splitter` parameter to `DataBlock` do?** Splits training and validation set. 
1. **How do we ensure a random split always gives the same validation set?** Provide a seed value. 
1. **What letters are often used to signify the independent and dependent variables?** independent is x and dependent is y. 
1. **What's the difference between the crop, pad, and squish resize approaches? When might you choose one over the others?**
1. **What is data augmentation? Why is it needed?** Using exisitng images can modfying them by flipping, rotation, perspective warping, brightness changes to generate more variation in images. 
1. **What is the difference between `item_tfms` and `batch_tfms`?**  single data vs a dataset. 
1. **What is a confusion matrix?** Predictions vs correct labels. Help clear up which classes are getting confused with eachother. 
1. **What does `export` save?** pkl file of trained model. 
1. **What is it called when we use a model for getting predictions, instead of training?** When we use a model for getting predictions, instead of training, we call it *inference*.
1. **What are IPython widgets?** GUI componenets in notebook. 
1.** When might you want to use CPU for deployment? When might GPU be better?** Multiprocessing. Makes training quicker. 
1. **What are the downsides of deploying your app to a server, instead of to a client (or edge) device such as a phone or PC?** connectivity or lag. 
1. **What are three examples of problems that could occur when rolling out a bear warning system in practice?** Environmental conditions, identifying other animals, occulsions or low resolution.  
1. **What is "out-of-domain data"?** TBC
1. **What is "domain shift"?** TBC
1. **What are the three steps in the deployment process?** Manual Process, Limited scropt Deployment, Gradual Expansion. 
