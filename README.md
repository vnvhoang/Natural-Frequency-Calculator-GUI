# Natural Frequency Calculator for FGM Sandwich Plates

Welcome to the **Natural Frequency Calculator**, a MATLAB-based Graphical User Interface (GUI) tool developed to predict the non-dimensional fundamental frequency of Functionally Graded Material (FGM) sandwich plates. This tool is designed to assist researchers and engineers in the field of material science and structural engineering by providing quick and accurate frequency predictions based on user-defined parameters.

This GUI was developed as part of the research paper titled "Free Vibration and Nonlinear Transient Analysis of Blast-Loaded FGM Sandwich Plates with Stepped Face Sheets: Analytical and Artificial Neural Network Approaches" by Peng Shi et al. The paper provides detailed insights into the methodology and applications of the Natural Frequency Calculator.

---

## Table of Contents

- [Overview](#overview)
- [Features](#features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [Usage](#usage)
  - [Launching the GUI](#launching-the-gui)
  - [Input Parameters](#input-parameters)
  - [Selecting a Model](#selecting-a-model)
  - [Predicting the Frequency](#predicting-the-frequency)
- [Models Description](#models-description)
- [GUI Components](#gui-components)
- [Troubleshooting](#troubleshooting)
- [Authors and Acknowledgments](#authors-and-acknowledgments)
- [Contact Information](#contact-information)
- [Citation](#citation)

---

## Overview

The Natural Frequency Calculator provides an interactive platform for predicting the non-dimensional fundamental frequency of FGM sandwich plates using pre-trained neural network models. By inputting specific material and geometric parameters, users can obtain frequency predictions that aid in design and analysis tasks.

---

## Features

- **User-Friendly Interface**: An intuitive GUI designed for ease of use.
- **Multiple Pre-Trained Models**: Choose from various configurations trained using different algorithms and activation functions.
- **Real-Time Predictions**: Instant calculation and display of results upon input.
- **Customizable Inputs**: Specify a wide range of material and geometric parameters.

---

## Getting Started

### Prerequisites

- **MATLAB**: Version R2020b or later is recommended.
- **MATLAB Toolboxes**:
  - **Neural Network Toolbox** (now part of the Deep Learning Toolbox)

Ensure that these toolboxes are installed and licensed on your MATLAB environment.

### Installation

1. **Download the Repository**
 Download the ZIP file of the repository and extract its contents to a directory of your choice.

2. **Verify File Structure**

   Ensure the following files are present in the directory:

   - `FrequencyCalculator.exe`  (Main MATLAB-based GUI executable)
   - `Figure.png` (Background image for the GUI)
   - Neural network model files:
     - `A1_LM_logsig.mat`
     - `A1_LM_tansig.mat`
     - `A1_BR_logsig.mat`
     - `A1_BR_tansig.mat`
     - `A2_LM_logsig.mat`
     - `A2_LM_tansig.mat`
     - `A2_BR_logsig.mat`
     - `A2_BR_tansig.mat`

---

## Usage

### Launching the GUI**

1. **Locate the Executable**

   Navigate to the folder where **`FrequencyCalculator.exe`** is stored on your computer.

2. **Run the Executable**

   Double-click on **`FrequencyCalculator.exe`** to launch the GUI.

3. **GUI Window**

   The GUI will open in a new window titled **"Natural Frequency Calculator"**.

**Note:** Ensure that all necessary supporting files and folders are in the same directory as **`FrequencyCalculator.exe`** for the application to function correctly.

### Input Parameters

The GUI requires eight input parameters related to the FGM sandwich plate's material properties and geometry:

1. **$$h_1/H$$**: The thickness ratio of the core layer to the total thickness (Segment I).
2. **$$h_2/H$$**: The thickness ratio of the core layer to the total thickness (Segment II).
3. **$$a/H$$**: Aspect ratio of plate length to total thickness.
4. **$$b/a$$**: The ratio of the plate width to the plate length.
5. **$$d/a$$**: The ratio of the length of Segment II to the total plate length.
6. **$$p$$**: The power-law index of the FGM (material gradation exponent).
7. **$$\overline{G}_1$$**: The non-dimensional Winkler coefficient.
8. **$$\overline{G}_2$$**: The non-dimensional Pasternak shear coefficient.

**Instructions**:

- Enter numeric values into each field corresponding to the parameters listed.
- Ensure all values are within the valid ranges specified in the research paper for accurate predictions.

### Selecting a Model

A dropdown menu allows you to choose from different pre-trained neural network models:

- **Model Configurations**:
  - **A1** and **A2**: Different structural configurations as defined in the research.
- **Training Algorithms**:
  - **LM**: Levenberg-Marquardt algorithm.
  - **BR**: Bayesian Regularization algorithm.
- **Activation Functions**:
  - **Log-sigmoid** (`logsig`)
  - **Tan-sigmoid** (`tansig`)

**To Select a Model**:

- Click on the dropdown menu.
- Choose the desired model based on your analysis needs.

### Predicting the Frequency

1. **Input Completion**:

   Ensure all input fields are filled with valid numeric values and a model is selected.

2. **Predict Button**:

   - Click the **"Predict"** button located in the **Output Parameter** section.

3. **Result Display**:

   - The predicted non-dimensional fundamental frequency will be displayed next to the label **"Frequency:"**.
   - The value is presented with four decimal places precision.

---

## Models Description

The tool uses several pre-trained neural network models saved as `.mat` files. Each model is trained using specific algorithms and activation functions to cater to different analysis scenarios.

### Available Models

1. **Configuration A1**:
   - **LM Algorithm with Log-sigmoid Activation** (`A1_LM_logsig.mat`)
   - **LM Algorithm with Tan-sigmoid Activation** (`A1_LM_tansig.mat`)
   - **BR Algorithm with Log-sigmoid Activation** (`A1_BR_logsig.mat`)
   - **BR Algorithm with Tan-sigmoid Activation** (`A1_BR_tansig.mat`)

2. **Configuration A2**:
   - **LM Algorithm with Log-sigmoid Activation** (`A2_LM_logsig.mat`)
   - **LM Algorithm with Tan-sigmoid Activation** (`A2_LM_tansig.mat`)
   - **BR Algorithm with Log-sigmoid Activation** (`A2_BR_logsig.mat`)
   - **BR Algorithm with Tan-sigmoid Activation** (`A2_BR_tansig.mat`)

**Note**: Choose the model that best fits the characteristics of your specific problem or matches the conditions outlined in the research.

---

## GUI Components

The GUI is divided into several sections for ease of navigation:

1. **Left Panel**:

   - Displays an image (`Figure.png`) illustrating the FGM sandwich plate or relevant schematic.
   - Enhances visual understanding of the plate configuration.

2. **Title Bar**:

   - Shows the title **"Graphical user interface (GUI) tool for predicting non-dimensional fundamental frequency of FGM sandwich plate"**.
   - Positioned at the top center of the GUI.

3. **Input Parameters Panel**:

   - Contains labeled input fields for all required parameters.
   - Includes the model selection dropdown.

4. **Output Parameters Panel**:

   - Houses the **"Predict"** button.
   - Displays the calculated frequency result.

5. **Author Information**:

   - Located at the bottom right corner.
   - Provides developer's name, affiliation, and contact details.

---

## Troubleshooting

- **Model File Not Found**:

  - **Error Message**: "The model file [filename] does not exist. Please check the file name and path."
  - **Solution**: Verify that all model `.mat` files are present in the same directory as `FrequencyCalculator.exe`.

- **Invalid Input Values**:

  - Ensure all input fields contain numeric values.
  - Check that the values are within realistic and valid ranges.

- **GUI Display Issues**:

  - If GUI elements are misaligned or not displaying correctly, adjust your screen resolution.
  - Ensure MATLAB is not running in a scaled display mode that might affect GUI rendering.

- **MATLAB Compatibility**:

  - If encountering errors, confirm that your MATLAB version meets the minimum requirement (R2020b or later).
  - Update MATLAB and toolboxes if necessary.

---

## Authors and Acknowledgments

- **Developer**: **Vu Ngoc Viet Hoang**
- **Affiliation**: Bach Khoa Phu Tho Technology Co., Ltd, Ho Chi Minh City, Vietnam

**Acknowledgments**:

- Special thanks to all collaborators and contributors who have supported the development of this tool.
- Appreciation to the research community for valuable feedback and insights.

---

## Contact Information

For questions, suggestions, or support, please contact:

- **Email**: [vnvhoang2610@gmail.com](mailto:vnvhoang2610@gmail.com)

---

## Citation

If you find this tool useful in your research or professional work, please consider citing the associated research paper:

> **Author(s)**: Peng Shi, Vu Ngoc Viet Hoang, Jian Yang, Haoge Shou, Qi Li, Ferruh Turan
>
> **Title**: Free vibration and nonlinear transient analysis of blast-loaded FGM sandwich plates with stepped face sheets: Analytical and artificial neural network approaches
>
> **Journal**:
>
> **DOI**: 


---

Thank you for using the Natural Frequency Calculator. We hope this tool enhances your research and development efforts in the field of FGM sandwich plates.

Feel free to share feedback or contribute to the project to help us improve and expand its capabilities.

---
