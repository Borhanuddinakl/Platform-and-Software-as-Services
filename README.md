# Platform-and-Software-as-ServicesAssessment Title

AWS Practical Concepts Evaluation

DCE01: Platform and Software as Services

DCE-01 | Assessment-1.2

(Question and Answers)

Cover page

Prepared by: Md Borhan Uddin

Prepared for: Ovesh Vohra

Content

Task 1: Deploying a Domain Controller in the Cloud.........................................................5

EC2 Instance.................................................................................................................5

Domain Name...............................................................................................................5

VPC Name.....................................................................................................................6

Task 2: Setting Up a Sample Website on the Domain Controller.......................................7

Configure a sample website on your Domain Controller instance. ...................................8

Use the AWS Management Console and log in with the root user credentials from your registered AWS account to complete this setup .............................................................9

Task 3: Configuring Client Instances for Domain Authentication.....................................11

Create two additional EC2 instances, naming them CL-1 and CL-2.................................12

Configure both instances to join the domain set up on your Domain ..............................12

Task 4: Setting Up Shared File Storage. ........................................................................13

Use Amazon FSx to create file storage...........................................................................14

Connect this storage to the Microsoft Active Directory Service from Task 1, ensuring directory-controlled access.........................................................................................14

Task 5: Accessing Shared Storage Across Instances......................................................15

b) Access this folder from CL-2 using the shared storage configuration and capture a screenshot to verify that both machines can interact with the shared directory..............16

Task 6 brief explanation................  ....................................................................17,18,19

Task1:

A) Create and configure a Virtual Private Cloud (VPC) with a public subnet to host this server.

b) Deploy a Microsoft Windows Server 2016 instance as a Domain Controller with an Elastic IP in your AWS environment, specifically within the ap-southeast-2 (Sydney) region.

Submission: Follow the naming conventions below and include below screenshots:

• EC2 Instance: 

• Domain Name: 

• VPC Name: 

Task 2:

a) Configure a sample website in your Domain Controller instance. Using AWS services, ensure the website is accessible only from your registered IP address.

b) Use the AWS Management Console and log in with the root user credentials from your registered AWS account to complete this setup.

Submission: website 

Website accessible:

Security group:

Website not accessible:

Security group:

Website accessible again:

Task3:

a) Create two additional EC2 instances, naming them CL-1 and CL-2.

b) Configure both instances to join the domain set up on your Domain Controller created in Task-1.

Domain Cl1and Cl2:

Task4:

a) Use Amazon FSx to create file storage, configuring the storage with options that fit Yoobee’s needs.

b) Connect this storage to the Microsoft Active Directory Service from Task 1, ensuring directory-controlled access

Task 5:

a) Create a folder named aws on CL-1.

b) Access this folder from CL-2 using the shared storage configuration and capture a screenshot to verify that both machines can interact with the shared directory.

Task 6:

Task 1: Deploying a Domain Controller in the Cloud

This task involves setting up a Microsoft Windows Server 2016 as a Domain Controller in AWS. The domain controller is responsible for managing authentication and access control for users and resources in the network. What i did is 

First i Created a Virtual Private Cloud (VPC) to provide a secure network environment.

Then deployed an EC2 instance with Windows Server 2016 and configuring it as a Domain Controller.

Assigning a public IP to ensure the server has a static public IP for accessibility.

This task is crucial because it establishes centralized identity management for the organization and enhances security by managing user authentication in the cloud.

Task 2: Setting Up a Sample Website on the Domain Controller

The purpose of this task is to set up a web service on the domain controller to demonstrate secure access to a hosted application. The key steps that i have done is 

First Configuring a web server (IIS) on the domain controller.

Then Deploying a basic website on the IIS server.

Restricting access to a specific IP address to control who can access the website.

This helps in understanding access control mechanisms in AWS and ensures that internal applications are secure and accessible only by authorized users.

Another key takeaway from this task is learning how to leverage AWS security mechanisms, such as IAM policies, network ACLs, and security groups, to define access control rules. 

Task 3: Configuring Client Instances for Domain Authentication

This task involves setting up two EC2 instances CL-1 and CL-2 as client machines and making them join the Active Directory domain configured in Task 1. The process includes:

We need to Create EC2 instances with CL1 and CL2 then configuring network settings.

Joining the domain using Active Directory credentials.

Verifying authentication to confirm that clients can access resources using domain-based authentication.

This ensures that all users and devices are centrally managed, improving security and operational efficiency in a cloud-based environment.

One key benefit of this setup is that IT administrators can centrally manage user access without needing to configure authentication on each individual machine. If an employee leaves the organization, their access can be revoked centrally without requiring manual intervention on every client device.

Task 4: Setting Up Shared File Storage

The process begins with creating an FSx file system in AWS and configuring it to join the existing domain set up in Task 1. FSx is specifically designed for Windows workloads, providing a native file-sharing solution with full compatibility with NTFS file systems and Windows ACL. In this task what i did was 

First, we need to create an FSx file system in AWS.

Then we Integrated FSx with Active Directory for securing access control.

Configuring permissions to allow specific users to access shared storage.

This task is important because shared storage improves collaboration while maintaining security and controlled access to files.

Task 5: Accessing Shared Storage Across Instances

This task will explain how multiple users can access and share files across client machines in the domain. In this step 

First, we created a shared folder on CL-1 with aws and configuring proper permissions

Accessing the shared folder from CL-2, ensuring domain-based authentication.

Testing file sharing to confirm both clients can access and modify shared files.

The shared storage configuration also demonstrates real-world use cases such as file-sharing across departments, collaborative editing, and centralized data management. AWS FSx ensures data redundancy, automated backups, and integration with cloud security policies, enhancing reliability and auditing. By using Active Directory authentication, IT administrators can track user activities, enforce permissions, and prevent unauthorized access to sensitive data
