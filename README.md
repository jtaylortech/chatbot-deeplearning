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
- these succeeding steps will be completed in the `train.ipynb` file
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


