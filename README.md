# LeafPredict - Plant Disease Detection

## Overview

LeafPredict is a web application built with Django that uses a machine learning model to identify plant diseases from uploaded images of leaves. It currently supports the detection of diseases in pepper, potato, and tomato plants.

## Features

* **Image Upload:** Users can upload images of plant leaves through a simple web interface.
* **Disease Prediction:** The application uses a pre-trained Keras model to predict potential diseases affecting the plant.
* **Detailed Information:** After prediction, the application provides details about the identified diseases, sourced from a JSON file.
* **Multiple Disease Support:** The application can identify multiple diseases present in a single image.

## Technologies Used

* **Django:** A high-level Python web framework.
* **OpenCV:** A library of programming functions mainly aimed at real-time computer vision.
* **Keras:** A high-level neural networks API, capable of running on top of TensorFlow.
* **TensorFlow:** An open-source machine learning framework.
* **NumPy:** A library for numerical computing in Python.

## Setup and Installation

1. **Clone the repository:**

   ```bash
   git clone [repository_url]
   cd LeafPredict_Plant_Disease_Detection
   ```
2. **Create a virtual environment:**

   ```bash
   python -m venv .venv
   ```
3. **Activate the virtual environment:**

   ```bash
   .venv\Scripts\activate  # On Windows
   source .venv/bin/activate # On macOS and Linux
   ```
4. **Install the dependencies:**

   ```bash
   pip install -r requirements.txt
   ```
5. **Apply migrations:**

   ```bash
   python manage.py migrate
   ```
6. **Load static assets:**

   ```bash
   python manage.py collectstatic
   ```
7. **Run the development server:**

   ```bash
   python manage.py runserver
   ```

   Open your web browser and navigate to `http://localhost:8000/` to access the application.

## Project Structure

* `myapp/`: Contains the Django app with the core logic.
  * `views.py`: Handles the web application's logic, including image processing and disease prediction.
  * `models.py`: Defines the data models for the application.
  * `templates/`: Stores the HTML templates for the web pages.
* `media/`: Stores uploaded images and model data.
  * `model_data/`: Contains the pre-trained machine learning model (`plant_leaf_diseases_model.h5`) and disease details (`plant_diseases_details.json`).
* `static/`: Contains static files such as CSS and JavaScript.
* `requirements.txt`: Lists the Python packages required to run the application.
* `manage.py`: A Django command-line utility for administrative tasks.

## Usage

1. Navigate to the home page (`/`) to upload an image for disease prediction.
2. Upload an image of a plant leaf.
3. The application will display the predicted diseases and their details.

## Contributing

Contributions are welcome! Please feel free to submit pull requests or open issues to suggest improvements or report bugs.

## License

[Choose a license and add it here]
