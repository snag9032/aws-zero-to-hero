#### INSTRUCTOR DETAILS

|  Information             | Details                                                                      |
|----------------------    |------------------------------------------------------------------------------|
| **Name**                 | Moole Muralidhara Reddy                                                      |
| **Email**                | techworldwithmurali@gmail.com                                                |
| **Website**              | https://www.techworldwithmurali.com               |
| **LinkedIn profile**     | [Moole Muralidhara Reddy](https://www.linkedin.com/in/moole-muralidhara-reddy) |

### Access Control List (ACL) in Amazon S3:
- **Purpose**: ACLs define who can access your buckets and objects and what level of access they have (read, write, etc.).
- **Types**: S3 supports both bucket-level and object-level ACLs.
- **Permissions**: ACLs can grant permissions to AWS accounts or predefined groups (e.g., authenticated users, everyone).
- **Granularity**: Object ACLs can be more granular than bucket ACLs, allowing specific permissions per object.
- **Management**: ACLs can be managed using AWS Management Console, AWS CLI, or SDKs.
- **Alternatives**: S3 also supports more flexible and recommended access management through Bucket Policies and IAM policies.

ACLs provide a straightforward way to control access to your S3 resources based on specific needs and security requirements.

----
### Lab Session - Apply ACL for S3 Bucket

1. **Sign in to AWS Management Console:**
   - Navigate to the S3 Dashboard at [AWS Management Console](https://s3.console.aws.amazon.com/s3/).

2. **Apply ACL for S3 Bucket:**
   - Select the bucket for which you want to modify ACL.
   - Click on "Permissions."
   - Under "Access control list (ACL)," configure permissions for specific AWS accounts or users.
   - Choose permissions like read, write, or full control.
----

### Amazon S3 (Simple Storage Service) bucket lifecycle

- Amazon S3 (Simple Storage Service) bucket lifecycle management allows you to manage your objects so that they are stored cost-effectively throughout their lifecycle.
- You can define lifecycle rules to transition objects between different storage classes or to expire objects after a specified period.

### Key Concepts

1. **Lifecycle Configuration**: A set of rules that define actions (transition or expiration) on a group of objects within an S3 bucket.

2. **Storage Classes**: Different storage classes like STANDARD, INTELLIGENT_TIERING, STANDARD_IA (Infrequent Access), ONEZONE_IA, GLACIER, and DEEP_ARCHIVE.

3. **Transition Actions**: Moving objects to a different storage class.

4. **Expiration Actions**: Deleting objects after a specified period.

### Creating a Lifecycle Rule

1. **Log in to AWS Management Console**:
   Go to the S3 service.

2. **Select the Bucket**:
   Choose the bucket you want to configure.

3. **Go to the Management Tab**:
   Navigate to the "Management" tab in the bucket's properties.

4. **Lifecycle Rules**:
   Click on "Lifecycle" and then "Add lifecycle rule."

5. **Configure Rule**:
   - **Rule Name**: Give your rule a meaningful name.
   - **Scope**: Choose if the rule applies to all objects or to a subset of objects (prefix or tags).

6. **Set Transition Actions**:
   - Add transitions to move objects to different storage classes. Specify the number of days after object creation when the transition should occur.
   - Example: Move objects to STANDARD_IA after 30 days and to GLACIER after 365 days.

7. **Set Expiration Actions**:
   - Define when objects should be deleted (e.g., 365 days after creation).
   - Optionally, set clean-up options for incomplete multipart uploads.

8. **Review and Create**:
   Review your rule configurations and create the lifecycle rule.

----
### Hosting a Static Website using Amazon S3

1. **Sign in to AWS Management Console:**
   - Navigate to the S3 Dashboard at [AWS Management Console](https://s3.console.aws.amazon.com/s3/).

2. **Hosting a Static Website:**
   - Select the bucket you want to use for hosting.
   - Click on "Properties" and then "Static website hosting."
   - Enable static website hosting and configure index and error documents.
   - Note the endpoint URL provided for accessing your static website.

----
### Presigned URLs in AWS S3

**Presigned URLs:** URLs that grant temporary access to download or upload a specific S3 object with a specified expiration time.

### Lab Session - Working with Presigned URLs in AWS S3
 **Generate Presigned URL (Download):**
   - Use AWS SDK or AWS CLI to generate a presigned URL for an object.
   - Example using AWS CLI:
     ```bash
     aws s3 presign s3://<bucket_name>/<object_key> --expires-in 3600
     ```
   - This URL allows temporary access to download the object for one hour.

----

### Server-side Encryption for Amazon S3 Buckets:
- **Definition**: It encrypts objects stored in S3 buckets at the server level, ensuring data confidentiality.
- **Types**:
  - **SSE-S3**: Server-side encryption with Amazon S3-managed keys (SSE-S3). AWS manages and rotates keys automatically.
  - **SSE-KMS**: Server-side encryption with AWS Key Management Service (SSE-KMS). Provides additional control over encryption keys, including key management and auditing.
  - **SSE-C**: Server-side encryption with customer-provided keys (SSE-C). Allows you to manage your own encryption keys outside of AWS.
- **Encryption Process**: Objects are encrypted before being written to disks and decrypted when retrieved.
- **Management**: Encryption settings can be configured at the bucket level or applied to individual objects.
- **Benefits**: Enhances data security and compliance with encryption standards without requiring changes to applications.
- **Usage**: Managed via AWS Management Console, AWS CLI, or SDKs, providing flexibility in implementation and management.

Server-side encryption ensures that data stored in Amazon S3 remains protected against unauthorized access, providing a critical layer of security for sensitive information.

----

### Lab Session - Delete an S3 Bucket

1. **Sign in to AWS Management Console:**
   - Navigate to the S3 Dashboard at [AWS Management Console](https://s3.console.aws.amazon.com/s3/).

2. **Delete an S3 Bucket:**
   - Select the bucket you want to delete.
   - Click on "Actions > Delete bucket."
   - Confirm the deletion.

