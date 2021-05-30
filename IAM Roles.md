# Creating IAM Roles

![image](https://user-images.githubusercontent.com/20463821/120115104-1f494b00-c17a-11eb-94aa-b04b4c095fd9.png)

## Tasks
1. Log into AWS Management Console.

2. Create IAM Role for EC2 service

3. Create IAM Role for DynamoDB service.

- Sign-in to AWS Management Console
- Go to IAM and click on **Roles** on the navigation pane to the left and **Create role** button 

![image](https://user-images.githubusercontent.com/20463821/120115335-2755ba80-c17b-11eb-8150-987f437a1b9c.png)

- Select a use case **EC2 instance** and click on **Permissions** button and **Tags** button

![image](https://user-images.githubusercontent.com/20463821/120115410-6be15600-c17b-11eb-8d69-fb9a18d9cb87.png)

- Add a tag, to give a brief information about the IAM role, then click on **Review** button

![image](https://user-images.githubusercontent.com/20463821/120115510-e0b49000-c17b-11eb-9664-2758f0ef53f8.png)

- Under Review page, provide the necessary information and click on the **Create role** button

![image](https://user-images.githubusercontent.com/20463821/120115572-3426de00-c17c-11eb-8669-e3c6917f7be0.png)

- To create role for DynamoDB service, repeat the previous steps above, select **DynamoDB** as the use case

![image](https://user-images.githubusercontent.com/20463821/120115695-d5ae2f80-c17c-11eb-9263-fdea43050129.png)

- Review the information and click on **Create role** button

![image](https://user-images.githubusercontent.com/20463821/120115745-042c0a80-c17d-11eb-86ad-ad5241f1c464.png)

- A list of the available IAM roles on the root account is displayed

![image](https://user-images.githubusercontent.com/20463821/120115774-2b82d780-c17d-11eb-876e-fcf249e8d985.png)

I have been able to create 2 IAM roles for EC2 instance and DynamoDB.
