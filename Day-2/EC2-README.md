#### INSTRUCTOR DETAILS

|  Information             | Details                                                                      |
|----------------------    |------------------------------------------------------------------------------|
| **Name**                 | Moole Muralidhara Reddy                                                      |
| **Email**                | techworldwithmurali@gmail.com                                                |
| **Website**              | https://www.techworldwithmurali.com               |
| **LinkedIn profile**     | [Moole Muralidhara Reddy](https://www.linkedin.com/in/moole-muralidhara-reddy) |

### What is Amazon EC2?

Amazon EC2 (Elastic Compute Cloud) is a web service that provides resizable compute capacity in the cloud. It allows you to obtain and configure virtual servers (known as instances) to run your applications, scalable depending on your needs.

### Features of Amazon EC2

1. **Scalability:** Easily scale compute resources up or down as needed.
2. **Variety of Instances:** Choose from various instance types optimized for different use cases (e.g., compute-optimized, memory-optimized).
3. **Security:** Secure instances with built-in security groups and key pairs.
4. **Flexible Pricing:** Pay only for the compute capacity you actually use.
5. **Integration:** Easily integrate with other AWS services and third-party tools.
----
### Amazon EC2 Instance Types and Use Cases

Amazon EC2 offers a variety of instance types to cater to different workloads and performance needs. Here are some common instance types along with their use cases:

1. **General Purpose Instances (e.g., M5, T3)**
   - **Description**: These instances offer a balance of compute, memory, and networking resources.
   - **Use Cases**: 
     - Web servers
     - Small databases
     - Development environments

2. **Compute-Optimized Instances (e.g., C5, C6g)**
   - **Description**: These instances are optimized for compute-intensive workloads.
   - **Use Cases**:
     - High-performance computing
     - Scientific modeling
     - Batch processing

3. **Memory-Optimized Instances (e.g., R5, X1)**
   - **Description**: These instances are optimized for memory-intensive workloads.
   - **Use Cases**:
     - In-memory databases
     - Big data analytics
     - High-performance computing

4. **Storage-Optimized Instances (e.g., D2, I3)**
   - **Description**: These instances are optimized for storage-intensive workloads.
   - **Use Cases**:
     - NoSQL databases
     - Data warehousing
     - Elasticsearch

5. **GPU Instances (e.g., G4, P3)**
   - **Description**: These instances provide access to high-performance GPUs for graphics-intensive workloads.
   - **Use Cases**:
     - Video rendering
     - Machine learning
     - Gaming

6. **FPGA Instances (e.g., F1)**
   - **Description**: These instances are designed for the acceleration of custom hardware logic.
   - **Use Cases**:
     - Genomics analysis
     - Financial modeling
     - Real-time video processing

### Key Points

- **Instance Sizes**: Each instance type is available in different sizes, offering varying amounts of CPU, memory, storage, and networking capacity.
- **Customizable**: Users can select the instance type and size that best suits their specific workload requirements.
----
### Lab Session - Creation of a Linux EC2 Instance

1. **Sign in to AWS Management Console:** Navigate to the EC2 Dashboard.
2. **Launch Instance:** Click on "Launch Instance" to start the instance creation process.
3. **Choose AMI:** Select a Linux-based Amazon Machine Image (AMI) such as Amazon Linux or Ubuntu.
4. **Choose Instance Type:** Select an instance type based on your requirements (e.g., t2.micro for a free-tier eligible instance).
5. **Configure Instance:** Configure instance details, storage, tags, and security groups.
6. **Review and Launch:** Review your instance configuration and launch it.
7. **Connect to Instance:** Use SSH to connect to your Linux instance (details for connecting will vary based on your operating system).
----
### Lab Session - Downloading PuTTY and PuTTYgen

PuTTY is a popular SSH client for Windows, while PuTTYgen is used to generate and convert SSH keys.

1. **Download PuTTY:** Go to the PuTTY download page and download the PuTTY installer.
2. **Download PuTTYgen:** Download PuTTYgen from the same page.
3. **Install PuTTY:** Run the PuTTY installer and follow the installation instructions.
4. **Run PuTTYgen:** Launch PuTTYgen to generate or convert SSH keys as needed.

### Lab Session - Convert PEM to PPK file

To convert a PEM file (typically used in Linux) to a PPK file (used in PuTTY for Windows):

1. **Open PuTTYgen:** Launch PuTTYgen.
2. **Load PEM Key:** Click on "Load" and select your PEM file.
3. **Save Private Key:** Click on "Save private key" to save the key in PPK format.
----
### Lab Session - Connecting to Linux server

Use SSH to connect to your Linux server:

1. **Open Terminal (Linux/Mac) or PuTTY (Windows):** Launch your SSH client.
2. **SSH Command:** Use the SSH command with the instance's public IP address or DNS name and your private key file:
   ```
   ssh -i /path/to/private-key.pem ec2-user@public-ip-address
   ```
   Replace `/path/to/private-key.pem` with the path to your PEM file, `ec2-user` with your instance's username (may vary by AMI), and `public-ip-address` with your instance's public IP address or DNS.

----
### Lab Session - Creation of a Windows EC2 Instance

1. **Sign in to AWS Management Console:**
   - Navigate to the EC2 Dashboard at [AWS Management Console](https://console.aws.amazon.com/ec2/).

2. **Launch Instance:**
   - Click on "Launch Instance" to start the instance creation process.

3. **Choose AMI:**
   - In the "Step 1: Choose an Amazon Machine Image (AMI)" section, click on "AWS Marketplace" on the left sidebar.
   - Search for "Windows Server" and select a suitable Windows Server AMI. Ensure you choose a version that suits your requirements (e.g., Windows Server 2019 Base).

4. **Choose Instance Type:**
   - Select an instance type based on your requirements (e.g., t2.micro for a free-tier eligible instance). Click "Next: Configure Instance Details" when ready.

5. **Configure Instance:**
   - Configure instance details such as:
     - Number of instances to launch.
     - Network settings (usually default VPC and subnet settings are fine).
     - Optionally, configure advanced settings like IAM role, monitoring, and instance shutdown behavior. Click "Next: Add Storage" when ready.

6. **Add Storage:**
   - Specify the storage requirements for your instance. The default settings are typically sufficient for basic needs. Click "Next: Add Tags" when ready.

7. **Add Tags:**
   - Optionally, add tags to your instance for easier identification and management. Click "Next: Configure Security Group" when ready.

8. **Configure Security Group:**
   - Configure security group settings to control inbound and outbound traffic to your instance. At least allow RDP (Remote Desktop Protocol) access (port 3389) for Windows instances. You may also want to allow HTTP (port 80) or HTTPS (port 443) depending on your application needs.

9. **Review Instance Launch:**
   - Review all your instance details. Ensure everything is configured correctly. Click "Launch" when ready.

10. **Select Key Pair:**
    - In the pop-up window, select an existing key pair or create a new key pair. Note that for Windows instances, you typically do not need to use SSH keys directly. Instead, you will use RDP to connect.

11. **Access Windows Instance:**
    - Once the instance is launched, note the public IP address or DNS name of your instance from the EC2 dashboard.

12. **Connect to Windows Instance:**
    - Use Remote Desktop Protocol (RDP) to connect to your Windows instance. On your local machine:
      - Search for "Remote Desktop Connection" in the Start menu (Windows).
      - Enter the public IP address or DNS name of your instance. Click "Connect."
      - Enter the credentials (username and password) specified during instance launch.

13. **Start Using Windows Instance:**
    - You are now connected to your Windows EC2 instance. Start configuring Windows settings, installing applications, and exploring the capabilities of Windows on AWS.
----

### Lab Session - Create an AMI from an Amazon EC2 Instance

1. **Select Instance:** In the EC2 Dashboard, select the instance you want to create an AMI from.
2. **Actions > Image and templates > Create image (AMI):** Click on "Actions," then "Image and templates," and finally "Create image (AMI)."
3. **Enter Image Details:** Provide a name and description for your AMI.
4. **Create Image:** Click "Create image" to initiate the AMI creation process.
5. **Use AMI:** Once created, you can use this AMI to launch new instances with the same configuration as the original instance.

