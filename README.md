# Natural Frequency Calculator for FGM Sandwich Plates

Welcome to the **Natural Frequency Calculator**, a MATLAB-based Graphical User Interface (GUI) tool developed to predict the non-dimensional fundamental frequency of Functionally Graded Material (FGM) sandwich plates. This tool is designed to assist researchers and engineers in the field of material science and structural engineering by providing quick and accurate frequency predictions based on user-defined parameters.

This GUI is developed as part of a research paper and is intended to be a supplementary tool referenced within the paper. A link to this repository will be included in the publication.

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
- [Contributing](#contributing)
- [License](#license)
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
- **Visualization**: Includes graphical elements to enhance user experience.

---

## Getting Started

### Prerequisites

- **MATLAB**: Version R2018b or later is recommended.
- **MATLAB Toolboxes**:
  - **Neural Network Toolbox** (now part of the Deep Learning Toolbox)
  - **Image Processing Toolbox** (optional, for displaying images)

Ensure that these toolboxes are installed and licensed on your MATLAB environment.

### Installation

1. **Clone or Download the Repository**

   Clone the repository using Git:

   ```bash
   git clone https://github.com/yourusername/natural-frequency-calculator.git
   ```

   Or download the ZIP file and extract it to a directory of your choice.

2. **Verify File Structure**

   Ensure the following files are present in the directory:

   - `FrequencyCalculator.m` (Main MATLAB script)
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

### Launching the GUI

1. **Open MATLAB**

   Start MATLAB on your computer.

2. **Set Path**

   In MATLAB, set the current directory to the location where the files are stored.

3. **Run the Script**

   In the MATLAB Command Window, type:

   ```matlab
   FrequencyCalculator
   ```

   Press **Enter** to execute the command.

4. **GUI Window**

   The GUI will launch in a new window titled **"Natural Frequency Calculator"**.

### Input Parameters

The GUI requires eight input parameters related to the FGM sandwich plate's material properties and geometry:

1. **$$h_1/H$$**: Thickness ratio of the top layer to the total thickness.
2. **$$h_2/H$$**: Thickness ratio of the bottom layer to the total thickness.
3. **$$a/H$$**: Aspect ratio of plate length to total thickness.
4. **$$b/a$$**: Ratio of plate width to plate length.
5. **$$d/a$$**: Dimensionless parameter (related to boundary conditions or material gradation).
6. **$$p$$**: Power-law index of the FGM (material gradation exponent).
7. **$$\overline{G}_1$$**: Non-dimensional shear modulus for the top layer.
8. **$$\overline{G}_2$$**: Non-dimensional shear modulus for the bottom layer.

**Instructions**:

- Enter numeric values into each field corresponding to the parameters listed.
- Ensure all values are within the valid ranges specified in the research paper or relevant literature for accurate predictions.

### Selecting a Model

A dropdown menu labeled **"Select Model"** allows you to choose from different pre-trained neural network models:

- **Model Configurations**:
  - **A1** and **A2**: Different structural configurations or setups as defined in the research.
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

### Model Selection Guidance

- **LM (Levenberg-Marquardt)**: Generally faster convergence, suitable for smaller datasets.
- **BR (Bayesian Regularization)**: Provides better generalization, suitable for complex datasets.
- **Activation Functions**:
  - **Log-sigmoid**: Good for binary outputs and probabilities.
  - **Tan-sigmoid**: Useful when data is centered around zero.

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
  - **Solution**: Verify that all model `.mat` files are present in the same directory as `FrequencyCalculator.m`.

- **Invalid Input Values**:

  - Ensure all input fields contain numeric values.
  - Check that the values are within realistic and valid ranges.

- **GUI Display Issues**:

  - If GUI elements are misaligned or not displaying correctly, adjust your screen resolution.
  - Ensure MATLAB is not running in a scaled display mode that might affect GUI rendering.

- **MATLAB Compatibility**:

  - If encountering errors, confirm that your MATLAB version meets the minimum requirement (R2018b or later).
  - Update MATLAB and toolboxes if necessary.

---

## Contributing

Contributions to enhance the functionality or usability of the tool are welcome.

- **Fork the Repository**: Create your own fork on GitHub.
- **Create a Branch**: For new features or bug fixes.
- **Submit a Pull Request**: Describe the changes made and submit for review.

**Note**: For significant changes, please open an issue first to discuss what you would like to change.

---

## License

This project is licensed under the terms of the **MIT License**. You are free to use, modify, and distribute the software as per the license conditions.

See the [LICENSE](LICENSE) file for more details.

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
> **Journal/Conference**: [Name of the Journal or Conference], [Year], [Volume(Issue)], [Page Numbers].
>
> **DOI**: [DOI Number]


---

Thank you for using the Natural Frequency Calculator. We hope this tool enhances your research and development efforts in the field of FGM sandwich plates.

Feel free to share feedback or contribute to the project to help us improve and expand its capabilities.

---
