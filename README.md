## What is Linux? ##
Linux is an open-source operating system kernel that serves as the foundation for various Linux distributions, such as Ubuntu, CentOS, Debian, and Fedora. 
It was initially developed by Linus Torvalds in 1991 and has since gained popularity and widespread adoption.

## Why is it popular? ##
There are several reasons why Linux is popular:

1. Open Source: Linux is open-source software, which means its source code is freely available for anyone to view, modify, and distribute. 
This fosters a collaborative development model and allows individuals and organizations to customize and contribute to the operating system.

2. Stability and Reliability: Linux is known for its stability and reliability. It is designed to handle heavy workloads and can run for long periods without the need for rebooting. This makes it suitable for mission-critical applications and production environments.

3. Security: Linux has a reputation for being more secure than some other operating systems. The open-source nature of Linux allows security vulnerabilities to be identified and patched quickly by the community. Additionally, Linux provides robust security features, such as user access controls, file permissions, and built-in firewall capabilities.

4. Flexibility and Customizability: Linux offers a high degree of flexibility and customizability. Users can choose from various distributions and customize the operating system to meet their specific needs. Linux also supports a wide range of hardware architectures, making it versatile for different use cases.

5. Cost-effective: Linux is generally free to use, which makes it a cost-effective choice for businesses and individuals. 
There are no licensing fees associated with the operating system itself, and many Linux distributions come with a wide range of free and open-source software applications.

6. Scalability: It is very light-weight and secure. 
## Why is it used for production servers so often? ##

Linux is commonly used for production servers due to several reasons:

1. Stability and Performance: Linux's stability, reliability, and efficient resource management make it well-suited for server environments. It can handle high workloads and run 24/7 without performance degradation.

2. Scalability: Linux scales well, allowing businesses to easily add or remove resources as needed. It can efficiently handle large-scale server deployments and accommodate growing demands.

3. Server Software Support: Linux has extensive support for various server applications, frameworks, and technologies.

## Steps in creating an instance ##

1. Name and tags: use tech254_bolutife_nginx
![img_2.png](img_2.png) 
2. Application and OS images: Browse more AMIs, Community AMIs, then search 18.04 lts 1e9, select ubuntu from the two options
![img_3.png](img_3.png)
3. Instance type: choose t2.micro( resources being used)
4. Key pair login : use tech254
5. ensure the .pen file is on .ssh folder
6. Edit security group under network settings. change security group name to tech254_bolutife_basesg

Copy the same thing to the description group.
![img_4.png](img_4.png)
7. Inbound security group rules; select ssh for the first one; and source type being anywhere
8. Add security group rule. Under the security group rule, choose HTTP; source type anywhere.
9. Security group rule 3: Add HTTPS; source type: anywhere
![img_6.png](img_6.png)
10. Configure storage: no change required. 
11. Select launch an instance. Under instance summary, copy public ip address
![img_8.png](img_8.png) ![img_9.png](img_9.png)
12. Instance summary page
![img_7.png](img_7.png)
## Gitbash steps
1. $ cd .ssh : To locate the pem folder in .ssh
2. $ chmod 400 tech254.pem : Used to change mode; change permissions
3. Open your connect to instance page, select SSH client. Copy the ubuntu command and type $ ssh -i "tech254.pem"link(starting from ubuntu)
confirming the identity. Press enter
4. Are you sure u want to connect? yes. Copy the address below. 
![img_10.png](img_10.png) ubuntu@ip-172-31-53-162:~$

5.  To check that you are in the right gitbash and you are now using linux,
type $ ls then $uname
ubuntu@ip-172-31-53-162:~$ uname
Linux
ubuntu@ip-172-31-53-162:~$

6. $ sudo apt update : finds the apps that need to be updated. 
7. $ sudo apt upgrade -y : Implements the updates, and ensures the latest version are installed. 
8. $ sudo apt install nginx -y
9. $ sudo systemct1 start nginx
10. $ sudo systemct1 status
