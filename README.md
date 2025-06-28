
# Optimized Deep Learning for Early Grapevine Esca Detection: Performance and Efficiency at Constrained Resolutions

## Project Overview

This project develops and evaluates advanced deep learning models for the early detection of Esca disease in grapevine leaves. Focusing on low-resolution imagery (80x45 pixels), which is ideal for deployment on cost-effective, resource-constrained edge devices, this work addresses the significant overfitting challenges observed in simpler models. We compare the performance and efficiency of a Baseline Simple CNN, ResNet50, and MobileNetV2 to identify optimal solutions for practical agricultural applications.

## Live Demo

Experience the application live here: [**https://escadiseasedetection.streamlit.app/**]

## Features

* **Image Upload:** Easily upload grapevine leaf images for analysis.
* **Model Selection:** Choose between ResNet50 and MobileNetV2 for classification.
* **Real-time Prediction:** Get instant classification results (Healthy/Esca Diseased) with confidence scores.
* **Optimized for Low Resolution:** Models are trained and evaluated on 80x45 pixel images, suitable for embedded systems.

## Key Findings & Contributions

* **Mitigation of Overfitting:** Our ResNet50 model significantly reduced the training-testing accuracy gap (from ~3.11% in baseline to ~0.32%), demonstrating superior generalization capabilities at low resolutions.
* **Comparative Performance Analysis:**
    * **ResNet50:** Achieved a test accuracy of **0.9680**, offering high diagnostic reliability and robust generalization.
    * **MobileNetV2:** Provided a compelling balance with a test accuracy of **0.9298**, coupled with significantly enhanced computational efficiency (smaller model size, faster inference time).
* **Efficiency for Edge Deployment:** MobileNetV2 was found to be approximately **[1.35] times faster** for inference compared to ResNet50 and considerably smaller, making it highly suitable for real-time applications on constrained hardware.
* **Comprehensive Evaluation:** Utilized detailed metrics including Precision, Recall, F1-score, and Confusion Matrices to provide a nuanced understanding of model performance.

## Technologies Used

* **Python:** Programming Language
* **TensorFlow / Keras:** Deep Learning Framework
* **Streamlit:** Web Application Framework
* **NumPy:** Numerical Computing
* **Pillow (PIL):** Image Processing
* **Git / GitHub:** Version Control & Repository Hosting

## Getting Started (Local Setup)

To run this application locally, follow these steps:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/itsaimankhan/Esca_Disease_Detection_App.git
    cd Esca_Disease_Detection
    ```

2.  **Create a virtual environment (recommended):**
    ```bash
    python -m venv venv
    source venv/bin/activate # On Windows: .\venv\Scripts\activate
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Download Trained Models:**
    * The model files (`esca_resnet_model.h5`, `esca_mobilenet_model.h5`) should be in the root directory. If they are hosted via Git LFS or external links (e.g., Google Drive), you might need to download them manually if Git LFS isn't configured or if they exceed GitHub's direct file size limits.
    * *(If using Git LFS, ensure Git LFS is installed and `git lfs pull` is run after cloning).*

5.  **Run the Streamlit app:**
    ```bash
    streamlit run app.py
    ```
    The app will open in your web browser.
