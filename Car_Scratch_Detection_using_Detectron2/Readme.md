**Car Scratch Detection Using Detectron2**

This repository contains a car scratch detection project using Detectron2, a state-of-the-art object detection library. The project focuses on identifying and classifying scratches and dents on car parts.

**Project Overview**

The goal of this project is to detect and classify different types of car damages such as scratches and dents. The model is trained using Detectron2, which leverages a deep learning approach for object detection tasks.

**Features**

- Detection and Classification: Identify and classify various types of scratches and dents on car parts.
- Dataset: Custom dataset with annotations for detecting and classifying damages.
- Evaluation Metrics: Model performance is evaluated using standard COCO metrics.

**Dataset**

The project uses a custom dataset formatted in COCO style with the following categories:
- Minor Dent
- Minor Scratch
- Moderate Dent
- Moderate Scratch
- Severe Dent
- Severe Scratch
- Severe Broken
- Moderate Broken
- Severity Damage

**Installation**

1. Clone the repository:

   ```
   git clone https://github.com/yourusername/car-scratch-detection.git
   cd car-scratch-detection
   ```

2. Set up the environment:

   - Create a virtual environment (optional but recommended):

     ```
     python -m venv detectron2-env
     source detectron2-env/bin/activate  # On Windows use detectron2-env\Scripts\activate
     ```

   - Install the required packages:

     ```
     pip install -r requirements.txt
     ```

   - Install Detectron2. Follow the instructions in the Detectron2 installation guide: https://detectron2.readthedocs.io/en/latest/tutorial.html#install-detectron2.

**Usage**

1. Prepare the Dataset:

   - Ensure your dataset is formatted according to COCO standards.
   - Place your dataset and annotations in the appropriate directory.

2. Train the Model:

   - Configure your training parameters in `config.yaml`.
   - Run the training script:

     ```
     python train_model.py
     ```

3. Evaluate the Model:

   - Use the provided evaluation script to test your model on a validation set:

     ```
     python evaluate_model.py
     ```

4. Run Inference:

   - Use the inference script to make predictions on new images:

     ```
     python infer_model.py --image_path /path/to/image.jpg
     ```

**Results**

The model's performance is evaluated using the COCO metrics, including Average Precision (AP) and Average Recall (AR) across different categories.

**Contributing**

Contributions are welcome! Please fork the repository, make changes, and create a pull request.

**Contact**

For questions or comments, please reach out to manishgadhave1072@gmail.com.

