# Face segmentation: Mask R-CNN on supervisely
Create model for Face segmentation using transfer learning from Mask R-CNN model on Supervisely tool

Supervisely is a powerful platform for computer vision development, where individual researchers and large teams can annotate and experiment with datasets and neural networks. This help people with and without machine learning expertise to create state-of-the-art computer vision applications.

## Let's see step by step process to create, train and test face segmentation model on supervise.ly
* Go to https://app.supervise.ly/ and login, if don't have account create new one
* Create Team (Optional. we can use existing one also)

![S1](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S1.png)

* We will get one workspace inside created team

![S2](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S2.png)

* Import the collected images

![S3](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S3.png)

* Save in one folder

![S4](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S4.png)

* Segment the imported images, supervisely annotate images automatically

![S5](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S5.png)

* We require a large dataset for training our model so we run DTL for image augmentation to create train set

![S6](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S6.png)

* It will give the code that we required for augmentation. We can change the values inside code for increasing or decreasing the size of dataset

![S7](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S7.png)

* After this we get the train set

![S8](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S8.png)
![S9](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S9.png)

* Create neural network, clone Mask R-CNN (Keras + TF) (COCO)

![S10](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S10.png)
![S11](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S11.png)
![S12](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S12.png)

* Create cluster

![S13](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S13.png)

* Create an agent system for training model. An agent is an OS that provides the resources for training our model. The agent must have all the resources that are required to train the model. I am launching an agent system on AWS cloud with Ubuntu Deep learning image which provide all the resources that are required for training our model
* Launch EC2 instance on AWS with required AMI 


![S14](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S14.png)
![S15](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S15.png)
![S16](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S16.png)
![S17](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S17.png)
![S18](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S18.png)
![S19](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S19.png)
![S20](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S20.png)
![S21](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S21.png)
![S22](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S22.png)

* Connect to EC2 instance with SSH
* To connect to agent run the highlighted command on the agent system

![S23](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S23.png)

* To start training, go to neural network and Click on Train and provide the training dataset in the popup window and RUN

![S24](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S24.png)
![S25](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S25.png)
![S26](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S26.png)
![S27](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S27.png)
![S28](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S28.png)
![S29](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S29.png)
![S30](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S30.png)
![S31](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S31.png)

* Training graph

![S32](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S32.png)

* Checkpoint of the model

![S33](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S33.png)

* For testing, go to neural network and Click on Test on trained model and provide the testing dataset in the popup window and RUN

![S34](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S34.png)
![S35](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S35.png)
![S36](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S36.png)
![S37](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S37.png)
![S38](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S38.png)

* Output images

![S39](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S39.png)
![S40](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S40.png)
![S41](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S41.png)

* Complete workflow

![S42](https://github.com/surinder2000/face-segmentation-maskrcnn-on-supervisely/blob/master/Screenshots/S42.png)


### Thank you!




