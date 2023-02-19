# Iranian car license plate recognition using YoloV7 

In this project, we want to perform license plate recognition using pre-trained YoloV7 model training on the dataset of cars with Iranian and foreign license plates.
Then, using the trained model and OCR, we recognize the license plate and the text in it in three modes: photo, video and webcam.

## Table of Contents

- [Iranian car license plate recognition using YoloV7](#iranian-car-license-plate-recognition-using-yolov7)
- [Table of Contents](#table-of-contents)
- [How To Run](#how-to-run)
  - [Install Requirements](#install-requirements)
  - [Run Code](#run-code)
- [Results](#results)
- [License](#license)
- [Contact](#contact)

## How To Run

### Install Requirements

- In the first step, to train the model on Google Colb, follow the steps below:
1. Mount Google Drive
```
from google.colab import drive
drive.mount('/content/gdrive')
```
2. Clone the yolov7 github
```
!git clone https://github.com/augmentedstartups/yolov7.git
```
3. Go to the project directory
4. Install requirements by running
```
!pip install -r requirements.txt
!pip install roboflow
```

- In the second step, to run the Yolov7_IRPD_OCR.py script in order to identify the license plate and its text, do the following steps.
1. It is suggested to create a conda environment. `conda create -n [your-env-name] python=3.8`
2. Clone the yolov7 github
```
!git clone https://github.com/augmentedstartups/yolov7.git
```
3. Go to the project directory
4. Install requirements by running
```
!pip install -r requirements.txt
!pip install easyocr
!pip install deep-sort-realtime
```

### Run Code

- To train the pre-trained YoloV7 model on the new dataset, run the Yolov7_IRPD_Train.ipynb notebook cells in order.

- To recognize the license plate and its text and numbers, run the Yolov7_IRPD_OCR.py script. To choose license plate recognition from the content of photo or video or webcam, uncomment the corresponding lines of code at the end of the script.

*Please read the file in the report folder before running the codes in order to learn how to set the path of the files and variables.*

## Results

1. The result of detecting an Iranian car license plate with a high confidence score:

![377_jpg rf 896dc281783d7ffee182c64bf0522fb0](https://user-images.githubusercontent.com/112625556/219901873-967bbc88-2f74-4fdb-af5d-8bb287b681e2.jpg)

2. The result of license plate detection along with its text identification:

![detected_plate](https://user-images.githubusercontent.com/112625556/219901883-aaf91592-3f70-470e-87a1-57abace7a746.png)

- The easyocr method used to recognize Persian text and number has a little error.

## License

This project is licensed under the MIT License.

## Contact

If you have any questions about the implementation of the project, you can send your questions to this email: alrzbqr@gmail.com
