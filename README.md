## Detailed and step-by-step guide for creating a virtual machine in Azure, both for Linux and Windows.

**Creating a Virtual Machine in Azure for Linux (Detailed Steps for Students):**

Certainly, I'll provide a detailed step-by-step guide for students to create a virtual machine in Azure, including the input fields following best practices that consider the free tier for resources where applicable. This guide will focus on creating a virtual machine for a Linux-based environment.

**Creating a Virtual Machine in Azure for Linux (Free Tier and Best Practices):**

1. **Sign in to Azure:**
   - Sign in to the Azure portal (https://portal.azure.com) using your Azure account.

2. **Create a Resource:**
   - Click on "Create a resource" on the left-hand menu.

3. **Search for Ubuntu Server:**
   - In the search bar, type "Ubuntu Server."
   - Select "Ubuntu Server" from Canonical and click "Create."

4. **Basics**:

   - **Subscription**: Choose your Azure subscription (ensure it's a subscription that supports the free tier if available).
   - **Resource group**: Create a new resource group or use an existing one (keep resource group names unique).
   - **Virtual machine name**: Enter a unique name for your VM.
   - **Region**: Choose a region (e.g., East US) near your location for better performance.
   - **Availability options**: Keep this as "No infrastructure redundancy required."
   - **Image**: Select "Ubuntu Server 20.04 LTS."
   - **Size**: Choose a size that fits within the free tier limits, such as "B1s" (1 vCPU, 1 GB RAM).
   - **Authentication type**: Select "SSH public key."
   - **SSH public key**: Paste your public SSH key for secure access.

5. **Disks**:
   - **OS disk type**: Choose "Standard SSD" for better performance (the free tier doesn't have specific disk limitations).
   - **Size (GiB)**: Use the default size, which is often 30 GB.

6. **Networking**:
   - **Virtual network**: Create a new virtual network or use an existing one.
   - **Subnet**: Create a new subnet or use an existing one (e.g., "default").
   - **Public IP**: Create a new public IP address.
   - **NIC network security group**: Choose "Basic."
   - **Public inbound ports**: Select "SSH (22)."

7. **Management**:
   - **Boot diagnostics**: Enable this for troubleshooting.
   - **OS guest diagnostics**: Leave this as "On."
   - **Enable auto-shutdown**: Configure an auto-shutdown time to save costs (e.g., daily at 6:00 PM).

8. **Advanced**:
   - This section is optional, and you can skip it.

9. **Tags**:
   - Add tags to categorize your resources if desired (e.g., Name: MyLinuxVM).

10. **Review + Create**:
    - Review the settings to ensure they align with best practices and free tier limits.
    - Click "Create" to initiate the VM provisioning process.

11. **Deployment**:
    - Azure will start deploying your Linux VM. Monitor the progress in the Azure portal.

12. **Connect to Your Linux VM**:
    - After deployment, go to the VM's details in the Azure portal.
    - Find the public IP address to connect to your Linux VM using SSH. 

By following these detailed steps, students can create a Linux-based virtual machine in Azure while adhering to best practices and, where applicable, taking advantage of the free tier resources. This exercise will provide students with practical experience in deploying resources on Azure.

---
**Creating a Virtual Machine in Azure for Windows (Detailed Steps for Students):**

The steps for creating a Windows VM are similar to the Linux VM creation process, with some differences:

1. **Sign in to Azure:**
   - Access the Azure portal at https://portal.azure.com.

2. **Create a Resource:**
   - Click on "Create a resource" in the left-hand menu.

3. **Search for Windows Server:**
   - In the search bar, type "Windows Server."
   - Select the Windows Server version you prefer (e.g., "Windows Server 2019").

4. **Basics:**
   - Follow the same basic steps as for a Linux VM but provide the following details:
     - **Username**: A username for your Windows VM.
     - **Password**: A strong password.

5. **Disks:**
   - Follow the same disk configuration steps as in the Linux VM creation process.

6. **Networking:**
   - Configure the network settings, virtual network, subnet, and public IP address just as in the Linux setup.

7. **Management**:
   - Configure monitoring, management, and auto-shutdown as needed, similar to the Linux setup.

8. **Advanced**:
   - Customize advanced settings if necessary, but this section is typically optional.

9. **Tags**:
   - You can add tags for better organization, but this is optional.

10. **Review + Create**:
    - Review your settings and ensure they are correct.
    - Click "Create" to start the VM provisioning process.

11. **Deployment**:
    - Azure will start deploying your Windows VM. Monitor the progress in the Azure portal.

12. **Connect to Your Windows VM**:
    - After deployment, go to the VM's details in the Azure portal.
    - Find the public IP address and connect to your Windows VM using a Remote Desktop client, providing the username and password you configured during VM creation.

This detailed guide should help students create both Linux and Windows virtual machines in Azure with precise instructions on what to select and enter in each field. It's a practical exercise that allows them to gain hands-on experience with Azure VM deployment.
