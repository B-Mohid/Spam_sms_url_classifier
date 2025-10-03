SpamGuard AI - Client-Side Spam Classifier
SpamGuard AI is a powerful, privacy-focused web application that classifies SMS messages and URLs as spam or not spam directly in your browser. It leverages pre-trained TensorFlow.js models to perform all computations on the client side, ensuring that your data never leaves your device.

✨ Features
Dual-Mode Analysis: Classify both SMS text messages and URLs.

Client-Side Processing: All analysis happens in your browser. No data is sent to a server, guaranteeing 100% privacy.

Futuristic UI/UX: A sleek, responsive interface designed for a modern user experience.

High Accuracy: Utilizes deep learning models trained on extensive datasets for reliable predictions.

Zero Installation: Runs entirely in any modern web browser.

🚀 Project Setup
Clone the repository:

git clone <your-repo-url>
cd <repo-folder>

Add Model Files:
This project requires six specific model and index files that you have trained. Create a models directory in the root of the project and place your files inside it. The final structure should look like this:

/
|-- models/
|   |-- sms_model.json
|   |-- sms_model.bin
|   |-- sms_word_index.json
|   |-- url_model.json
|   |-- url_model.bin
|   |-- url_char_index.json
|-- index.html
|-- README.md
|-- .gitignore
|-- requirements.md

Run the Website:
You need to serve the files using a local web server because loading models via the file:// protocol is restricted by browser security policies.

If you have Python installed:

# For Python 3
python -m http.server

If you have Node.js and serve installed (npm install -g serve):

serve .

Then, open your browser and navigate to http://localhost:8000 (or the address provided by your server).

🛠️ Built With
TensorFlow.js: For running machine learning models in the browser.

Tailwind CSS: For futuristic and responsive UI design.

HTML & Vanilla JavaScript: For the core application logic.