# CNN and YOLO Demo Notebooks

## Setup Instructions

### 1. Create Virtual Environment

First, create a virtual environment using the requirements file:

```bash
python -m venv venv
```

### 2. Activate the Environment

**On Windows:**
```bash
venv\Scripts\activate
```

**On macOS/Linux:**
```bash
source venv/bin/activate
```

### 3. Install Requirements

```bash
pip install -r requirements.txt
```

### 4. Select Kernel and Start Jupyter Server

1. **Select the kernel** in your Jupyter notebook
2. Press **Ctrl + Shift + P** (or **Cmd + Shift + P** on macOS) to open the command palette
3. Search for **"Jupyter: Select Interpreter"**
4. Click on it and select the virtual environment you just created as the interpreter
5. This will start the Jupyter server with the correct environment

## Dataset Format Requirements

### CNN Classification (`cnn_demo.ipynb`)

Your dataset must be organized in the following structure:

```
datafolder/
├── train/
│   └── [image files]
├── test/
│   └── [image files]
└── val/          (optional)
    └── [image files]
```

Additionally, you need CSV files with labels:
- `train.csv` - Contains image filenames and their corresponding class labels
- `test.csv` - Contains image filenames and their corresponding class labels
- `val.csv` - (Optional) Contains image filenames and their corresponding class labels

**CSV Format Example:**
```csv
image_name,label
image1.jpg,class1
image2.jpg,class2
```

**Note:** If your data is not in this format, you can create a Python script to reorganize your dataset into the required structure and generate the necessary CSV files.

### YOLO Object Detection (`yolo_demo.ipynb`)

For the YOLO demo, please check the dataset format restrictions and requirements in the link provided in the notebook. The notebook references the [Ultralytics Object Detection Datasets Documentation](https://docs.ultralytics.com/datasets/detect/#ultralytics-ndjson-format) for supported formats like YOLO and NDJSON.

## Important Notes

**Run cells in order**: Make sure to execute each cell in the notebooks sequentially from top to bottom. Running cells out of order may result in undeclared or missing variable errors, as later cells depend on variables and functions defined in earlier cells.

