# Geospatial Hospital Detection

<2021>, by ISB Institute of Data Science    
Contributors: Dr. Shruti Mantri, Gokul S Kumar and Vishal Sriram     
Faculty Mentors: Dr. Manish Gangwar and Dr. Madhu Vishwanathan    
Affiliation: Indian School of Business   

GNU AGPLv3 https://choosealicense.com/licenses/agpl-3.0/
[![License: AGPL v3](https://img.shields.io/badge/License-AGPL%20v3-blue.svg)](https://www.gnu.org/licenses/agpl-3.0)
[![Coverage Status](https://coveralls.io/repos/github/geospoc/Hospital_detection/badge.svg?branch=main)](https://coveralls.io/github/geospoc/Hospital_detection?branch=main)

## Aim & Objective
To design and develop an intelligent system that identifies hospitals and healthcare facilities from satellite images.


## Steps involved
1. Collecting the names of major cities in Maharashtra.
2. Using Google Maps API to get the addresses of hospitals in these cities, including their coordinates.
3. Using Mapbox API to get the aerial images for the collected coordinates of hospital buildings.
4. Use CVAT Online to annotate these images with the help of Google Earth Pro.
5. Convert the annotations in XML files to binary masks.
6. Split the data into Urban and Rural areas, and then into train and test sets.
7. Split the train data into train and validation data and train the UNet model.
8. Use the model weights to make predictions.

Use the "requirements.txt" file to clone the environment in which the model eas developed.

## Repo contents
- **input**: The address (and coordinates) CSV's from Google Maps API, the image files from Mapbox and the respective annotation XML files from CVAT.
- **models**: The final model weights.
- **notebooks**: Jupyter notebooks used for data visualization and other purposes.
- **src**: All the python scripts associated with the project.
- **inference**: Contains the geotiff infra maps, tile numbers containing infrastructure, images used for inference & predictions in .npz and geojson format.


## FAQs

1. How to clone the repo to start developing?  
A: ```git clone https://github.com/geospoc/Hospital_detection.git```

2. How to set-up the dev environment?  
A: Use the "requirements.txt" file to clone the environment in which the model was developed.

3. How to build on the existing work?  
A: Use the model weights available [here](https://github.com/geospoc/Hospital_detection/tree/main/models) as pre-trained weights and develop new strategies to further improve the predictions.

