# Configure-Azure-Bastion

### What is Azure Bastion?
Azure Bastion is a fully managed platform-as-a-service (PaaS) by Microsoft that provides secure RDP and SSH connectivity to your virtual machines directly through the Azure portal. It eliminates the need to expose VMs to the public internet by working over a private IP within your virtual network. Azure Bastion helps protect against threats like port scanning and brute-force attacks, since VMs don’t need public IPs or open management ports. It provides a browser-based experience, simplifies network security, and can integrate with Azure Active Directory for identity-based access controls.
### Key Benefits:
No public IP required on your VMs.

Secure access via the Azure portal using TLS (Transport Layer Security).

Protection against port scanning and other threats, since RDP/SSH ports (like 3389 and 22) aren't exposed to the internet.

Browser-based access, no need for a remote desktop client.

Integration with Azure AD, for better identity-based access control (with certain configurations).

### How Azure Bastion Works?
Deploy Azure Bastion inside your Virtual Network (VNet).

It creates a private, secure connection between the Azure portal and your VM.

Access your VM directly from the Azure portal using RDP or SSH, without requiring a public IP address.

### When to Use Azure Bastion?
When you need secure, browser-based access to VMs.

To eliminate exposure of RDP/SSH ports to the internet.

When you want simplified management without configuring VPNs or jump servers.

Limitations 
Only supports browser-based connections (No direct RDP/SSH client support).

Higher cost compared to using a public IP with NSG restrictions.

Cannot be used across VNets unless peered with an appropriate configuration.

### Summary: Configuring Azure Bastion for Secure VM Access
In this project, I created a Virtual Network (VNet) with a subnet, reserving an additional subnet for Azure Bastion. After setting up a Virtual Machine (VM) within the subnet, I configured Azure Bastion to enable secure, browser-based RDP/SSH access without exposing the VM to the internet. This setup ensures a secure, hassle-free connection without the need for a public IP.

### Step-1
i. Create a Virtual Network (VNet) and configure a subnet with a /26 IP address range to allocate 64 IP addresses.

![Capture1](https://github.com/user-attachments/assets/1be083e3-f58b-4729-80ea-181b7f8fbc2c)

ii.Create a <strong>Virtual Machine (VM)</strong> and associate it with the <strong>subnet</strong> you created within the <strong>Virtual Network (VNet)</strong>.

![Capture2](https://github.com/user-attachments/assets/1faf0680-8f0f-46a1-8af1-f75cab97d628)

### Step-2
i. Once the VM is created, click on the Connect button, then select Connect using Bastion.

![Capture3](https://github.com/user-attachments/assets/c5d8ecb0-9919-42d7-bddd-aad9645ee183)

ii. Now, click on Deploy Bastion to set up the Azure Bastion service for secure VM access.

![Capture4](https://github.com/user-attachments/assets/f7387a02-d928-42be-adda-82f35b15d8dd)

iii. Enter your username and password, then click on the Connect button to access the VM securely through Azure Bastion.

![Capture5](https://github.com/user-attachments/assets/045adbae-6f31-4d04-bfeb-fb4b389ee49a)

iv. Now, you will see that the VM is successfully connected using Azure Bastion, providing a secure, browser-based RDP/SSH session without exposing the VM to the internet. 🚀

![Capture6](https://github.com/user-attachments/assets/d482ebae-744c-43b9-8cb4-144ed8cc7cd7)





