## Detailed and step-by-step guide for creating a virtual machine in Azure, both for Linux and Windows.

**Creating a Virtual Machine in Azure for Linux (Detailed Steps for Students):**

1. **Sign in to Azure:**
   - Sign in to the Azure portal (https://portal.azure.com) using your Azure account.

2. **Create a Resource:**
   - Click on "Create a resource" on the left-hand menu.

3. **Search for Ubuntu or CentOS:**
   - In the search bar, type "Ubuntu" or "CentOS."
   - Select the Linux distribution you want (e.g., "Ubuntu Server 20.04 LTS").

4. **Basics:**
   - **Resource group**: Create a new resource group or use an existing one.
   - **Virtual machine name**: Provide a unique name for your VM.
   - **Region**: Choose a region close to your location.
   - **Availability options**: Leave the default settings.
   - **Image**: The selected Linux distribution (e.g., "Ubuntu Server 20.04 LTS").
   - **Size**: Choose a size based on your needs.
   - **Authentication type**: Select "Password" or "SSH public key."
   - **Username**: If using SSH, provide a username.
   - **Password/SSH public key**: Enter your password or SSH public key based on your choice.

5. **Disks:**
   - **OS disk type**: Leave as "Standard HDD" for cost-effective options.
   - **Size (GiB)**: Configure the OS disk size if needed (e.g., 30 GB).

6. **Networking:**
   - **Virtual network**: Create a new virtual network or use an existing one.
   - **Subnet**: Choose or create a subnet.
   - **Public IP**: Create a new one for your VM.
   - **NIC network security group**: You can leave this as "Basic."
   - **Public inbound ports**: Select SSH (22) if you're using SSH.

7. **Management**:
   - **Boot diagnostics**: Enable this option for troubleshooting.
   - **OS guest diagnostics**: Leave this as "On."
   - **Enable auto-shutdown**: Optionally, set a time for auto-shutdown to save costs.

8. **Advanced**:
   - You can skip this section for basic setup.

9. **Tags**:
   - You can add tags for organization and categorization (optional).

10. **Review + Create**:
    - Review the settings you've configured, ensuring they are correct.
    - Click "Create" to start provisioning the VM.

11. **Deployment**:
    - Azure will begin deploying the Linux VM. Monitor the deployment progress in the Azure portal.

12. **Connect to Your Linux VM**:
    - Once the VM is provisioned, go to the VM's details in the Azure portal.
    - Find the public IP address to connect to your Linux VM using SSH.

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
