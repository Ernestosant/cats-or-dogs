# Cat to Dog Replacer 🐱➡️🐶

This repository provides a solution to a coding challenge that involves detecting and replacing cats in images with dogs using deep learning models. The project is implemented in a Jupyter Notebook and includes a user-friendly interface built with Gradio.

## 📁 Repository Structure

```
├── test_image/
│   ├── gato.PNG
│   └── perro.PNG
├── CatToDog_Replacer.ipynb
├── requirements.txt
└── README.md
```

- **test_image/**: Contains sample images for testing.
- **CatToDog_Replacer.ipynb**: Jupyter Notebook with the complete solution.
- **requirements.txt**: Lists all necessary dependencies.
- **README.md**: Project overview and instructions.

## Try it on Google Colab

You can run the notebook directly on Google Colab by clicking the link below:

[![Open in Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1EPnq2HRHx-8MMMiB66ntB29tLxEykC8L?usp=sharing)

This will allow you to try the code without any local setup required.


## 🚀 Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/your_username/CatToDog_Replacer.git
   cd CatToDog_Replacer
   ```

2. **Create a virtual environment (optional but recommended):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Open the Jupyter Notebook:**
   ```bash
   jupyter notebook CatToDog_Replacer.ipynb
   ```

## 🛠️ Usage

The pipeline performs the following steps:

1. **Object Detection:** Uses **YOLOv5** to detect and locate cats in an image.
2. **Segmentation:**
   - **Mask R-CNN** for precise cat segmentation.
   - **DeepLabV3** for segmenting dogs.
3. **Image Manipulation:** Removes the detected cat using inpainting and replaces it with the segmented dog.
4. **End-to-End Pipeline:** Combines all steps into a seamless process.

### Gradio Interface

A Gradio interface is provided for easy interaction:

1. **Launch the Interface:**
   Run the last cell in the notebook to start Gradio.

2. **Upload Images:**
   - **Cat Image:** Upload the image containing the cat.
   - **Dog Image:** Upload the dog image to replace the cat.

3. **Replace Cat with Dog:**
   Click the "Replace Cat with Dog" button to process.

4. **View Results:**
   The interface displays the final image with the dog replacing the cat and the original image with detected cats highlighted.

## 💡 Solution Overview

- **YOLOv5:** Selected for its high performance in detecting cats.
- **Mask R-CNN:** Chosen for accurate cat segmentation.
- **DeepLabV3:** Utilized for effective dog segmentation.
- **OpenCV:** Used for inpainting to remove the cat from the image.
- **Gradio:** Provides an intuitive web interface for users to interact with the pipeline.

## 🏆 Coding Challenges Addressed

1. **Object Detection:** Detect and locate cats using a pre-trained YOLOv5 model.
2. **Image Manipulation:** Replace detected cats with predefined dog images.
3. **End-to-End Pipeline:** Integrate detection and replacement into a cohesive workflow.
