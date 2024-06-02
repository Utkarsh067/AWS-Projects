![image](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/d557083d-0332-4c3f-bed6-e33e14530f05)

[Amazon Web Services(AWS)](https://aws.amazon.com/) is a cloud computing platform that offers a variety of services on-demand, including storage, computing power, databases, and more. AWS is free to join, and users only pay for what they use. AWS services are available globally from data centers in different regions, and the scale of the data centers is based on user traffic and needs to provide low-latency services. 

## In this project, we will be using the S3 service of AWS for 'Hosting a Website on AWS'.

### What is S3?
Amazon Simple Storage Service (Amazon S3) is an object storage service that offers industry-leading scalability, data availability, security, and performance. You can use Amazon S3 to store and retrieve any amount of data at any time, from anywhere.

## Now starting with our project

**Steps:**
1. Create or log in to an AWS account using Root User.

2. In the Dashboard, you will see a search option, a search for S3, and it will be in Storage services.

3. Click on S3 and create a Bucket, bucket name should be unique.

4. Remove 'Block all public access' and let other things be at default and click on 'Create Bucket'.

5. After creating the Bucket, click on the name of the bucket, go to its properties, and scroll all the way down, you will see 'Static website hosting', click edit on it.

6. In 'Static website hosting', you have to enable it and go down to 'Index Document' and write the HTML document name (for ex - index.html) and save changes

7. After this, in 'Static website hosting' you will get a 'Bucket website endpoint', copy it and paste it into a new tab, it will give an error because we haven't uploaded files on S3 yet.

8. Now, go to the S3 bucket's Permissions, and there you will see 'Bucket Policy', click on edit and write the code given below -

```json
{
  
    "Version": "2012-10-17",
    
    "Statement": [
    	{
        	"Sid": "PublicReadGetObject",
        	"Effect": "Allow",
        	"Principal": "*",
        	"Action": [
            	"s3:GetObject"
        	],
        	"Resource": [
                "arn:aws:s3:::Bucket-Name/*"
        	]
    	}
    ]
}
```

+ **This allows everyone to read/view everything in the bucket.  Be sure to update the Bucket Name and save changes**

9. Now you must go to bucket objects and upload your files.

10. Refresh or reopen the link you copied from 'Bucket website endpoint' and now you can see your website fully functioning.

11. Congratulations you have hosted your website on AWS!!!🎉🎉🎉.
