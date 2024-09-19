Solution: The name of the dam is Malampuzha dam in Palakkad

How did I find out?

The challenge starts like this:

![image](https://github.com/user-attachments/assets/bcad718d-998e-4b8b-b390-0c9ef49d056c)

When you click the link, it takes you to this image called heaven.jpg

![image](https://github.com/user-attachments/assets/a97aa55f-f12c-4224-96b0-9f7323288a4b)

The task is to figure out the name of the dam of the reservoir. 

A quick search in Google lets you know of a tool named Exiftool that can be used to extract meta data of an image. Why meta data? Well, meta data is a data in a data, basically in the case of images, meta data can give me several information regarding the image like information about the camera settings, the date and time when the image was taken, the camera model and most importantly, the gps coordinates.

Getting the gps coordinates can help me identify the location of the image, so I installed Exiftool. 

![image](https://github.com/user-attachments/assets/a1a0b28e-8f4a-4086-b0df-5b8e8305397f)

After extracting the zip file, I dragged and dropped my required image in exiftool.exe. This is what I got:

![image](https://github.com/user-attachments/assets/876a90ce-7c06-4895-8f2c-6320a8e8c3a6)

At first glance, this doesn't seem to contain anything seemingly important. But when you look at the image description, it kinda looks like base64 code.

![image](https://github.com/user-attachments/assets/78735177-6e16-4ff4-b45b-df30f7b1088b)

So I used Notepad++ to decode the base64 and well, I got two decimal numbers, that very much resemble coordinates of an image

![image](https://github.com/user-attachments/assets/831d10f1-a997-4b42-ac4c-f29e46e43f6e)

So, I searched up the coordinates in Google Maps and here's what I found:

![image](https://github.com/user-attachments/assets/71c553a0-92e6-43b0-ad21-485508222a61)

And hence, I solved the mystery of the dam: Its Malampuzha dam in Palakkad
