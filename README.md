# WDL-project-online-quiz

1.      Create a New User via IAM service on the AWS Console named admin user. 
Choose to create an Access key - Programmatic access and give the name for the user.
To Set Permissions select: Administrator Access.
Add tags if you wish to and create the user.
Download CSV File of the credentials of Access Key when prompted as it is essential for future steps. Incase you forget to save the Secret Access Key then once user is created, select the User and in Security Credentials tab, generate new Access Key and save it.
(Creating an IAM User can help you or maybe your team to access the project on the console without having to share the Root User credentials as every user created, gets a separate set of credentials assigned.)

![image](https://user-images.githubusercontent.com/61246381/164277830-b74c5ba6-b125-4bc7-ac69-37708b133153.png)
![image](https://user-images.githubusercontent.com/61246381/164278129-32bca770-c5b1-4c6b-b480-415008652cc5.png)


2.      Create an EC2 Instance. Make the following changes while creating an Instance. 
Choose AMI: Microsoft Windows Server 2022 Base (in Free Tier)
Instance Type: t2.micro
No change in Instance Details.
No change is Storage. Assigned storage is sufficient.
Add a tag: Key: Name
Value: instance_1 (name of instance you want)
Security Group Configuration: Add Rules: Custom TCP protocol and set port number to 8080. Add HTTP and HTTPS rules as well.	
When asked for Key Pair, select Create a new Key Pair. Name the Key Pair and create. A .pem file will be downloaded. Know the location of this file for further use.
Launch the instance
Go to EC2>>Instances and wait for the Instance State to display Running and Status Check to display 2/2 checks passed before proceeding.

![image](https://user-images.githubusercontent.com/61246381/164278959-c72d81f7-5d6c-4924-8d0a-6c3884fcd53e.png)

3.      Create RDP Connect.
Select the instance you created and click on Connect in the top panel.
 Navigate to the RDP Client section.
Click on Download remote desktop file, and a .rdp file will be downloaded.
In the password section, click on Get Password.
Here, browse and select the Key Pair file we downloaded in the previous step in .pem format. Click on Decrypt Password. You will be redirected to the previous page and will see the password.
Open the .rdp file now. Click on Connect in the pop-up. You will be asked to enter a password for the Administrator user. Copy the Decrypted password from the console and paste in the dialogue box and connect to the RDP client. Click on Yes if another pop-up appears.
As we have chosen Windows AMI, a VM will open up with Windows OS. Wait till you see the instance details on the Desktop of this VM before moving further. Select Refresh by right-clicking in the VM if you don’t see the details in the top right corner.
RDP Connection is now established.
To run this project, install Python and/or Xampp if you wish to check the SQL connectivity. You open the Apache and MySQL connection on Xampp, create a database by the name of text_summarizer in phpMyAdmin and import the .sql file.



![image](https://user-images.githubusercontent.com/61246381/164278985-fef50bbc-5c21-4ebe-a75b-ed79b27ae938.png)

4.      Connecting to [XAMPP](https://www.javatpoint.com/xampp) 
Start the Apache and [MySQL](https://www.javatpoint.com/mysql-tutorial) application through the XAMPP Control Panel. XAMPP Control Panel is a management tool that offers to supervise the actions of individual components of XAMPP. It controls each component of the text server. The user can initiate or halt discrete modules by operating upon the buttons below the "Actions" column. Control panels efficiently manage all the components of the XAMPP Package. One can use the Control Panel to determine whether Apache, MySQL, Mercury, etc. are currently in function or not. The development environment can only be used when Apache and MySQL are in running state. The XAMPP Control Panel icon exists in the system tray. It is an orange-colored icon that is visible when Panel is in running state.

![image](https://user-images.githubusercontent.com/61246381/164279405-a0446fec-2d4e-4922-ac0e-41cc2b68c5f2.png)


5.      Launching the project in the instance.
Copy and paste the required files into the dashboard folder of htdocs directory. 
To run the application, open the Google Chrome and open the following link : 3.110.164.108/dashboard/
Login using your username and password. If you don’t have an account then click on register.
Enter your details and create your profile. Go back to the login page and then login to your account,
You can choose from a list of exams created by the examiner. The examination begins. You are supposed to answer the multiple choice questions that appear within the stipulated time.
Once the timer runs out, the examination ends and you are shown the results of your tests immediately. Logout post viewing your result.

![image](https://user-images.githubusercontent.com/61246381/164279535-8f28537d-c631-4e1f-bf14-673d7946e62d.png)

![image](https://user-images.githubusercontent.com/61246381/164279980-fd6f8f9d-991e-4953-9e29-cdded28c4cd1.png)

![image](https://user-images.githubusercontent.com/61246381/164280039-1e0474af-437a-4fbe-8f79-e2cf55bdbe7b.png)

![image](https://user-images.githubusercontent.com/61246381/164280064-2a3504a5-4160-40b6-b2b2-1735b732da20.png)
