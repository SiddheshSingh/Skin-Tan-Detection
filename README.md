# Skin-Tan-Detection
Detection of change in Skin Tone (Tanning) of a person, irrespective of the lighting of an image

## Description
Detecting skin tone in an image has been a great problem, as every image (even of the same person) has different conditions (Camera Quality, Light Exposure, etc). This project is focused on detecting the differences in the skin tone (telling you if you've grown darker or lighter significantly). <br> 

**This can be done through extracting the Saturation value of the two images.** This value tells us the difference between the skin tones of the two images, usually irrespective of the conditions like Light Exposure etc. This is because the Light Exposure during capturing a photo effects the Brightness/Value. <br> 
*(Although the brightness of the image has some effects on the saturation, here it is considered of not having any significant effect. )*

## Procedure
1. The skin of the person from the image is isolated. This has been done by the use of skin segmentation by thresholding values. The whole background, which do not contain skin color, is turned black. K Nearest Neighbours algorithm is then used to find out the dominating colors in the image.<br> 
Details are described in : https://medium.com/datadriveninvestor/skin-segmentation-and-dominant-tone-color-extraction-fe158d24badf <br>
Code available at : https://github.com/octalpixel/Skin-Extraction-from-Image-and-Finding-Dominant-Color

2. The 1st skin tone out of top 5 is extracted. The BGR (Blue, Green, Red) code of this skin tone is converted to HSV (Hue, Saturation, Value). 

3. The Saturation (S) from the HSV code is compared between the two images. If they have significant changes, output is given describing if the second image is a result of tan or not, and by how much value. 

#### Resources
https://github.com/octalpixel/Skin-Extraction-from-Image-and-Finding-Dominant-Color <br>
https://www.w3resource.com/python-exercises/math/python-math-exercise-77.php
