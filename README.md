# Sunburst-Chart-Analyzer

SunburstChartAnalyzer is a tool for extracting hierarchical data from images of sunburst charts and representing it as a tree data structure.

## Description
Sunburst charts are a popular way to visualize hierarchical data using concentric circles and annular sectors. Manually extracting the data from sunburst chart images can be tedious.

This project aims to automate the data extraction process using computer vision and image processing techniques. Given an image, it first detects whether it contains a sunburst chart. If so, it extracts the text from the chart image and detects the hierarchical levels encoded in the chart geometry. Finally, it constructs a tree data structure representing the hierarchy and data labels from the sunburst chart.

The workflow consists of:

Chart classification - Use machine learning models like SVM and CNN to detect if the image contains a sunburst chart
Component extraction
Circle detection to find chart center
Text detection using OCR to extract labels
Text removal while retaining background
Line detection using probabilistic Hough transform to identify hierarchy levels
Hierarchical data extraction - Construct tree structure by assigning parent-child relationships based on geometry


## Installation
The project requires Python 3 and the following dependencies:

- OpenCV
- Scikit-learn 
- Matplotlib 
- Tensorflow

Install the required packages: ```$ pip install opencv-python sklearn matplotlib tensorflow $``` 

## Usage

The main script is sunburst_analyzer.py. Run it by passing the path of an image file:
