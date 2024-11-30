# Fire Detection: Deep Learning Model for Forest Fire Detection

This project provides a deep learning-based solution to detect fire in forests. It combines advanced model training and Azure Machine Learning Studio features to enhance the overall workflow and experiment tracking.

---

## 📌 Project Overview

This project is divided into two key parts:

1. **Fire Detection Model**  
   A robust deep learning model is designed to detect fire flames in aerial images. Detailed information, including the methodology and results, can be found in the `project_report.pdf` file included in this repository.

2. **Azure Machine Learning Integration**  
   Leverage your local machine as a compute runtime for Azure Machine Learning Studio to access experiment tracking, logging, and collaboration features at no additional cost. This setup bridges local development with cloud-based experimentation benefits.

---

## 🌐 Using Azure Machine Learning Studio for Experiment Tracking (For Free!)

Azure Machine Learning Studio provides a convenient way to track experiments. While tools like MLflow are an option, Azure ML simplifies collaboration and scalability without the need for deploying additional infrastructure.

### Prerequisites
To follow along, ensure you have:
- An Azure ML Studio subscription (a free tier works perfectly).
- A resource group, a storage account, and Azure ML Studio workspace set up.

### Dataset and Code

The dataset used for this project is sourced from the [IEEE Dataport](https://ieee-dataport.org/open-access/flame-dataset-aerial-imagery-pile-burn-detection-using-drones-uavs). You can access it for free by creating an IEEE account.

#### Dataset Details
This project utilizes items **7**, **8**, **9**, and **10** from the dataset. Specifically:
- Items 7 and 8 are used for the "Fire_vs_NoFire" image classification task.

**Dataset Setup:**
- Download item [7](https://ieee-dataport.org/open-access/aerial-images-pile-fire-detection-using-drones-uavs) for training and unzip it into the following directory structure:
    ```
    Repository/frames/Training
                        ├── Fire/*.jpg
                        ├── No_Fire/*.jpg
    ```
- Download item [8](https://ieee-dataport.org/open-access/aerial-images-pile-fire-detection-using-drones-uavs) for testing and unzip it into:
    ```
    Repository/frames/Test
                        ├── Fire/*.jpg
                        ├── No_Fire/*.jpg
    ```

---

## 🚀 Running the Project

### Training Phase
To initiate training:
1. Set the mode to **Training** in the `config.py` file:
   ```python
   Mode = 'Training'
2. Run the "azureml_run_dl_repro_expiriment.py" training script to start the model training process.

### Testing Phase
To test the trained model:
1. Use the test_classification.ipynb notebook.
2. Ensure the test dataset is in the correct directory structure as mentioned above.

---

## 🔗 Integrating Azure Machine Learning Studio 
To use Azure ML Studio features with your local machine as the compute instance:
1. Download the configuration JSON file from Azure ML Studio (found under the workspace's essential overview section).
2. Replace the existing config.json file in this repository with the downloaded JSON.
3. Once configured, you can seamlessly run experiments and jobs on Azure ML Studio while utilizing your local machine. 

---

## 📝 Additional Resources
For detailed explanations of the deep learning model, Azure ML integration, and experiment tracking, refer to:
* project_report.pdf for in-depth model details.
* Azure ML Studio documentation for workspace setup and usage.

---

This version ensures better readability and compatibility for Markdown rendering. Let me know if you need further tweaks!
