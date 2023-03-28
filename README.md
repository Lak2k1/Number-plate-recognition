# Number-plate-recognition
Recognise the number plate in a frame, and write the numbers of the number plate.

First we develop a model which detects number plates from an image. For that we use kaggle dataset with annotations. For the object detection we use the Tensorflow Objection Detection API, and the Tensorflow Model Zoo since they are all brilliantly trained for the purpose.

##Librares and Tools Used-
* Os
* Tensorflow Objection Detecion API and the model from TFOD Model Zoo
* cv2(open-CV)
* numpy 
* matplotlib (for visualization)
* easyocr (for optical character recognition)
* And other libraries for other small purposes

## So first we try to detect number plate in an image, using Tensorlfow Object Detection API.
I used a kaggle dataset for number plate images and their respective annotations. Trained the model on that dataset. The model was telling us about the number only if it was more than 80% sure about it.
![](https://github.com/Lak2k1/Number-plate-recognition/blob/main/1.gif)

## We then proceed to get the numbers on the number plate 
After recognising the number plate, the task at hand was to get the text from number plate. We considered the larger text because the smallers text on a number often describes the state of country, which is of no use for the data extraction. So we extracted the text on the plate which covers about 60-70% of the number plate and got the results.
You may notice that the webcam window froze, that was because during character recognition from the number plate, I used EasyOCR which uses PyTorch and I had already been running my Tensorflow Object Detection Model, my computer's GPU wasn't powerful enough to be running both these models side-by-side but the results were fine accordingly.
![](https://github.com/Lak2k1/Number-plate-recognition/blob/main/2.gif)
