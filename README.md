# AWS-Rekognition-Project
In this project I used the following AWS services, S3, Cloud 9 IDE using an EC2 instance and Rekognition. Here is an example of the architecture. Amazon Rekognition falls under the AI services of AWS, simply put enter an image and Rekognition will give you a prediction of what it is. Potential use cases include; 



•	Identifying products in store for inventory management.



•	Analysing customer behaviours 



•	Providing accessibility options for those who are visually impaired 


Overview

I am going to upload an image(s) to a newly created S3 bucket, then use the AWS software development kit SDK (Python version) I am going to use Rekognition to grab those images form the S3 bucket, analyse them and output with what the image is with a confidence label between 0%-100%.


Services


![image](https://github.com/user-attachments/assets/ee7b7763-72d6-4168-8345-4c1245121792) ![image](https://github.com/user-attachments/assets/d2574a37-497d-4576-9432-2c989086e1e0) ![image](https://github.com/user-attachments/assets/89fbd5a1-3a6d-452c-bb54-4ae6921f99c4)

AWS Rekognition - is a cloud-based image and video analysis service that makes it easy to add advanced computer vision capabilities to your applications. The service is powered by proven deep learning technology and it requires no machine learning expertise to use. Amazon Rekognition includes a simple, easy-to-use API that can quickly analyze any image or video file that’s stored in Amazon S3.                                                                                                                                


First stage was to create a brand new S3 bucket and upload images which was saved as .jpg.

Images I used were of dogs and a busy road with traffic.



![image](https://github.com/user-attachments/assets/553f9e90-ba6e-4e1f-8384-a2b8ee865522)


![image](https://github.com/user-attachments/assets/7e23b627-02bf-468e-9c19-fecbce34b5a5)



Next I installed the IDE on cloud 9.I had to create an environment which needed to create a EC2 instance (free tier).

![image](https://github.com/user-attachments/assets/e4b2b7cc-b093-47ed-844d-24f03c2407bc)
![image](https://github.com/user-attachments/assets/7e5ff46f-aa5d-4d27-8988-feb83352eedc)


Once the EC2 environment is created, I needed to install python, to do this I used the following command $ pip install boto3.

![image](https://github.com/user-attachments/assets/aea0dd27-0618-498b-9280-6decc3f8cace)


Once this is installed, you can access the python file via new template, this allows other languages, such as, Node JS, JavaScript etc.


![image](https://github.com/user-attachments/assets/5b80b333-af8f-4327-870b-fc212ebb14cb)

Next stage I had to input some code, this was available via AWS handbook as seen below.


#![image](https://github.com/user-attachments/assets/ab323152-124f-4400-ae30-4d583bcb76a9)


I did have to amend a couple of point on the code including bucket name and image name.


![image](https://github.com/user-attachments/assets/0839c36b-4c74-42e1-b25a-1c9276d01569)

Here is where the code comes to life, the first part states we are using Rekognition followed by obtaining the images from the S3 bucket titled ‘rekognition-project01’ and I uploaded the images one at a time in the below example ‘dogs.jpg’

![image](https://github.com/user-attachments/assets/3e3bb650-f965-460a-a281-87d284f63242)


The code was then saved and run. As you can see Rekognition came back with the following result on the dog image. Stating a 92% confidence there is a dog in the image.

![image](https://github.com/user-attachments/assets/0e67e780-27e9-4889-8fce-f0d43f5ff8e3)
![image](https://github.com/user-attachments/assets/ec6d452c-4962-439d-9ca9-48d0bb79f275)



Next I used Reckognition to analyse my second image which was more complex as it had more items to identify, I simply changed then photo name to ‘busy road.jpg’ to match the object in the S3 bucket.
The Rekognition software identified correct items in this image and below is selected few. It identified a Bicycle with 98% confidence, Traffic lights 97% confidence and a bus with 97% confidence

![image](https://github.com/user-attachments/assets/98e5c3bd-b63f-40af-b0a7-9e64150f4ba0) ![image](https://github.com/user-attachments/assets/811ccf83-d073-42ab-bc6e-6b092ef356bb) ![image](https://github.com/user-attachments/assets/8eca229c-7c6b-458b-8bef-d05027caf003)



![image](https://github.com/user-attachments/assets/37039c0a-04ec-4312-b61d-5d14e91aeafb)



















