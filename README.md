# CCTV Unpaid Customer & Long-Stay Detector Prototype

This repository contains a simple prototype for a "CCTV Unpaid Customer & Long-Stay Without Order Detector" designed to be run in a Google Colab environment. The project uses computer vision to monitor a video feed, detect and track people, and flag individuals based on specific behaviors (leaving without paying, staying too long without ordering).

## Features

-   **Live Video Processing:** Analyzes a live webcam feed in real-time.
-   **Person Detection & Tracking:** Utilizes the YOLOv8 object detection model to identify and track individuals.
-   **Behavioral Flags:**
    -   **Unpaid Customer Detection:** Identifies when a tracked person crosses a designated "exit" line.
    -   **Long-Stay Detection:** Flags individuals who remain in the scene beyond a configurable time limit.
-   **Interactive GUI:**
    -   Displays the live video feed with detection boxes and tracking IDs.
    -   Shows real-time counts of "Unpaid" and "Long-Stay" customers.
    -   Allows configuration of the long-stay time threshold.
    -   Shows a prominent alert message when thresholds are breached.
-   **Colab-Ready:** Packaged as a single `.ipynb` file that handles its own dependencies and can be run instantly in Google Colab.

## How to Run

1.  **Download the Notebook:**
    Download the `cctv_prototype.ipynb` file from this repository.

2.  **Upload to Google Colab:**
    -   Go to [colab.research.google.com](https://colab.research.google.com).
    -   Click on **File > Upload notebook...**.
    -   Select the `cctv_prototype.ipynb` file you downloaded.

3.  **Run the Application:**
    -   Once the notebook is open, click the **play button** (▶️) on the left of the single code cell.
    -   The first time it runs, it will install the required Python packages. This may take a minute.
    -   Your browser will ask for permission to use your webcam. You must **allow** it for the application to work.

4.  **Interact with the GUI:**
    -   The GUI window will appear below the code cell.
    -   You can see the live feed, the counts, and any alerts.
    -   To stop the application, simply close the browser tab or interrupt the execution in Colab.

**Note:** This is a simple prototype. The "paid" and "ordered" flags are currently simulated for demonstration purposes. In a real-world application, this would be integrated with a Point-of-Sale (POS) system.
