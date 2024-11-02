# Launch and Access Windows EC2 Instance via RDP with Private Keypair

## Aim
To launch a Windows EC2 instance and access it using an RDP client from any network or specified network using a private keypair.

## Procedure

1. **Open EC2 Console**  
   Go to the [Amazon EC2 console](https://console.aws.amazon.com/ec2/).

2. **Launch Instance**  
   From the dashboard, click on **Launch Instance**.

3. **Select Amazon Machine Image (AMI)**  
   - On the **Choose an Amazon Machine Image (AMI)** page, select an AMI for **Windows Server 2016 Base** or later (marked "Free tier eligible").

4. **Choose Instance Type**  
   - Select **t2.micro** (eligible for the free tier) as the instance type.
   - If **t2.micro** is unavailable in your region, select **t3.micro** under the free tier.

5. **Review and Launch**  
   - On the **Choose an Instance Type** page, click **Review and Launch** to proceed with default configurations.

6. **Configure Security Group**  
   - On the **Review Instance Launch** page, under **Security Groups**, choose **Edit security groups**.
   - Select **Choose an existing security group** and pick the security group created during setup, then proceed to **Review and Launch**.

7. **Launch Instance**  
   - Click **Launch** on the **Review Instance Launch** page.

8. **Select Key Pair**  
   - When prompted, select **Choose an existing key pair** and choose the RSA key pair created during setup. (Note: Windows instances do not support ED25519 keys.)

9. **Confirm Launch**  
   - After confirming, click **View Instances** to return to the console.

10. **Check Instance Status**  
    - Go to the **Instances** page to check the launch status. It may take a few minutes for the instance to reach the **running** state and receive a public DNS name.

11. **Connect Using RDP**  
    - Once the instance is in the **running** state, use an RDP client with the instance's public DNS and key pair to connect.



## Notes
- It may take a few minutes for the instance to initialize fully.
- Ensure that **RDP** access is allowed in the selected security group.

