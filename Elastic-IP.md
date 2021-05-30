# Allocate Elastic-IP and Associate to EC2-instance

![image](https://user-images.githubusercontent.com/20463821/120119917-2bd99d80-c192-11eb-9df9-e17b63eabeb0.png)

## Tasks
1. Log into AWS Management Console.

2. Create an Amazon Linux Instance from an Amazon Linux AMI

3. Find your instance in the AWS Management Console.

4. SSH into your instance and configure your server as a web server.

5. Create and publish a sample test.html file.

6. Test the page with the public IP address of EC2 Instance created.

7. Allocate an Elastic IP and associate it to the EC2 Instance.

8. Test the page with Elastic IP address of EC2 Instance.

- Sign-in to AWS Management Console
- Create and launch an EC2 instance
- SSH into the instance 

![image](https://user-images.githubusercontent.com/20463821/120122401-6ba78180-c1a0-11eb-9934-405f919020ae.png)

- Configure a Webserver such as Nginx
- Run update on the os `sudo yum update`
- To install nginx on Amazon Linux 2 AMI `sudo amazon-linux-extras install nginx1`
- Start nginx service after installation `sudo systemctl start nginx`
- Verify the service is active `sudo systemctl status nginx`

![image](https://user-images.githubusercontent.com/20463821/120122561-6e56a680-c1a1-11eb-81e9-a672a2f1d8d1.png)

- Enable port 80 in the security group of the instance on AWS Console

![image](https://user-images.githubusercontent.com/20463821/120122612-c7bed580-c1a1-11eb-848a-3caf2c9e1e1e.png)

- Confirm port 80 is accessible, run `curl http://localhost:80` on the terminal
- You can also search on the browser http://public-ip:80

![image](https://user-images.githubusercontent.com/20463821/120122709-4f0c4900-c1a2-11eb-95af-51b75ce342ca.png)

- Create a root web directory `sudo mkdir /var/www/test` and create an index file test.html `sudo vi test.html` in the test directory. 
- Edit nginx.conf file in /etc/nginx directory `sudo vi nginx.conf` and change the root to /var/www/test in the first server block and indicate the index points to test.html file, save file using **:wq**

![image](https://user-images.githubusercontent.com/20463821/120123718-65b59e80-c1a8-11eb-965d-6668e265aef0.png)

- Reload nginx service `sudo systemctl reload nginx`, so that the system will register the changes made 
- Reload browser which will reveal the content of the test.html file created.

![image](https://user-images.githubusercontent.com/20463821/120123773-baf1b000-c1a8-11eb-9559-41ea7bcffc55.png)

## Allocate Elastic-IP 
- On the AWS console, under **Services** dropdown menu, select *Networking & Content Delivery* > VPC

![image](https://user-images.githubusercontent.com/20463821/120123896-6ac71d80-c1a9-11eb-80f1-789d2ad1c3c7.png)

- Select **Elastic IPs** and click on *Allocate IP address* button

![image](https://user-images.githubusercontent.com/20463821/120123957-b24da980-c1a9-11eb-8188-cca039179305.png)

- Click on **Allocate** button

![image](https://user-images.githubusercontent.com/20463821/120124043-17090400-c1aa-11eb-89f8-6e9b53e53659.png)

- Confirm the elastic IP has been created successfully and click on **Associate this Elastic IP address** button

![image](https://user-images.githubusercontent.com/20463821/120124067-44ee4880-c1aa-11eb-8a00-6ac116c42ceb.png)

- Allocate to EC2 instance created, and you can specify a private ip if you want, click on **Associate** button

![image](https://user-images.githubusercontent.com/20463821/120124139-b8905580-c1aa-11eb-8db5-afb515d57d13.png)

- The Elastic IP address has been associated successfully

![image](https://user-images.githubusercontent.com/20463821/120124175-f9886a00-c1aa-11eb-8453-1368b1459bd1.png)

- Confirm and test the webpage with the Elastic IP address of the EC2 instance `54.159.202.129`

![image](https://user-images.githubusercontent.com/20463821/120124225-3f453280-c1ab-11eb-841c-577fdc7e3119.png)


I was able to create an EC2 instance, connect to it using SSH, install nginx webserver, load a static web page on it, also created an Elastic IP address and associated it with the EC2 instance created





