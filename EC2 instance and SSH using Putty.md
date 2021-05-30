# Launching EC2 instance and SSH using putty

![image](https://user-images.githubusercontent.com/20463821/120117067-46f0e100-c183-11eb-97d9-ccd4cf33c050.png)

## Tasks
1. Log into AWS Management Console.

2. Launch an Amazon Linux Instance from an Amazon Linux AMI 2

3. Find your instance in the AWS Management Console.

4. SSH into your instance for Mac Users.

5. SSH into your instance for Windows Users.

6. Run a few other helpful commands.

- Sign-in to AWS Managemnet Console
- On the Console Home, select **EC2**

![image](https://user-images.githubusercontent.com/20463821/120117389-dba80e80-c184-11eb-890c-1cbbdaf642b7.png)

- Select on *Instances* on the Navigation pane and click on **Launch instances** button 

![image](https://user-images.githubusercontent.com/20463821/120117506-743e8e80-c185-11eb-8422-334c1c168c0b.png)

- Select Amazon Linux 2 AMI base image

![image](https://user-images.githubusercontent.com/20463821/120117555-a3550000-c185-11eb-8335-45fc55f6cbc8.png)

- Leave the rest of the configuration as default and add a name tag

![image](https://user-images.githubusercontent.com/20463821/120117601-de573380-c185-11eb-8db3-fff5bdbd20c4.png)

- Create a security group and open 22 ie SSH

![image](https://user-images.githubusercontent.com/20463821/120117635-09418780-c186-11eb-85b0-939698038b89.png)

- Click on **Review and Launch button** then **Launch** button

![image](https://user-images.githubusercontent.com/20463821/120117681-3db54380-c186-11eb-9d0f-03b578e5931a.png)

- Prompts you to create a key pair or choose an existing key pair and click on **Launch instances** button

![image](https://user-images.githubusercontent.com/20463821/120117704-5d4c6c00-c186-11eb-8f82-38879d84b20c.png)

- View instances and confirm the instance created is up and running

![image](https://user-images.githubusercontent.com/20463821/120117750-984e9f80-c186-11eb-82d0-958517352975.png)

## Convert key to .ppk
- As a windows user, download and install PuTTY https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html 
- Locate the key pair (.pem file) downloaded from AWS, convert it to .ppk file using PuTTYgen
- Search for PuTTYgen from **Start** menu and launch
- Under Type of key to generate, choose RSA and click on **Load** to choose the .pem file, change file type to **All files**

![image](https://user-images.githubusercontent.com/20463821/120118011-355e0800-c188-11eb-8326-7e04c6d1c831.png)

- After the .pem file has been selected, a notice is displayed

![image](https://user-images.githubusercontent.com/20463821/120118138-fa100900-c188-11eb-8470-34e69cadb743.png)

- Click on **Save private key** button and click on **Yes**, to create without passphrase and save the putty file with the same name as the .pem file but with a new extension

## Connect to the Linux instance
- Search for PuTTY on start menu

![image](https://user-images.githubusercontent.com/20463821/120118348-00eb4b80-c18a-11eb-8af1-88d341c20d7b.png)

- Provide the public DNS of the instance, which can be found in the instance details using `instance-username@public-DNS`

![image](https://user-images.githubusercontent.com/20463821/120118464-8d960980-c18a-11eb-8649-c9dc72503a9b.png)

![image](https://user-images.githubusercontent.com/20463821/120118756-0d70a380-c18c-11eb-96fd-1e23893babb3.png)

- Under Category > Connection > SSH > Auth, choose the .ppk file using the **Browse** button
- A window showing connection to the instance is displayed

![image](https://user-images.githubusercontent.com/20463821/120118806-5e809780-c18c-11eb-9726-5f1e4fe873bc.png)

I have been able to successfully create an instance and connect using PuTTY


