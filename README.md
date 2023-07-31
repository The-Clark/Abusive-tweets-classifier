# Training & deploying BERTweet-based NLP model for tweet classification
Contents
   - The problem
   - Creating virtual environment, Installing and importing the necessary libraries
   - The data
   - Data pre-processing
     - Step 1. Dealing with missing values
     - Step 2. Dealing with class imbalance
     - Step 3. Data cleansing and processing into the right format
   - Model Training
     - Step 1. Create your virtual environment (_Optional but advisable_)
     - Step 2. Build the baseline model
     - Step 3. Check model architecture to ensure it works well with data
     - Step 4. Start Model training (_For model performance monitoring purpose, ensure training loss and accuracy is tracked for each iteration_)
   - Model Deployment
     - Step 1. Ensure model is saved with its state_dict so the architecture used in training is maintained.
     - Step 2. Load model maintaining the same architecture used during training
     - Step 3. Deploy model using Streamlit (_Ensure all dependencies are installed, if you can create a Streamlit virtual environment_)

###  The problem
The rapid growth of social media has brought with it an increasing concern over abusive, violent, and hate speech on online platforms. To address this pressing issue, a powerful classification model utilizing BERTweet-based NLP is built. 
This model harnesses the capabilities of BERTweet, a language representation model designed specifically for social media content, to accurately identify and categorize harmful tweets. By effectively distinguishing between offensive and non-offensive content, this NLP-driven approach offers a promising solution to mitigate the spread of harmful messages and foster a safer digital environment for users worldwide.

### Creating virtual environment, Installing and importing the necessary libraries
It is good practice to create and work within a virtual environment as it is important to ensure all versions of libraries used is maintained without being upgraded unknowningly in order to avoid missing dependencies issues. For this classification task, the following libraries is installed and imported. To install, use [pip install (library name)]
   - [x] Libraries
   - [ ] pandas
   - [ ] numpy
   - [ ] torch
   - [ ] sklearn
   - [ ] transformers
   - [ ] regex

### The data
The data used for the training of the model was collected from twitter using entreprise API. It is important to note that the the dataset is domain-centered. The interest for this work is tackling abusive, violent and hate comments on twitter specifically in the sport domain. The majority of the label tweets collected are tweets that are sports related (football, basketball and tennis). The tweets have been labelled into abusive (class 1) and non-abusive (class 0).

### Data pre-processing
The performance of the model is highly dependent on how clean the data is, so this process is the most important process in the model development as it forms the basis of the work. Since we are dealing with texts, it is important to properly clean the text off unwanted noises such as missing values, emojis, flags, white spaces, hashtags, url links, html tags, unicode characters, stop words, digits, @ mentions, punctuations, dealing with class imbalance to eliminate bias and finally ensure our text is formatted to be in lower case.

### Model Training
Before the data is parsed into the model for training, the data is first stemmed/lemmatized to its root form and tokenized so the algorithm can easily learn the patterns in the dataset. Model architecture is built with all the hyper-parameters such as max length, learning rate, epoch etc are set to required values and then the model can now be trained.

### Model Deployment
For the model deployment, Streamlit is used. This is a free service to use for model deployment. There are other tools like flask, heroku etc. The model is hosted on Streamlit as a web app and then tested with unseen data for classification purpose.

All the codes used has been properly commented and it is available in this repo. You can simply download and study the code.

  ###### Lets connect :punch:

 [linkedin](https://www.linkedin.com/in/doyin-a-584865170)|[twitter](https://twitter.com/virgo4470)
 




