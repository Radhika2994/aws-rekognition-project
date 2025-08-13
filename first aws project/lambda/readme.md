Next, I created a Lambda function in Python. This was the main logic. I did the following in the code:

Read the image from S3

Call Rekognition to detect labels

Save the labels as JSON back to S3

Insert each label into DynamoDB

Send an SNS email if a special label is detected (like Person)

At first, it was confusing how to connect all the services, but I learned how Lambda is event-driven, so it runs automatically whenever an image is uploaded.

I realized my Lambda function needed permissions to:

Read/write S3

Access Rekognition

Put items in DynamoDB

Publish to SNS

I attached the policies step by step. It helped me understand that without proper IAM permissions, nothing works, and AWS is very secure about service access.

