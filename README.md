# Automatic-Tinder

## Problems
- Communicating With Android
- Controlling Device Programmatically
- Capturing The Images
- Detecting Person Within That Image
- Classifying The Image
- Making Decisions

### Communicating With Android

I just have one word i.e ADB. For anyone who are wondering what the hell on earth is adb , relax I got your back. ADB stands for Android Debug Bridge which is mostly used by (as you have guessed it YES!) programmers or developers. It lets you establish a tcp connection via USB or remote(depending on your devices). It consists of a client and server on the host PC, where the server connects to the daemon on the android device.

### Controlling Device Programmatically

ADB is just a mechanism to communicate but the main challenge is to control the android device programmatically. Since python is my bread and butter I just need a ADB client library. So, I came across a well documented library namely pure-python-adb which will be our go to for communication.

### Capturing The Images

Now , we have power to control the device. We can just take a screenshot after forcing device to open tinder when we run the script. After the screenshot is captured within the device , it is pulled via adb to our local device (PC).

### Detecting Person Within That Image
Detecting person within an image is fairly easy task as we will be using OpenCv’s haarcascade for frontal face detection.

### Classifying The Image
In this project we will be just classifying the gender of the person and the age. The catch is to swipe right for all the females detected within the age limit. You don’t wanna swipe right to all the images , or do you? *wink . Here we will be using a small caffe model

### Making Decisions
After we have classified the images we need a mechanism to swipe right or swipe left. Again adb comes in handy.
