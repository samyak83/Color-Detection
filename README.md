# Color-Detection
Color recognition from an image by doubleclick on any point.

# Dataset
Colors are made up of 3 primary colors; red, green, and blue.In computers, we define each color value within a range of 0 to 255.The colors.csv file includes 865 color names along with their RGB and hex values.

# Prerequisites
Before starting with this Python project with source code, you should be familiar with the computer vision library of Python that is OpenCV and Pandas.

OpenCV, Pandas, and numpy are the Python packages that are necessary for this project in Python. To install them, simply run this pip command in your terminal:

[pip install opencv-python numpy pandas]

# Steps for Building a Project in Python – Color Detection
# 1. Download and unzip the zip file
The project folder contains 3 files:

1)Color_detection.py – main source code of our project.   
2)Col.jpg – sample image for experimenting.   
3)Colors.csv – a file that contains our dataset.

# 2. Taking an image from the user
We are using argparse library to create an argument parser. We can directly give an image path from the command prompt:   
      
import argparse   
ap = argparse.ArgumentParser()    
ap.add_argument('-i', '--image', required=True, help="Image Path")    
args = vars(ap.parse_args())    
img_path = args['image']    
#Reading image with opencv    
img = cv2.imread(img_path)    

# 3. Next, we read the CSV file with pandas
The pandas library is very useful when we need to perform various operations on data files like CSV. pd.read_csv() reads the CSV file and loads it into the pandas DataFrame. We have assigned each column with a name for easy accessing.

#Reading csv file with pandas and giving names to each column   
index=["color","color_name","hex","R","G","B"]  
csv = pd.read_csv('colors.csv', names=index, header=None) 
