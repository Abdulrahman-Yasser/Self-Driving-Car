### Training our own YOLO model to detect most of things the car needs to sees<br />
## the steps i followed<br />
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
