# Face segmentation: Mask R-CNN on supervisely
Create model for Face segmentation using transfer learning from Mask R-CNN model on Supervisely tool

Supervisely is a powerful platform for computer vision development, where individual researchers and large teams can annotate and experiment with datasets and neural networks. This help people with and without machine learning expertise to create state-of-the-art computer vision applications.

## Let's see step by step process to create, train and test face segemtation model on supervise.ly
* Go to https://app.supervise.ly/ and login, if don't have account create new one
* Create Team (Optional. we can use existing one also)

![S1]()

* We will get one workspace inside created team

![S2]()

* Import the collected images

![S3]()

* Save in one folder

![S4]()

* Segment the imported images, supervisely annotate images automatically

![S5]()

* We require a large dataset for training our model so we run DTL for image augmentation to create train set

![S6]()

* It will give the code that we required for augmentation. We can change the values inside code for increasing or decreasing the size of dataset

![S7]()

* After this we get the train set

![S8]()
![S9]()

* Create neural network, clone Mask R-CNN (Keras + TF) (COCO)

![S10]()
![S11]()
![S12]()

* Create cluster

![S13]()

* Create an agent sytem for training model. An agent is an OS that provides the resources for training our model. The agent must have all the resources that are required to train the model. I am launching an agent system on AWS cloud with Ubuntu Deep learning image which provide all the resources that are required for training our model
* Launch EC2 instance on AWS with required AMI 


![S14]()
![S15]()
![S16]()
![S17]()
![S18]()
![S19]()
![S20]()
![S21]()
![S22]()

* Connect to EC2 instance with SSH
* To connect to agent run the highlighted command on the agent system

![S23]()

* To start training, go to neural network and Click on Train and provide the training dataset in the popup window and RUN

![S24]()
![S25]()
![S26]()
![S27]()
![S28]()
![S29]()
![S30]()
![S31]()

* Training graph

![S32]()

* Checkpoint of the model

![S33]()

* For testing, go to neural network and Click on Test on trained model and provide the testing dataset in the popup window and RUN

![S34]()
![S35]()
![S36]()
![S37]()
![S38]()

* Output images

![S39]()
![S40]()
![S41]()

* Complete workflow

![S42]()


### Thank you!




