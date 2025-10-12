SpamClassifier AI: Client-Side SMS & URL Classifier
A privacy-focused, AI-powered web application that detects spam in SMS messages and malicious URLs directly in your browser. No data ever leaves your device.

Live Demo: https://spam-sms-url-classifier.vercel.app/ 

🚀 Key Features
100% Client-Side: All AI model inference happens locally in the user's browser using TensorFlow.js.

Privacy Guaranteed: No text, URLs, or user data is ever sent to a server.

Dual-Model System:

SMS Model: A specialized model trained on word-level analysis to understand the nuances of text-based spam.

URL Model: A second model trained on character-level analysis to identify patterns in malicious links.

No Backend Required: A completely static application that can be hosted for free on platforms like Vercel or Netlify.

Futuristic & Responsive UI: A sleek, modern interface built with Tailwind CSS that works beautifully on both desktop and mobile devices.

🛠️ Technology Stack
Frontend:

HTML5

CSS3 with Tailwind CSS (via CDN)

Vanilla JavaScript

Machine Learning (In-Browser):

TensorFlow.js: To build and run the deep learning models.

NPY.js: A lightweight library to parse the raw model weights exported from Python.

Model Training (Google Colab):

Python

TensorFlow / Keras: For building and training the original models.

Pandas & Scikit-learn: For data preprocessing.

NumPy: For exporting the raw model weights to .npy files.

📁 Project Structure
The project is designed for simplicity and easy deployment.

/
├── 📂 models/
│   ├── embedding_sms_0.npy
│   ├── dense_1_sms_0.npy
│   ├── ... (and all other raw .npy weight files)
│   ├── sms_word_index.json
│   └── url_char_index.json
│
├── 📜 index.html        # The entire application logic, UI, and styling
├── 📜 favicon.svg         # The website icon
├── 📜 license.md
└── 📜 README.md         # You are here!

🧠 The AI Models
The core of this project is its two specialized AI models. They were trained in a Google Colab environment using TensorFlow/Keras.

SMS Spam Model: Trained on the spam.csv dataset. It uses a word-level tokenizer and an Embedding layer to learn the relationships between words commonly found in spam messages.

URL Spam Model: Trained on the spaml.csv dataset. It uses a character-level tokenizer, which is more effective for URLs, as malicious links often rely on subtle character patterns and substitutions rather than whole words.

To overcome significant challenges with TensorFlow.js converters, the final, robust solution involves exporting the raw weights for each model layer as individual .npy files. The index.html file then reconstructs the model architecture in JavaScript and manually loads these weights, ensuring perfect compatibility and performance.

⚙️ Getting Started
To run this project locally, follow these steps:

Clone the repository:

git clone [https://github.com/B-Mohid/spam_sms_url_classifier.git](https://github.com/B-Mohid/spam_sms_url_classifier.git)
cd spam_sms_url_classifier

Generate the Model Files:

Open the Dual Spam Model Training (NPY Exporter).ipynb notebook in Google Colab.

Upload the spam.csv and spaml.csv datasets when prompted.

Run all the cells in the notebook. This will train the models and download a models.zip file.

Place the Models:

Unzip the models.zip file.

Place the resulting models folder (containing all the .npy and .json files) into the root of your project directory.

Run Locally:

You cannot simply open index.html from the file system due to browser security policies (CORS). You must serve it using a local web server.

If you have Python installed, the easiest way is:

python -m http.server

Then, open your browser and go to http://localhost:8000.

🚀 Deployment
This application is fully static and can be deployed for free on services like Vercel or Netlify in under a minute.

Push your project code (including the models folder) to a GitHub repository.

Sign up for Vercel or Netlify and connect your GitHub account.

Import your repository.

No build settings are required. Just click "Deploy". Your site will be live!

📄 License
This project is licensed under the MIT License. See the LICENSE file for details.
