#### INSTRUCTOR DETAILS

|  Information             | Details                                                                      |
|----------------------    |------------------------------------------------------------------------------|
| **Name**                 | Moole Muralidhara Reddy                                                      |
| **Email**                | techworldwithmurali@gmail.com                                                |
| **Website**              | https://www.techworldwithmurali.com               |
| **LinkedIn profile**     | [Moole Muralidhara Reddy](https://www.linkedin.com/in/moole-muralidhara-reddy) |

### What is VPC Peering?

- **VPC Peering** is a networking connection between two Virtual Private Clouds (VPCs) that allows you to route traffic between them using private IP addresses.
- Instances in either VPC can communicate with each other as if they are within the same network.
- VPC peering allows for seamless communication across different VPCs, whether they are in the same account, different accounts, or even different regions (inter-region VPC peering).

### VPC Peering Key Points

1. You can create a VPC peering connection between:
   - Your own VPCs.
   - A VPC in another AWS account.
   - A VPC in a different AWS Region.

2. A VPC peering connection is a one-to-one relationship between two VPCs.

3. You can create multiple VPC peering connections for each VPC.

4. Transitive peering relationships are not supported.

5. You can modify a VPC peering connection to enable instances in your VPC to communicate with linked EC2-Classic instances in the peer VPC.

6. There is no single point of failure for communication or a bandwidth bottleneck.

7. A VPC peering connection helps facilitate the transfer of data.

8. The traffic remains in the private IP space.

![VPC Peering Diagram - Tech World with Murali - Moole Muralidhara Reddy.png](https://github.com/techworldwithmurali/aws-zero-to-hero/blob/main/Day-15/images/Day%2015-VPC%20Peering%20Diagram%20-%20Moole%20Muralidhara%20Reddy%20-%20Tech%20World%20with%20Murali.png)

### Types of VPC Peering

1. **Intra-Account VPC Peering**:
  -  Intra-region VPC peering within the same AWS account
  -  Intra-region VPC peering within the different AWS account
   
2. **Inter-Account VPC Peering**:
  -  Inter-region VPC peering within the same AWS account
  -  Inter-region VPC peering within the different AWS account

![Types of VPC Peering - Tech World with Murali - Moole Muralidhara Reddy.png](https://github.com/techworldwithmurali/aws-zero-to-hero/blob/main/Day-15/images/Day%2015-Types%20of%20VPC%20Peering%20-%20Moole%20Muralidhara%20Reddy%20-%20Tech%20World%20with%20Murali.png)
