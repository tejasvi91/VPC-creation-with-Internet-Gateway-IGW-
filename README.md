# VPC Creation with Internet Gateway (IGW)
## Overview

This guide outlines the process of creating a Virtual Private Cloud (VPC) in AWS, attaching an Internet Gateway (IGW) to allow internet access, and modifying key VPC settings such as enabling DNS hostnames.
![image](https://github.com/user-attachments/assets/b21dcb49-b2f7-4ea3-9c8c-7be24cbb56fa)

## Steps Involved

* Creating a VPC with a specified CIDR block.


  ![image](https://github.com/user-attachments/assets/4d03ed60-6d08-4f8d-9496-64867c6121f3)


  ![image](https://github.com/user-attachments/assets/e88974b0-a9e8-4a46-ba41-3f4743a7ca20)

* Enable DNS host names.

 Once VPC is created , go to __Actions__ , change we VPC settings and enable DNS settings as mentioned below

  Actions > edit vpc settings > DNS settings > enable DNS hostnames

__Note__: If we do not do so, then there will be no public access

  ![image](https://github.com/user-attachments/assets/2781bcdb-8dda-4e7d-aef5-6702e10cbba2)

  * Create subnet named App_servers.

  ![image](https://github.com/user-attachments/assets/fcdcfe05-a5b1-4e0f-b1ed-7ff4c68d7220)

 * Create subnet named Web_servers.
  ![image](https://github.com/user-attachments/assets/0b1e521b-438c-4fb1-9579-31882d1bed13)


  * Create subnet named DB_servers.
  ![image](https://github.com/user-attachments/assets/af656acb-6f8c-4d27-b7a0-562ee38c27c6)

  * Creating and Attaching an IGW to the VPC.




  ![image](https://github.com/user-attachments/assets/ae2843ee-e227-49ae-84b6-0a115e4a3c85)



  ![image](https://github.com/user-attachments/assets/a9b3b922-c439-43ab-a727-7545a37dc32d)



  ![image](https://github.com/user-attachments/assets/dc36b351-b687-45af-9037-a3dd3ca99132)










* Creating the route table.


  In this step, route tables to be created and select which are the subnets to be given internet access. In this case, all the subnets are included in the route table. 

![image](https://github.com/user-attachments/assets/721e800b-b423-4df9-aa40-fc9399f77e5a)

![image](https://github.com/user-attachments/assets/4aac96c9-339e-433c-b4f1-33cde02c7214)

![image](https://github.com/user-attachments/assets/b17f1784-959a-463e-bef2-56de1d29d037)

__Note__: In the above image we see that in __edit routes__, we are giving access to all traffic or public ip's like 0.0.0.0/0 . This is done only in personal projects like here for testing purpose. In real time it is not recommended. 

![image](https://github.com/user-attachments/assets/a0210ceb-5762-48a1-bbba-3f5593eb886b)

Here we are selecting all the subnets which are to be given internet access. 

![image](https://github.com/user-attachments/assets/5a3dae33-700e-49d5-9809-035d5b32de39)


## How to Use

1. Clone the repository:

     git clone <repository_url>

2. Navigate to the project folder and follow the instructions for setting up your VPC in AWS.

> [!NOTE]
> Please do not forget to delete all the resourcs like VPC when done.
> ALL this can be achieved in AWS free tier account







