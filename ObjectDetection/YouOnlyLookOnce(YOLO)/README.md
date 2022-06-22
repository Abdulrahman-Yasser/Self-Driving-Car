### Training our own YOLO model to detect most of things the car needs to sees<br />
## the steps i followed<br />
1 - i changed udacity dataset and i've united all the traffic-light together in one class ID <br />
2 - Udacity dataset became (0:car , 1:pedestrian, 2:traffic-light, 3:truck, 4:bicker ) <br />
3 - i've trained the model over the edited dataset <br />
## Now i wanted to also detect all the traffic sign in the road, so i appended another dataset to the last dataset <br />
4 - i downloaded the traffic-sign dataset here <br />
5 - i changed all the traffic-sign dataset and united all the ids into 5, so all the traffic-signs has ID = 5 <br />
## Now we need to detect and localize all the other objects in the new traffic-sign dataset <br />
6 - i've run the custom-trained YOLO we made in step 3 on all the images in the new traffic-sign dataset i choosed in step 5 to detect the other objects in the images  <br />
7 - now we have got text files that contains the other objects data that we got from running the trained YOLO model to detect all the other objects, we can append the lines in bothe texts together (step5 text + step 6 text) <br />
8 - we will train a new YOLO model to detect a new combined dataset (0:car , 1:pedestrian, 2:traffic-light, 3:truck, 4:bicker, 5:trafficsign) <br />
