Amazon Rekognition Project.

In this project I used the following AWS services, S3, Cloud 9 IDE using an EC2 instance and Rekognition. Here is an example of the architecture. Amazon Rekognition falls under the AI services of AWS, simply put enter an image and Rekognition will give you a prediction of what it is. Potential use cases include; 

•	Identifying products in store for inventory management, 

•	Analysing customer behaviours 

•	Providing accessibility options for those who are visually impaired 


Overview

I am going to upload an image(s) to a newly created S3 bucket, then use the AWS software development kit SDK (Python version) I am going to use Rekognition to grab those images form the S3 bucket, analyse them and output with what the image is with a confidence label between 0%-100%.

![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/6cd856e6-9b68-48e2-8333-39847318936f) AWS SDK (Python)
Rekognition ![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/1bf8b5db-ac67-4c2b-b83f-df187a888be4)



First stage was to create a brand new S3 bucket and upload images which was saved as .jpg.



![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/fa230983-af57-4da3-a918-33354bef8ec1)

![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/2fd15214-bef4-47d4-a13e-d517a61be50a)


Next I installed the IDE on cloud 9.I had to create an environment which needed to create a EC2 instance (free tier).


![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/6750d269-9094-4d08-8449-d77eaef6d9f8) ![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/908fdae6-bf85-44c8-81c1-c90a666757df)


Once the EC2 environment is created, I needed to install python, to do this I used the following command $ pip install boto3.


![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/fbdd02c3-8d89-4b69-a017-eb0769943ef6)


Once this is installed, you can access the python file via new template, this allows other languages, such as, Node JS, JavaScript etc.


![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/63472397-bce9-4278-a301-9754b6ec5acd)


Next stage I had to input some code, this was available via AWS handbook as seen below.


![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/774b49f3-9dbc-42a2-9a71-b7d8d8ade684)


I did have to amend a couple of point on the code including bucket name and image name.

 
 ![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/c2997aaa-7af3-4565-8213-4a7e48050c52)

 
 Here is where the code comes to life, the first part states we are using Rekognition followed by obtaining the images from the S3 bucket titled ‘rekognition-project01’ and I uploaded the images one at a time in the below example ‘dogs.jpg’

 
 ![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/10e3d02b-6d18-4c87-a9c1-3ff0bbea5570)

 
 The code was then saved and run. As you can see Rekognition came back with the following result on the dog image. Stating a 92% confidence there is a dog in the image.

 
 ![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/a84fc8c3-9131-48fb-a32e-059a1edf45cf)

 
 ![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/74cfe180-1cfd-4ec8-bc23-f803c209336c)



 Next I used Reckognition to analyse my second image which was more complex as it had more items to identify, I simply changed then photo name to ‘busy road.jpg’ to match the object in the S3 bucket.


 ![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/fe6e2294-454b-40c9-bf49-ee21bc5e4557)


 The Rekognition software identified correct items in this image and below is selected few. It identified a Bicycle with 98% confidence, Traffic lights 97% confidence and a bus with 97% confidence

 
 ![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/660e9a19-bb01-4944-bb99-72dd45e8166b)
 ![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/75ec600f-ef77-46ee-b4ca-0a9cfcb1fb29)
 ![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/5a660990-bb46-4bee-b2a8-55a8e1f3d97a)

 ![image](https://github.com/JimSchell/AWS-Rekognition-Project/assets/165466444/4cf7c603-e6ce-448a-915a-7f06f7b46e4d)





















                                                                                                                                 

                                                                                                                                 

               
                                                                                                                                 
