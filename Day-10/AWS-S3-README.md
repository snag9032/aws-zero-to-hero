#### INSTRUCTOR DETAILS

|  Information             | Details                                                                      |
|----------------------    |------------------------------------------------------------------------------|
| **Name**                 | Moole Muralidhara Reddy                                                      |
| **Email**                | techworldwithmurali@gmail.com                                                |
| **Website**              | https://www.techworldwithmurali.com               |
| **LinkedIn profile**     | [Moole Muralidhara Reddy](https://www.linkedin.com/in/moole-muralidhara-reddy) |

### What is AWS S3:
1. **Definition**: Amazon S3 is a simple storage service offering durable, highly available, and scalable data storage infrastructure at low costs.
2. **Object Storage**: It is a key-based object store.
3. **File Upload**: Allows uploading files ranging from 0 bytes to 5TB each.
4. **Scalability**: Offers unlimited storage capacity.
5. **Bucket Storage**: Files are stored in containers called buckets.
6. **Key Structure**: Keys (object identifiers) can mimic hierarchical structures.
7. **Data Accessibility**: Enables storing and retrieving any amount of data from anywhere on the internet.
8. **Global Unique Names**: Operates with a universal namespace; bucket names must be globally unique.
9. **DNS Name**: Each bucket has a DNS name for access (e.g., `https://s3-eu-east-2.amazonaws.com/bucket_name`).

### Bucket:
1. **Object Container**: Buckets are containers for storing objects.
2. **Hierarchy**: Does not provide object hierarchy natively but uses object key names (prefixes) to simulate folders.
3. **Folder Simulation**: Users can create folders within buckets using object key names.
4. **Nested Buckets**: Nested buckets are not supported.
5. **URL Access**: Bucket names are part of the URL for accessing stored objects.
6. **Region Specific**: Each S3 bucket is specific to a region.
7. **Global Name Uniqueness**: Names must be globally unique due to S3's universal namespace.
8. **Logging**: Supports enabling logging to track access and usage.

### Objects in Bucket:
- **Definition**: Objects are individual items stored in an S3 bucket.
- **Characteristics**: Each object has a unique key and can store data up to 5TB, along with optional metadata.
- **Hierarchy**: Objects are organized using unique keys, often resembling file paths, to simulate folder structures.
- **Access**: Accessed via URLs incorporating bucket names and object keys (e.g., `https://s3.amazonaws.com/bucket_name/object_key`).
- **Operations**: Common operations include upload, download, copy, delete, and list, managed via AWS SDKs, CLI, or AWS Management Console.
----
### Types of Storage Classes in AWS S3

1. **Standard:** Provides high durability, availability, and performance for frequently accessed data.
2. **Intelligent-Tiering:** Automatically moves objects between two access tiers based on changing access patterns.
3. **Standard-IA (Infrequent Access):** For data that is accessed less frequently but requires rapid access when needed.
4. **One Zone-IA:** Lower-cost option for infrequently accessed data that doesn't require multiple Availability Zone resilience.
5. **Glacier and Glacier Deep Archive:** For archival data with retrieval times ranging from minutes to hours.

----
### Lab Session - Create an S3 Bucket

1. **Sign in to AWS Management Console:**
   - Navigate to the S3 Dashboard at [AWS Management Console](https://s3.console.aws.amazon.com/s3/).

2. **Create S3 Bucket:**
   - Click on "Create bucket."
   - Enter a unique bucket name and choose a region.
   - Configure optional settings like versioning, logging, and tags.
   - Review and create the bucket.
----
### Lab Session - Upload Objects to S3 using the AWS Console

1. **Sign in to AWS Management Console:**
   - Navigate to the S3 Dashboard at [AWS Management Console](https://s3.console.aws.amazon.com/s3/).

2. **Upload Objects:**
   - Select the bucket to which you want to upload objects.
   - Click on "Upload" and select files from your local machine.
   - Configure upload options and permissions as needed.
   - Upload the files to the S3 bucket.
----
### Lab Session - Upload Objects to S3 using the AWS CLI

1. **Open Command Line Interface:**
   - Open a terminal or command prompt on your local machine.

2. **Upload Objects using AWS CLI:**
   - Use the `aws s3 cp` command to copy files to S3:
     ```bash
     aws s3 cp <local_file_path> s3://<bucket_name>/<remote_file_name>
     ```
   - Optionally, use `aws s3 sync` for syncing directories:
     ```bash
     aws s3 sync <local_directory> s3://<bucket_name>/<remote_directory>
     ```
----
### S3 Versioning and Enabling it

- **Versioning:** Keeps multiple variants of an object in the same bucket.
- **Enable Versioning:**
   - Sign in to AWS Management Console.
   - Navigate to S3 Dashboard.
   - Select the bucket and click on "Properties."
   - Under "Advanced settings," enable versioning.
----
### Bucket Policy in Amazon S3

- **Bucket Policy:** JSON-based access policy applied at the bucket level to manage permissions.
- **Working with Bucket Policy for S3 Bucket:**
   - Define permissions for who can access (e.g., IAM users, roles, or specific IP ranges).
   - Define actions allowed (e.g., read, write, delete).
   - Apply conditions for access (e.g., based on IP address, user agent).
----
### Lab Session - Working with the Bucket Policy for S3 Bucket

1. **Sign in to AWS Management Console:**
   - Navigate to the S3 Dashboard at [AWS Management Console](https://s3.console.aws.amazon.com/s3/).

2. **Configure Bucket Policy:**
   - Select the bucket and click on "Permissions."
   - Click on "Bucket Policy" and enter or modify the JSON policy document.
   - Use AWS policy generator to generate a policy based on requirements.
   - Review and apply the policy to manage access to the S3 bucket.

