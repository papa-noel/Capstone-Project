# Capstone-Project

## Project Background

Our overall goal was to train a machine learning model to be able to identify SDG&E (San Diego Gas and Electric) electrical equipment from google street view images. I used the DETR image detection model and "fine tuned" it to be able to detect SDG&E power poles and power boxes that you would normally find out in town. This was the goal of our Quarter 1 project that is part of a larger problem that SDG&E tackles daily. That problem involves the upkeep of these poles and boxes so that they are always in adequate condition as to not be the cause of damage to property or even death. The main cause of the worst wildfire in California history was due to powerlines.

## How to use this Repo

### Files in the Repo
The training, validation, and test images (along with their annotations) for the model are stored in the annotations_and_images folder. Annotations refer to the images but they are overlayed with labels identifying the SDG&E equipment. This labeling will allow the training of the model. The annotations are stored as COCO json files, which are the most appropriate for this type of data.

The stand alone file in the repo is the actual notebook, created in google colab. You will be using this notebook to run everything.

### Running the Notebook
To view the project in full action, all you will have to do is run the notebook. Make sure to open the notebook in google colab, so that the proper files and GPU can be used.

The first cell in the notebook will download the necessary training, validation, and test images and annotation files onto the colab notebook from this github repo. There are no scripts that you need to run or anything special to do. All you simply need to do is run the cells to view the training and testing of the model.

The DETR model that I will be fine tuning and using can be found here, in another REPO on my github: (https://github.com/papa-noel/detr.git). If you would like more information on what DETR is/does, you can view this repo to get a better idea. In the repo, you can find helpful explanations and links that can help you wrap your head around how it all works. It honestly can get a bit confusing, but the gist of DETR is image detection/classification. To utlize DETR for your own tasks, you simply need to fine tune it. Instructions to fine tune can also be found on the repo.

The actual training of the model will take some time, about ~18 minutes or so.

Afterwards, there are cells that generate graphs that will show you statistics of the training and validation results.

At the end of the notebook, you can run the model on different images. A quick note: a "NameError" appears with two cells, but I do not know why. Nonetheless, running the cells still works. 

There are commented out lines that can be used to run the model on different images. Here an example: 
```
#img_name = '/content/Capstone-Project/annotations_and_images/images/validation_images/D150379_5_1.png'
```
Uncomment only one `img_name` at once to see how the model does on these images.
