# Brain-Tumor-Detection
A cutting-edge Brain Tumor Detection system leveraging Deep Learning and Convolutional Neural Networks (CNN).

Problem Statement
Detecting brain tumors is a crucial task in medical imaging with significant implications for patient outcomes. The complexity of the human brain and the variability in tumor appearance pose challenges in accurate detection. This project addresses the need for an automated and accurate brain tumor detection system to assist healthcare professionals in diagnosing brain tumors.

Project Overview
The goal of this project is to develop a robust brain tumor detection system capable of classifying brain scans as either containing a tumor or not. The system is designed to handle the variability in brain scans and deliver accurate results efficiently. Additionally, it features a user-friendly interface to make the model accessible to healthcare professionals and patients.

Key Components
Machine Learning Model:
Model: VGG16 Convolutional Neural Network (CNN)
Dataset: Brain scan images with and without tumors
Data Augmentation: Applied transformations such as rotation, flipping, scaling, and shifting to increase dataset size and variability.
Training: The VGG16 model was trained on augmented data using techniques such as dropout and regularization to prevent overfitting. The model achieved an accuracy of 99% on the test set.
Model Saving: The trained model was saved using the pickle library.

Backend API:
Frameworks: Flask and FastAPI
Functionality: Exposes REST API endpoints to accept image uploads and return predictions on whether the image contains a tumor.
Image Processing: Converts base64-encoded images to a format suitable for the model, performs preprocessing, and returns predictions as JSON.
Security: Implemented JWT-based authentication to secure access to the API.

Front-End Application:
Framework: React
Functionality: Provides a web-based interface for users to upload brain scan images and receive predictions.

Features:
User-friendly form for image upload.
Loading indicator during prediction.
Display of prediction results with accuracy percentage.
Design: Utilized React components and CSS for a clean and responsive user interface.

How It Works
Image Upload: Users upload brain scan images via the React front-end.
Image Processing: Images are converted from base64 format, resized, and preprocessed.
Prediction: The processed images are passed through the VGG16 model to generate predictions.
Results: Predictions are returned to the user via the API and displayed on the front-end.

Installation and Usage
Clone the Repository:
git clone <repository-url>

Install Dependencies:
Python packages: fastapi, uvicorn, pydantic, numpy, pandas, opencv-python, Pillow, keras, tensorflow, pyjwt, Flask
JavaScript libraries: react, axios

Run the Backend:
uvicorn app:app --reload

Run the Front-End:
npm install
npm start

Access the Application:
Backend API: http://127.0.0.1:8000
Front-End: http://localhost:3000
