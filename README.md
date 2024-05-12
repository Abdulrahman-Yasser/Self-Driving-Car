# Self-Driving-Car
a project that controls a rc-car depending on an object detection, line detection and road sign classification techniques <br>
Graduation project's book : https://github.com/Abdulrahman-Yasser/Graduation-Book

![image AMDPN2](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/6b313952-45a7-4fbf-96bf-668bf8bba339)


# First section : Image processing 

![Screenshot from 2024-05-12 08-40-15](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/d804079b-7112-474f-bc9c-3d34a92c206b)

# Second section : Object detection using YOLO with my editions

## Training our own YOLO model to detect most of things the car needs to sees<br />
### the steps i followed<br />
1 - i choosed randomly some images from Udacity dataset<br /><br />
<img src="https://user-images.githubusercontent.com/63866803/175038139-c498145c-b24d-441d-8cd9-cc7896bce845.png" width="600" height="300" ><br /><br />
2 - i changed udacity dataset and i've united all the traffic-light together in one class ID <br /><br />
![image](https://user-images.githubusercontent.com/63866803/175036273-772692c4-5d9c-446e-bcc9-d02374410ae4.png)<br />
![image](https://user-images.githubusercontent.com/63866803/175036314-0b15cd41-c68c-4153-8322-e4ecfb9b8565.png)<br />

3 - Udacity dataset became (0:biker , 1:car, 2:pedestrian, 3:traffic-light, 4:truck ) <br />
4 - i've trained the model over the edited dataset <br /><br />
<img src="https://user-images.githubusercontent.com/63866803/175036422-bb236516-cad5-49e9-8f9b-9bbef9def93e.png" width="790" height="400" ><br />

## Now i wanted to also detect all the traffic sign in the road, so i appended another dataset to the last dataset <br />
5 - i downloaded the traffic-sign dataset here <br />
6 - i changed all the traffic-sign dataset and united all the ids into 5, so all the traffic-signs has ID = 5 <br /><br />
![image](https://user-images.githubusercontent.com/63866803/175037160-5d90b7eb-9128-4c55-a316-9cbe510f91b9.png)<br />
## Now we need to detect and localize all the other objects in the new traffic-sign dataset <br />
7 - i've run the custom-trained YOLO we made in step 3 on all the images in the new traffic-sign dataset i choosed in step 5 to detect the other objects in the images  <br />
8 - we will convert the produced YOLO text files format into YOLO training format<br /><br />
![image](https://user-images.githubusercontent.com/63866803/175037080-d799eeef-b5c9-4b1a-a1cb-b491af79aa2f.png)<br />

9 - now we have got text files that contains the other objects data that we got from running the trained YOLO model to detect all the other objects, we can append the lines in bothe texts together (step5 text + step 6 text) <br /><br />
![image](https://user-images.githubusercontent.com/63866803/175037187-94978ccf-6245-4bf6-90ef-97b7f085644e.png) <br />


10 - we will train a new YOLO model to detect a new combined dataset (0:biker , 1:car, 2:pedestrian, 3:traffic-light, 4:truck, 5:trafficsign) <br /><br />
<img src="https://user-images.githubusercontent.com/63866803/175037243-ba7a6a8c-93d3-4d5a-97b3-06f2db7f549c.png" width="600" height="300" ><br />
## The result i've got 
<img src="https://user-images.githubusercontent.com/63866803/175038587-f7f8c856-848b-4d90-9afb-823b9601557e.png" width="790" height="400" ><br />
<img src="https://user-images.githubusercontent.com/63866803/175038627-85b374e0-b1b2-42c4-b175-aaf2ee3557d3.png" width="790" height="400" ><br />
<img src="https://user-images.githubusercontent.com/63866803/175038708-541eb03b-496d-4e22-b1ea-aa7694ad6e20.png" width="790" height="400" ><br />


# Third section : Behavioral cloning (UDACITY simulation)


![Screenshot_2024-05-12_08-50-28](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/0b70c43a-34e2-4f98-acf2-6d41ff03dd76)
![Screenshot from 2024-05-12 08-51-17](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/c4f94011-7a22-4580-9497-86db09f96dfd)
![Screenshot from 2024-05-12 08-49-59](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/6c34811a-95e0-4561-b07a-9c6c605be363)

# Fourth Section : Traffic sign recognition (leNet model)
![image 1VUON2](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/23b8a304-e26c-4db9-bee4-a752c91ca3e1)
![image 115UN2](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/9b401265-1762-49e1-b61f-b87d4b044393)
![image GKYON2](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/aa7f6fd0-9a0d-4041-9e41-f9ebb4d493f7)

## Tunning the model
![image 64KQN2](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/328ea7e8-828a-4034-b561-6d31e627bf0e)
![image 5NDXN2](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/89afddf2-bff9-4689-8756-17797ec2e6f0)

## Result : 

![image 6LZ4N2](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/a512f1df-3589-4532-8e20-29b7c2df6130)
![image PE4ZN2](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/8c9c4774-abbd-4eb4-9d01-102551c88005)
![image XBIYN2](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/bf54a4b0-ce94-4317-9a39-903f3d76dd43)

# Fifth section : Tiva-C programming (Bare-metal drivers)
### It was bad code because i didn't have time to enhance it, and it didn't affect the core project that much. It worked, so don't touch it XD

<br>PLL : <br>
![image K4OTN2](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/64632868-4462-4348-934f-759d78a5816b)
<br>PWM : <br>
![image TBA4N2](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/6239c126-2e35-422c-87d9-0238c067a166)
<br> UART : <br>
![image 65PNN2](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/59e0a199-b21f-4858-a270-f6cb7aeebf3b)
![image I8N3N2](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/9a1b823f-bdb8-4cc5-bf95-7d7cc43282f8)
<br>Common : <br>
![image 5LMQN2](https://github.com/Abdulrahman-Yasser/Self-Driving-Car/assets/63866803/4d64d348-dbf2-488e-833d-d44b37421ba4)







