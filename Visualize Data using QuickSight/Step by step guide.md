### Steps:

1. Log in to the AWS account using Root user.

2. Search for S3 in services under Storage.

3. Click on Create Bucket, and name your bucket, it should be in lowercase and unique, and let all other things be at default.

4. I have provided the 'Dataset csv' file and 'JSON manifest' in this folder, you have to download it and upload it to your bucket
   **Note - Open the JSON file before uploading it, and in place of Bucket-Name use the name of your bucket.**

5. After uploading the files, open AWS Quicksight in a new tab, you can find Quicksight by searching it in AWS services.

6. Quicksight will ask you to create an account.
   
  ![Screenshot 2024-06-05 005957](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/ee1ea12e-43c8-4660-a84a-20b61d779b0f)

7. Make sure you are using the 30-day free trial option in Quicksight, you would have to select your region, choose your username, and write your e-mail. After all these click on Create Account.

8. Now, you will arrive at the QuickSight Dashboard
    
  ![Screenshot 2024-06-05 004629](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/f5cc45f3-3b0c-47e9-92a2-bcf10fbc61e6)

9. Go to Datasets, it will appear like this
    
  ![Screenshot 2024-06-05 004805](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/85f1c7b0-a047-4011-9fea-bf1ecd01b0bc)

10. Click on New Dataset, it will provide various options, you have to choose S3
    
    ![Screenshot 2024-06-05 004816](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/3ff5cbcb-07ef-481b-bdad-6340271421f7)

11. Now it will ask you to give 'Data Source Name', it can be anything, and it will also ask for the URL of the JSON Manifest file.
    You can get the URL by -
    + Go to the Bucket we created
    + Click on the manifest file
    + Go to its properties
    + Copy Object URL

    Now paste this URL into Quicksight and click Connect.

    ![Screenshot 2024-06-05 004826](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/812cfa94-afa6-4f56-adb0-2893197f15ab)
      
12. Now, it will ask you to choose between Interactive Sheet or Paginated Report, you have to select Report Interactive and click Create.
    
    ![Screenshot 2024-06-05 004919](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/78b71620-2814-4d71-8d12-87ba5a31cf07)

13. It will provide you with a screen like this

    ![Screenshot 2024-06-05 005028](https://github.com/Utkarsh067/AWS-Projects/assets/161854515/7c75b120-eb84-4d55-85f0-b3dd71ef379d)

    Here you have to drag and drop the criteria you want to be visualized (like brands, price, etc.). 
    You can also sort the graph in ascending or descending order or based on the data you are using.

14. Don't forget to delete your QuickSight account, as you will be charged after the trial period is over.

15. Congratulations, you have successfully visualized your data in AWS using QuickShight🎉🎉.
