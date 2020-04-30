# Text-Recognition-by-Reading-RCs
Detects and puts a bounding box around the text using EAST Text Detector and extracts it using Tesseract OCR.

# Requirement
1. Python 
2. OpenCV 3.4.2 or better is required
3. Tesseract v4

# Description
1. Performs text detection using OpenCV’s EAST text detector, a highly accurate deep learning text detector used to detect text in natural scene images.
2. Once we have detected the text regions with OpenCV, we’ll then extract each of the text ROIs and pass them into Tesseract, enabling us to build an entire OpenCV OCR pipeline.


      ![OpenCV OCR pipeline](https://github.com/goyalmayank522/Text-Recognition-by-Reading-RCs/blob/master/img.png)


### EAST Text Detector:
We call the algorithm “EAST” because it’s an: Efficient and Accurate Scene Text detection pipeline. The EAST pipeline is capable of predicting words and lines of text at arbitrary orientations on 720p images, and furthermore, can run at 13 FPS, according to the authors.

It detect the presence of text in an image. The EAST text detector will give us the bounding box (x, y)-coordinates of text ROIs.

### Tesseract OCR:
Tesseract, a highly popular OCR engine, was originally developed by Hewlett Packard in the 1980s and was then open-sourced in 2005. Google adopted the project in 2006 and has been sponsoring it ever since.

We’ll extract each of these ROIs and then pass them into Tesseract v4’s LSTM deep learning text recognition algorithm. The output of the LSTM will give us our actual OCR results. Finally, we’ll draw the OpenCV OCR results on our output image.
