WEB STACK IMPLEMENTATION (LEMP STACK)

What is LEMP STACK?
LEMP is a variation of the ubiquitous LAMP stack used for developing and deploying web applications. Traditionally, LAMP consists of Linux, Apache, MySQL, and PHP. Due to its modular nature, the components can easily be swapped out. With LEMP, Apache is replaced with the lightweight yet powerful Nginx.

LEMP stands for Linux, Nginx, MySQL, PHP or Python, or Perl.

Preparing Prerequisites

Spinning up a new EC2 instance (an instance of a virtual server) is only a matter of a few clicks.

You can follow the instructions below to get yourself set up:

1) Register a new AWS account following this instruction.
2) Select your preferred region (the closest to you) and launch a new EC2 instance of t2.micro family with Ubuntu Server 20.04 LTS (HVM)

Important

Linux Linux is the operating system for this stack, and the flavor we will be using is Ubuntu.

Installling an OS

We will be utilising AWS service (Elastic Cloud Computing - EC2 instance) to create a server. To access this feature, you need to first create an account with AWS or sign in if you have an existing account


![](images/awslaunch.png)

Click "Launch a virtual machine"

Type in the search bar Ubuntu Sever 20.01 LTS (HVM), SSD, click select.

![](images/searchubuntu.png)

Next, keep highlighted the selection in the image, and scroll down and click "Review and Launch"

![](images/step2.png)

On the next page click "Launch"

![](images/step7launch.png)

Create and save your key-pair pem file in a secure and accessible location. This will be needed to access your server from your local machine. Click "Download Key Pair" and then click "Launch Instances"

![](images/keypair.png)

Click what's highlighted in red. Please note your number will be different.

![](images/launchinstance.png)
![](images/ins.png)

Connecting to your EC2 instance using Terminal

- Change directory into the loacation where your `PEM` file is. Most likely will be in the **Downloads** folder

`cd ~/Downloads`

**IMPORTANT** - Anywhere you see these anchor tags **< >** , going forward, it means you will need to replace the content in there with values specific to your situation. For example, if we need you to replace the name you have saved the private key on your machine, we will write something like **< private-key-name >**.

If the private key you downloaded was named **my-private-key.pem** simply remove the anchor tags and insert **my-private-key.pem** in the command you are required to execute. Lets try this and follow the instructions below to get some work done.

- Change premissions for the private key file (.pem), otherwise you can get an error “Bad permissions”

`sudo chmod 0400 <private-key-name>.pem`

- Connect to the instance by running

`ssh -i <private-key-name>.pem ubuntu@<Public-IP-address>`

Congratulations! You have just created your very first Linux Server in the Cloud and our set up looks like this now: (You are the client)

![](images/connectec2.png)