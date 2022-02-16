## Deep Learning Based Chat Bot
Developing an intelligent chatbot using deep learning with Keras. 

## Steps to Follow
### Establish the Required Packages
- see `requirements.txt` file
- install the dependencies 
    - run `pip install -r requirements.txt`

### Define Intents
- these intents are created to to establish context during a conversation
- create `intents.json` file

### Data Prep
- these succeeding steps will be completed in the `train.ipynb` file -> everything is successfully ran in the `train-kg.ipynb` file
    - import all the required packages
    - load the json file and extract necessary data
        - the `training_sentences` variable is what holds the training data -> the sample messages is the intent categories
        -the `training_labels` variable holds the target labels that correspond with the training data
    - create the "LabelEncoder()" function to convert the target labels into an understandable model form
    - create `tokenizer` class to vectorize the data corpus 
        - using this class for the pre-processing tasks removes the punctuations and splits the words into lists of tokens
        - the tokens are then indexed or vectorized
        - the `oov_token` attribute is used to deal with out of vocabulary tokens
    - the  `padded_sequences ` method is to make the training text sequences the same size

### Model Training
- used `Sequential` class from __Keras__ to define the Neural Network architecture for the proposed model
- used the `fit` method to train the model
- saved the required files to use at inference time

### Inference
- implementing a chat function to communicate with users
- __How This Works?__
    - upon receiving a new message, the chat bot calculates the similarity between the new text sequence and the training data
    - with the confidence scores from each category, the model categorizes the user's message to an intent with the correlating highest confidence score
- this is all laid out in the `chat.py` file