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

