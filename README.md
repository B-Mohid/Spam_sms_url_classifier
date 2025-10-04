SpamGuard AI - Client-Side Spam Classifier
SpamGuard AI is a high-performance, privacy-focused web application that classifies SMS messages and URLs as spam or safe. It utilizes two specialized deep learning models that run entirely in your browser using TensorFlow.js.

Your data never leaves your computer.

Key Features
Dual AI Models: An expert model for SMS text and another for URL structures.

100% Client-Side: All analysis happens on your device. No data is ever uploaded or stored.

Futuristic UI: A clean, responsive, and visually engaging interface.

Instant Analysis: Near-real-time classification.

Easy Deployment: Ready to be hosted on any static hosting platform like Vercel.

Project Structure
SpamGuard_AI/
│
├── 📂 models/
│   ├── sms_model.json
│   ├── sms_model.bin
│   ├── sms_word_index.json
│   ├── url_model.json
│   ├── url_model.bin
│   └── url_char_index.json
│
├── 📜 .gitignore
├── 📜 index.html
├── 📜 favicon.svg
├── 📜 README.md
└── 📜 vercel.json  <-- Configuration for Vercel

How to Deploy on Vercel (Recommended)
Prepare Your Project: Ensure your folder contains all the files provided, including the models directory with the six model files generated from the Colab notebook.

Push to GitHub: Create a new repository on GitHub and push your entire project folder to it.

Connect to Vercel:

Sign up for a free account at vercel.com.

On your Vercel dashboard, click "Add New... > Project".

Select "Continue with GitHub" and import the repository you just created.

Configure and Deploy:

Vercel will automatically detect that it is a static site.

You do not need to change any build settings. The vercel.json file will handle the configuration.

Click the "Deploy" button.

Vercel will build and deploy your site, providing you with a live URL in under a minute. Your SpamGuard AI will be live!
