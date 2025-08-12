
# CCTV Unpaid Customer & Long-Stay Detector Prototype

This repository contains a **simple prototype** for a **CCTV-based monitoring system** in food-serving hotels and shops, designed to run in **Google Colab**.
The system uses **computer vision** to monitor a video feed, detect and track people, and flag individuals who either:

* **Leave without paying**
* **Stay too long without ordering** (loitering for AC)

---

## **Features**

### 🎥 Live Video Processing

* Analyzes live webcam feed or sample video in real-time.

### 🧍 Person Detection & Tracking

* Uses **YOLOv8** object detection for identifying individuals.
* Tracks people using an ID system (SORT/DeepSORT).

### 🚨 Behavioral Flags

1. **Unpaid Customer Detection**

   * Flags when a tracked person crosses a designated **exit line** without a payment flag.
2. **Long-Stay Without Order Detection**

   * Flags people who stay in the scene **beyond a set time limit** without placing an order.

### 🖥 Interactive GUI

* Displays:

  * Live detection feed with **bounding boxes & tracking IDs**
  * **Unpaid** and **Long-Stay** customer counts
  * Configurable **thresholds** for alerts
* Shows a **red alert message** when a threshold is breached.

### ☁️ Colab-Ready

* Packaged as a single `.ipynb` file that installs all dependencies automatically.

---

## **How to Run**

### 1️⃣ Download the Notebook

Download `cctv_prototype.ipynb` from this repository.

### 2️⃣ Upload to Google Colab

* Go to **[Google Colab](https://colab.research.google.com/)**
* Click **File > Upload notebook...**
* Select `cctv_prototype.ipynb`

### 3️⃣ Run the Application

* Click the **▶️** button to run the first cell.
* The first run will install Python packages (takes \~1 min).
* Allow **webcam access** when prompted.

### 4️⃣ Interact with the GUI

* View the **live feed**, detection boxes, and counts.
* Alerts will show when limits are exceeded.
* Stop the app by **closing the browser tab** or **interrupting the kernel**.

---

## **Notes**

* This is a **prototype** — payment/order detection is **simulated** for demo purposes.
* In a real deployment, it would integrate with a **Point-of-Sale (POS) system** for accurate payment/order verification.
* Works with **sample video files** if webcam access is not available in Colab.

---

## **Tech Stack**

* **Python** (Google Colab)
* **OpenCV** (Video processing)
* **YOLOv8** (Object detection)
* **DeepSORT/SORT** (Object tracking)
* **PySimpleGUI / Tkinter** (GUI)
