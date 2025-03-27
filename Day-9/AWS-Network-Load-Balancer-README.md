#### INSTRUCTOR DETAILS

|  Information             | Details                                                                      |
|----------------------    |------------------------------------------------------------------------------|
| **Name**                 | Moole Muralidhara Reddy                                                      |
| **Email**                | techworldwithmurali@gmail.com                                                |
| **Website**              | https://www.techworldwithmurali.com               |
| **LinkedIn profile**     | [Moole Muralidhara Reddy](https://www.linkedin.com/in/moole-muralidhara-reddy) |

### What is an AWS Network Load Balancer?

AWS Network Load Balancer (NLB) is a load balancing solution designed to handle high volumes of traffic with low latency. It operates at the transport layer (Layer 4) and is capable of handling millions of requests per second while maintaining ultra-low latencies.

### Benefits of an AWS Network Load Balancer

1. **High Throughput:** Handles millions of requests per second with ultra-low latencies.
2. **Static IP:** Provides a static IP address per Availability Zone (AZ) for easy integration with applications.
3. **TLS Termination:** Supports TLS termination for end-to-end encryption.
4. **Target Group Support:** Routes traffic to target groups using IP addresses and ports.
5. **Health Checks:** Performs health checks on targets to ensure only healthy targets receive traffic.
----
### Lab Session - Creation of an AWS Network Load Balancer

1. **Sign in to AWS Management Console:**
   - Navigate to the EC2 Dashboard at [AWS Management Console](https://console.aws.amazon.com/ec2/).

2. **Create Network Load Balancer:**
   - Click on "Load Balancers" in the left sidebar under "EC2."
   - Click on "Create Load Balancer" and choose "Network Load Balancer."
   - Configure load balancer settings, including listeners, availability zones, security settings, and target groups.
   - Complete the creation and note the DNS name provided for your Network Load Balancer.
----
### Lab Session - Deletion of an NLB

1. **Sign in to AWS Management Console:**
   - Navigate to the EC2 Dashboard at [AWS Management Console](https://console.aws.amazon.com/ec2/).

2. **Delete Network Load Balancer:**
   - Click on "Load Balancers" in the left sidebar under "EC2."
   - Select the Network Load Balancer you want to delete.
   - Click on "Actions > Delete" and confirm the deletion.
----

### Difference between an Application Load Balancer (ALB) and a Network Load Balancer (NLB)

| Feature                         | Application Load Balancer (ALB)                          | Network Load Balancer (NLB)                              |
|---------------------------------|----------------------------------------------------------|----------------------------------------------------------|
| **Layer**                       | Operates at Layer 7 (Application layer)                  | Operates at Layer 4 (Transport layer)                    |
| **Use Case**                    | Ideal for HTTP/HTTPS traffic and advanced routing        | Ideal for TCP, UDP, and TLS traffic requiring high performance |
| **Routing**                     | Supports advanced routing based on HTTP headers, paths, and hostnames | Routes traffic based on IP protocol data without inspection |
| **Performance**                 | Suitable for applications requiring intelligent routing decisions | High performance, low latency required for real-time applications |
| **Protocol Support**            | HTTP, HTTPS, WebSocket                                   | TCP, UDP, TLS                                            |
| **SSL Termination**             | Supports SSL termination                                 | Supports SSL passthrough and SSL termination             |
| **Target Type**                 | Can route to EC2 instances, IP addresses, Lambda functions | Can route to EC2 instances, IP addresses, and AWS PrivateLink endpoints |
| **Health Checks**               | Supports health checks based on HTTP/HTTPS status codes and content | Supports health checks based on TCP connections and responses |
| **WebSocket Support**           | Yes                                                      | No                                                       |
| **Sticky Sessions**             | Yes, using cookies                                       | No                                                       |
| **Host-based and Path-based Routing** | Yes                                                      | No                                                       |
| **Cost**                        | Generally more expensive due to advanced features        | Generally less expensive due to its simplicity and lower overhead |


----
### Lab Session - Attaching an ALB to a New Auto Scaling Group

1. **Sign in to AWS Management Console:**
   - Navigate to the EC2 Dashboard at [AWS Management Console](https://console.aws.amazon.com/ec2/).

2. **Create Auto Scaling Group (ASG):**
   - Click on "Auto Scaling Groups" in the left sidebar under "Auto Scaling."
   - Click on "Create Auto Scaling group" and follow the wizard to create a new Auto Scaling group.
   - Configure scaling policies, network settings, and tags.
   - Choose the existing Application Load Balancer (ALB) during the creation process to attach it to the Auto Scaling group.
----
### Lab Session - Attaching an ALB to an Existing Auto Scaling Group

1. **Sign in to AWS Management Console:**
   - Navigate to the EC2 Dashboard at [AWS Management Console](https://console.aws.amazon.com/ec2/).

2. **Modify Auto Scaling Group (ASG):**
   - Click on "Auto Scaling Groups" in the left sidebar under "Auto Scaling."
   - Select the Auto Scaling group to which you want to attach the Application Load Balancer (ALB).
   - Click on "Edit" and modify the ASG settings to attach the existing ALB.
   - Update the Auto Scaling group configuration to include the ALB and complete the modification process.

