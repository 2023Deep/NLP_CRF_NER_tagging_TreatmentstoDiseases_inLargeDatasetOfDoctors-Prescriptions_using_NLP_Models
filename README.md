# Context

"BeHealthy" is a health-tech company and has a web platform that allows doctors to list their services and manage patient interactions and provides services for patients such as booking interactions with doctors and ordering medicines online. Here, doctors can easily organise appointments, track past medical records and provide e-prescriptions. So, companies like "BeHealthy" are providing medical services, prescriptions and online consultations and generating huge data day by day.

- The following snippet of medical data may be generated when a doctor is writing notes to his/her patient or as a review of a therapy that he or she has done. "The patient was a 62-year-old man with squamous cell lung cancer, which was first successfully treated by a combination of radiation therapy and chemotherapy."

- As we can see in this text, a person with a non-medical background cannot understand the various medical terms. We have taken a simple sentence from a medical data set to understand the problem and where one can understand the terms 'cancer' and 'chemotherapy'.


# Problem Statement

We have been given such a data set in which a lot of text is written related to the medical domain. There are a lot of diseases that can be mentioned in the entire dataset and their related treatments are also mentioned implicitly in the text, which we saw in the aforementioned example that the disease mentioned is cancer and its treatment can be identified as chemotherapy using the sentence. However, note that it is not explicitly mentioned in the dataset about the diseases and their treatment, but we can build an algorithm to map the diseases and their respective treatment.

- The train dataset is used to train the Continuous Random Field (CRF) model, and the test dataset is used to evaluate the built model.

# Steps
- Workspace Set Up: Import and Install Useful Packages
-- Installing Necessary Libraries
- Data Preprocessing
    - Construct the proper sentences from individual words and print the 5 sentences.
    - Count the number of sentences in the processed train and test dataset.
    - Count the number of lines of labels in the processed train and test dataset.
- Concept Identification
    - Extract those tokens which have NOUN or PROPN as their PoS tag and find their frequency
    - Print the top 25 most common tokens with NOUN or PROPN PoS tags
    - Defining features for CRF
- Getting the features
    - Write a code/function to get the features for a sentence
    - Write a code/function to get the labels of a sentence
- Define input and target variables
    - Define the features' values for each sentence as input variable for CRF model in test and the train dataset
    - Define the labels as the target variable for test and the train dataset
- Build the CRF Model
- Evaluation
    - Calculate the f1 score using the actual labels and the predicted labels of the test dataset
- Identifying Diseases and Treatments using Custom NER
    - Create the logic to get all the predicted treatments (T) labels corresponding to each disease (D) label in the test dataset.
    - Predict the treatment for the disease name: 'hereditary retinoblastoma'
