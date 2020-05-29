# Mlops_project
Why 60% ML Project Are Never Implemented ?
Reason:
when we train our model in machine learning , at the end we get accuracy of our Model . if accuracy is less or model give wrong prediction then we need to retrain the model by chnaging hyper-parameters like

-Number Of Fully Connected Layers.
-Number of Neurons in one particular layer
-Which optimizer to use?
-Which Activation function to use?
-Number Of CRP Layer is Used
-kernal box size and Polling box size
-No of Epoch.
Every time while implementing Machine learning Code or Project we need to Perform Hit and Trial by adjusting Hyperparameter Manually to get better Model Accuracy i.e Model prediction Accurate .But problem here is It may require more than one day .Sometimes This process goes on until you are not satisfied with the outcomes. Hence at last either it's too late for the production or the accuracy doesn't match our requirement, eventually ends in shutting down of project. This might create a huge loss for companies and it's reputation.

Human Can not able to perform manually this things i.e Adjusting Hyparameter to Get Better Accuracy .For This We Require Automation Which Adjust Hyperparameter Automatically To Get Better Accuracy .

This Automation is achived by Integration Of Devops CI/CD with Machine Learning OR Deep Learning . i.e Devops CI/CD Pipeline used to build and deploy ML and DL project . this Automation in Machine learning achieved Using DevOps Tools This Technology is Called as MLOps. This Automation is Achived Using Devops Tools Like Docker , Jenkins, Git Hub , Kubernetes.

this article is show how the automation occur between machine learning code and Devops To achieve greater Accuracy and Accurate prediction by using jenkins ,git hub,docker.

tasks: 

Create a container image that has Python3 and Keras or numpy installed using dockerfile.
 When we launch container using this created images, it should automatically starts Container and train the model in the present container.
create a job chain of job1, job2, job3 and job4 using build pipeline plugin in Jenkins 
Job1 : Pull the Python file present in Github repo automatically ,when developers push file to Github. and By looking at the code or program file, Jenkins should automatically start or create the respective Container which have machine learning software installed interpreter to train the model using appropriate image ( eg. If code uses CNN, then Jenkins should start the container that has already installed all the software required for the CNN processing).
 Job 2: Train your model and predict accuracy or metrics. If metrics accuracy is less than 95% , then tweak the machine learning model architecture. Retrain the model and get the train model by triggering Job3
Job3: This job sent the notification to developer or If we already provide a Hyperparameter to Job3 then job3 import the hyper-parameters in the python code and retrain the model until we get Accuracy greater than our Specified limit.
Create One extra job job5 for monitor : If container, where app is running, fails due to any reason then this job should automatically start the container again. And also sent a mail to developer.

for details about my project you can see on  https://www.linkedin.com/pulse/why-60-ml-project-never-implemented-rameshwar-somvanshi/?trackingId=Y3%2FoAWHNRQSqDTeBcbNs9g%3D%3D
