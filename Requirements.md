Project Requirements
This project runs entirely on the client-side in a web browser. There are no backend dependencies to install. However, to make the application functional, you must provide the six pre-trained model and index files.

Required Model Files
These are the files generated from your model training process in Google Colab.

Part 1 (SMS Model)
sms_model.json: The architecture of the SMS classification model.

sms_model.bin: The binary weights for the SMS model.

sms_word_index.json: The word-to-index mapping for tokenizing SMS text.

Part 2 (URL Model)
url_model.json: The architecture of the URL classification model.

url_model.bin: The binary weights for the URL model.

url_char_index.json: The character-to-index mapping for tokenizing URLs.

Setup Instructions
Create a directory named models in the root of the project.

Place all six of the files listed above into this newly created models directory.

The application is specifically coded to look for these files in the ./models/ path. Without them, the website will load, but the analysis functionality will fail.