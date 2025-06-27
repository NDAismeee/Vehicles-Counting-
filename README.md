# Vehicles-Counting-
Counting Vehicles for 360 Air Pollution Project


# Vehicle Counting with YOLO

This project uses a YOLO-based object detection model to count vehicles crossing user-defined lines in a video. The pipeline extracts frames, detects and tracks vehicles, and logs their crossings into a CSV file.

---

## Folder Structure

```
project_root/
├── src/
│   ├── yolo_counting.py
│   ├── vehicle-counting.ipynb
│   ├── run/                  # Put your input videos here
│   ├── output/               # CSV results will be saved here
│   └── ... (other scripts and utils)
└── report & slides
```

---

## Quick Start

### 1. Navigate to the `src` folder
```bash
cd src
```

### 2. Run the demo
Install dependencies and run the demo video:
```bash
pip install -r requirements.txt
python3 yolo_counting.py
```

---

## ▶Run Your Own Video

### Step 1: Prepare your video
Put your `.mp4` video inside the `src/run/` folder.

### Step 2: Create your own line set
Open `vehicle-counting.ipynb` to display the first frame of your video and define the lines like this:

```python
x1_start_line = 420
y1_start_line = 132
x1_end_line   = 802
y1_end_line   = 172

x2_start_line = 496
y2_start_line = 699
x2_end_line   = 813
y2_end_line   = 239

x3_start_line = False   # If not using this line
# y3_start_line = 207
# x3_end_line   = 516
# y3_end_line   = 97

x4_start_line = False   # If not using this line
# y4_start_line = 300
# x4_end_line   = 40
# y4_end_line   = 467
```

> **Note:** Set `xn_start_line = False` if you don't want to use that line.

### Step 3: Edit `yolo_counting.py`
Open `yolo_counting.py` and replace the existing demo line coordinates with your own.

### Step 4: Run the script
```bash
python3 yolo_counting.py
```

### Step 5: Check the output
The vehicle count results will be saved as a `.csv` file inside the `src/output/` folder.
