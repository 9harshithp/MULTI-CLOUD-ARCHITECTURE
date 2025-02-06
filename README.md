# MULTI-CLOUD-ARCHITECTURE
**COMPANY**: CODTECH IT SOLUTIONS

**NAME**: HARSHITH P

**INTERN ID**:CT08IJR

**DOMAIN**: Cloud Computing

**BATCH DURATION**: January 30th, 2025 to March 1st, 2025

**MENTOR NAME**: NEELA SANTHOSH

**ENTER DESCRIPTON OF TASK PERFORMED NOT LESS THAN 500 WORDS**: 
Description of Task Performed:

The task involved setting up an AWS Lambda function named myfunction914 to process data from an S3 bucket. This task aimed to automate data processing using AWS’s serverless architecture. By leveraging the free-tier options and following best practices, the solution ensured efficiency, scalability, and cost-effectiveness. The steps below provide a detailed account of the work performed.

Step 1: Creating the S3 Bucket

The first step was to create an Amazon S3 bucket named my-multicloud-bucket914, which served as the central storage for data files. This bucket was configured to trigger the Lambda function whenever a new file was uploaded. Initially, I uploaded some sample data files to the bucket, such as CSV files, to test the integration. Proper permissions were required for the Lambda function to access the bucket. This was achieved by attaching an IAM policy that allowed actions like s3:GetObject on the bucket’s resources.

During this step, I encountered a challenge where the bucket policy conflicted with AWS’s default Block Public Access settings. To resolve this, I navigated to the Permissions tab of the bucket, reviewed the Block Public Access settings, and temporarily disabled the restrictions while ensuring no sensitive data was exposed. This allowed the policy to function as expected.

Step 2: Setting Up the AWS Lambda Function

Next, I created a Lambda function named myfunction914 to process files uploaded to the S3 bucket. The function was written in Python and utilized the boto3 library to interact with AWS services. The main functionality of the Lambda function included:

Detecting when a file was uploaded to the S3 bucket.
Downloading the file to the Lambda runtime environment.
Processing the file and printing the output to Amazon CloudWatch for monitoring.
The function was assigned an execution role with permissions to read files from the S3 bucket. This ensured secure access without exposing the bucket to unnecessary risks. After completing the function code, I deployed it and tested its execution.

Step 3: Connecting the Lambda Function to S3

To automate the workflow, I configured an S3 event trigger for the Lambda function. This trigger was set to invoke the Lambda function whenever a new file was uploaded to the bucket. The configuration involved:

Navigating to the Properties tab of the S3 bucket.
Selecting Event notifications and setting the event type to PUT.
Specifying the Lambda function myfunction914 as the destination.
After setting up the trigger, I uploaded a test file to the bucket to validate the integration. I checked the CloudWatch logs to confirm that the function executed successfully and processed the uploaded file.

Step 4: Using EC2 for Supporting Tasks

As part of the architecture, I also launched a t3.micro EC2 instance. This instance provided additional compute resources and acted as a backup for tasks that might require manual intervention or extended processing time. I installed the AWS CLI on the EC2 instance and tested its connectivity to the S3 bucket by downloading a file using the command:

I have added CSV folder to it.
This validated the interoperability between EC2 and S3. The t3.micro instance, being free-tier eligible, was a cost-effective addition to the architecture.

Step 5: Testing and Documenting the Workflow

Once the setup was complete, I conducted multiple tests to ensure the architecture was functioning as intended. I uploaded various files to the S3 bucket and observed the Lambda function's execution through CloudWatch logs. The logs confirmed that the files were successfully processed, and the output was accurate.

Finally, I documented the entire workflow, highlighting the integration between AWS services like S3, Lambda, and EC2. The documentation included the purpose of each service, configuration steps, and the challenges encountered (e.g., resolving bucket policy conflicts). I also provided screenshots and code snippets to make the documentation user-friendly.

Conclusion

This task demonstrated the power of AWS's serverless capabilities and its ability to handle automated data processing workflows. The Lambda function, paired with S3 and EC2, formed a scalable and efficient architecture. The challenges encountered, such as handling bucket permissions and configuring event triggers, provided valuable learning experiences. The setup is well-suited for real-world use cases requiring automation and integration in cloud environments.

**The output for the Task**:
<img width="958" alt="Image" src="https://github.com/user-attachments/assets/63f4c152-1acf-42dc-b7a1-a2247df759d6" />

<img width="960" alt="Image" src="https://github.com/user-attachments/assets/eec9898a-c586-4a50-ad90-56e02d699e3a" />

<img width="956" alt="Image" src="https://github.com/user-attachments/assets/80284600-4a04-4efc-93fa-2a5c8fba35ce" />
