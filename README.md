# 📘 OVERVIEW
The story follows a senior alumnus returning to National Central University, revisiting familiar places filled with memories. Players assist him in recalling the past by exploring various campus locations and uncovering fragments of his memories along the way.

## Storyline Locations

- Jhih-Shi Hall

- College of Management Building II

- Library

- Late-Night Snack Street (Li-Cheng)

- Pinecone Restaurant

- Dorm 9 Cafeteria

- Track and Field

- Teaching and Research Building

- Banyan Tree on the Main Lawn

## Operation Principle
The LINE bot detects images uploaded by users. If it recognizes that an uploaded photo corresponds to a symbol, it returns the name of the folder so that Colab can execute the next part of the scenario.
Example: Suppose we want the user to send a photo of Zhixi Hall. When the user uploads a photo, the recognition model compares it with the folders in the model. If the model identifies the uploaded photo as the symbol management1, it returns management1. Since our scenario file contains keywords related to management1, the next part of the scenario will be executed, and this process continues similarly.

## Applied Technologies

- Image Recognition: used for identifying visual elements and linking them to story events.

- Keyword Search System: includes two modes —

  - Template with image matching
  
  - Template without image matching

# ⚙️ Seeting Flow
## Step 1 – LINE Developer Parameter Input in Colab
1. Go to the LINE Developers website, log in with your LINE account, and create a new channel.
2. After creating the channel, navigate to Basic Settings and copy the LINE Channel Secret, then paste it into your Colab notebook.
3. Next, go to the Messaging API section, find the Channel Access Token, and paste it into Colab as well.
<img width="1150" height="562" alt="image" src="https://github.com/user-attachments/assets/5a856518-a492-4c4a-bc42-64a6ac0c0ee5" />
<img width="1152" height="545" alt="image" src="https://github.com/user-attachments/assets/d0d28a73-3212-4add-9104-d5129e1da4ad" />
<img width="1145" height="552" alt="image" src="https://github.com/user-attachments/assets/70dbfd06-904f-405f-a134-9b0cf01b1b08" />

## Step 2 – AWS AI Model Parameter Input in Colab
1.Open the AWS Learner Lab and enable the AWS services.
2.Upload the required image files to Amazon S3.
3.After uploading, go to Amazon Rekognition to perform image recognition on the files stored in S3.
4.Once the model setup is complete, you can start using it.
5.Enter the AWS CLI parameters and the model’s analysis results (ans) into Colab.
<img width="1147" height="563" alt="image" src="https://github.com/user-attachments/assets/35185766-a359-42cd-ab52-85b394c4345c" />
<img width="1148" height="539" alt="image" src="https://github.com/user-attachments/assets/dcae6ff0-fa01-4914-b48f-fc2583a20c29" />
<img width="1149" height="543" alt="image" src="https://github.com/user-attachments/assets/bc03d41e-96ab-4f21-9e0d-b92450dfe178" />

## Step 3 Training Data Collection
1.Record videos of the symbols, capturing them from as many angles as possible. Each video should be approximately 30–40 seconds long.
2.Use the Adpter video screenshot software to extract frames from the videos, taking about one or two screenshots per second (for the model to perform image recognition, at least 30–50 photos are needed for training).
3.Use PowerPoint to crop the images, ensuring that the symbol occupies most of the photo.

## Step 4 AWS Rekognition training
1.Click Create Project.
2.Choose to import images from S3, and paste the S3 image links into the model for training. You may need to grant permissions during this process.
3.After creating the project, proceed with labeling the images (this step can be skipped if the images were already organized into folders in S3). Then, you can start training the model.
<img width="1149" height="540" alt="image" src="https://github.com/user-attachments/assets/cf09eaf5-a363-4d70-85e4-b40df04cc387" />
<img width="1149" height="560" alt="image" src="https://github.com/user-attachments/assets/42ad3e71-7115-4f7f-a7b6-a16878826c51" />
<img width="1150" height="563" alt="image" src="https://github.com/user-attachments/assets/15309c91-421a-4b9d-97c8-7f6c8388a9a4" />
<img width="1148" height="559" alt="image" src="https://github.com/user-attachments/assets/2211157d-4902-4f11-b5a2-ea5cd6cc66dc" />

## Step 5 Establish Scenario
1.Create an Excel file and edit the scenario.
2.Use Line Bot Designer to generate the message reply JSON file.
3.According to the scenario requirements, generate the corresponding quick reply button JSON file (using the Colab program provided by the instructor).
4.Upload the completed files to the Colab execution environment.
<img width="996" height="611" alt="image" src="https://github.com/user-attachments/assets/440be066-b573-4f1b-acbd-4e74b5ab72be" />
<img width="1150" height="561" alt="image" src="https://github.com/user-attachments/assets/dbee80b7-8734-4d58-870a-f1eb6ea664eb" />
<img width="1147" height="523" alt="image" src="https://github.com/user-attachments/assets/fbfc2338-0794-442f-97f5-cb3b76010c84" />

