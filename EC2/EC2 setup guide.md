## Step-by-step guide on how to create an EC2 instance on AWS:

**1. Access the AWS Management Console:**

Login to your [AWS](https://aws.amazon.com/console/) account and navigate to the AWS Management Console.
As a Beginner, you can use AWS as a 'Root User'.

![image](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/259220b8-029f-44ba-9c85-2eaa5033e02e)


**2. Open the Amazon EC2 Service:**

In the AWS Management Console search bar, type "EC2" or find the "EC2" service under the "Compute" category.
Click on "EC2" to open the Amazon Elastic Compute Cloud service dashboard.

![image](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/a3e5cf69-7aa4-4e7f-b010-6535ee6f06b4)


**3. Launch an Instance:**

Click the orange button labeled "Launch Instance" on the EC2 dashboard.

![image](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/6f40b025-6227-4128-b055-1f49c69487bc)


**4. Choose an AMI (Amazon Machine Image):**

An AMI is a pre-configured software environment that provides the operating system and basic software for your instance.
You can browse popular AMIs provided by Amazon or search for specific operating systems.
I chose Amazon Linux as it was beginner-friendly and from a free tier.

![image](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/594170d8-fa00-44eb-9484-2378a1f9644e)


**5. Select an Instance Type:**

Instance types define the computing power, memory, and storage capacity of your EC2 instance.
Choose an instance type based on your workload requirements.
For beginners, a general-purpose instance type like t2.micro (free tier eligible) is a good starting point.
You can explore different instance types under the "Instance Type" section, considering factors like CPU cores, memory (RAM), and storage.

![image](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/fc04b32e-44bc-4c4c-a585-f3b1318d8411)


**6. Key Pair Creation:**

During launch, you might be prompted to create a key pair. A key pair is used for secure access to your Linux instance via SSH.
Now, you can use the key pair you earlier created or you can create a new one by clicking 'Create new key pair'.
Download the private key file securely and store it in a safe location. You'll need this file to connect to your instance later.

![image](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/4a771d63-1eef-4303-8a40-fae72e1766ff)


**7. Add Security Group:**

A security group defines the inbound and outbound traffic rules for your instance.
You can create a new security group or choose an existing one.
Ensure that you allow both HTTP and HTTPS traffic from the internet.
Make sure to allow SSH access (port 22) for initial connection if you're using a Linux-based AMI.
You can configure additional rules based on your application's needs.

![image](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/a5474436-70d4-4226-b1a1-8a5c6053c837)


**8. Review and Launch:**

Review the configuration details of your instance on the summary page.
Double-check the AMI, instance type, security group, and any other customized settings.
Click the orange "Launch" button to start the instance creation process.

![image](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/7dd21782-ae96-4268-aa09-af05b8d0d5c8)



**9. Instance State Monitoring:**

Once launched, your EC2 instance will appear in the list of instances with a status of "pending" while it's being provisioned.
The status will eventually change to "running" once the instance is ready. Wait till the Status Check changes to "2/2 checks passed".

![image](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/c95878d5-4b59-46ca-8a90-a378b499f9ef)


**10. Connecting to Your Instance:**

After the instance is running, you can connect to it using a terminal application like PuTTY (Windows) or the built-in terminal (Linux/macOS).
Use the public DNS name of your instance and your private key file to establish an SSH connection.
