# deep-learning-bottles
Deep learning model for plastic bottles / metal cans detection

Instructions for test (on Windows):
The submission folder consists of this report, model (frozen graph) and multiple assistant scripts.
I’m not sure if you will able to run these scripts on CPU version of tensorflow as GPU option will require specific software to be added (like CUDA and cuDNN). I’ve tested it on my non-GPU version and everything was fine. Please contact me if you have any issues.
Just follow these steps to test the model:
1)	Ensure that you have tensorflow and opencv installed
2)	Drop your test images into object_detection folder (where are located some of my test images as well)
3)	It’s recommended that your images will be about the same size with your resolution (overwise you will be able to see only part of the image due to some bug). You can do it manually or use one more script to do it in automatic way (instructions will be below).
4)	Navigate to object_detection folder via cmd/anaconda etc.
5)	Open “Object_detection_image.py” with any editor
6)	In line 34 replace the value IMAGE_NAME with your picture name (keep the same format, for example ‘test_pic1.jpg’, ‘img1.jpg’ etc.).
7)	Save and run the script from console/IDEA etc.
If you need to resize all the picture at once:
1)	Create image folder in object_detection
2)	Run “resize.py” with the following parameters (from cmd for example):
python resize.py -d images/ -s 800 600
Where:
-d images/ = the created directory in the object_detection folder
-s 800 600 = outcome size of your pictures 
3)  For example, if you create folder “test_img”, fill it with images and want size to be 1024x768, the right code will be:
python resize.py -d test_img/ -s 1024 768
