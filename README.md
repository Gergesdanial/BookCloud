# BookCloud

## Overview
BookCloud is a versatile platform that allows users to easily upload, organize, and share books and articles. Whether you're a student, researcher, or avid reader, BookCloud offers a seamless way to store and access your reading materials online.

<img width="1440" alt="Screenshot 2024-05-29 at 2 06 58 PM" src="https://github.com/Gergesdanial/BookCloud/assets/127982294/221f9f5c-c312-4815-816b-393898933b0c">

## Technology Stack
- **Frontend:** React
- **Backend:** Node.js, Express.js
- **Database:** DynamoDB
- **Image Storage:** AWS S3
- **Deployment:** AWS EC2
- **Content Delivery:** AWS CloudFront
- **AWS SDK:** Used for interacting with AWS services

## Features
1. **CRUD Operations:**
   - **Create:** Add new items to the dataset.
   - **Read:** View all items or a single item from the dataset.
   - **Update:** Modify existing items in the dataset.
   - **Delete:** Remove items from the dataset.

2. **High Availability Architecture:**
   - Application deployed across multiple EC2 instances in different Availability Zones for high availability.
   - CloudFront used for faster delivery of the application.

3. **DynamoDB Integration:**
   - A DynamoDB table with at least three attributes to manage the dataset.
   - 
<img width="1433" alt="Screenshot 2024-05-29 at 2 14 03 PM" src="https://github.com/Gergesdanial/BookCloud/assets/127982294/f80c34f8-1616-4fa6-95cd-dd6e45e68133">

4. **S3 Image Upload:**
   - Upload images for newly created items and store them in an S3 bucket.
   - Ensure images are displayed when items are retrieved.
   - Allow updating of images associated with items and retain old and new versions.
   - Delete images when corresponding items are deleted from the dataset
   
<img width="1433" alt="Screenshot 2024-05-29 at 2 12 44 PM" src="https://github.com/Gergesdanial/BookCloud/assets/127982294/282f3276-e35c-465e-88f2-b459cc39a53c">
<img width="1433" alt="Screenshot 2024-05-29 at 2 13 01 PM" src="https://github.com/Gergesdanial/BookCloud/assets/127982294/dea23418-6a65-422b-a24b-546d3b811783">
<img width="1433" alt="Screenshot 2024-05-29 at 2 13 31 PM" src="https://github.com/Gergesdanial/BookCloud/assets/127982294/2ecc80e7-3ca8-4ca3-a887-5abfb11d51d6">



5. **AWS SDK Usage:**
   - Programmatic interaction with AWS services using AWS SDK for JavaScript.

6. **Lambda Function:**
   - A Lambda function triggered upon the creation of new items to resize images uploaded to an S3 bucket. Additional bucket can be used for resized images if needed.
<img width="1400" alt="Screenshot 2024-05-29 at 2 11 54 PM" src="https://github.com/Gergesdanial/BookCloud/assets/127982294/51a2f869-eae6-4526-a25a-74437fe3fbca">



### Deploying to AWS
1. **EC2 Instances:**
   - Deploy the backend and frontend applications on multiple EC2 instances across different Availability Zones.
   - 
     <img width="1433" alt="Screenshot 2024-05-29 at 2 14 52 PM" src="https://github.com/Gergesdanial/BookCloud/assets/127982294/db0c70df-3e5a-4940-be27-02e498475a79">
     <img width="1400" alt="Screenshot 2024-05-29 at 2 11 24 PM" src="https://github.com/Gergesdanial/BookCloud/assets/127982294/9fc1b754-e1eb-4759-b2cd-9dd479eb82fe">



2. **Lambda Function:**
   - Deploy the Lambda function to resize images upon item creation.

## Usage
- Access the application via the EC2 loadbalancers .
- Perform CRUD operations through the web interface.
- Uploaded images will be stored in S3 and associated with items in DynamoDB.

