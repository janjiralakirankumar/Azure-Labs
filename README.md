## Lab-01: Step-by-Step Guide for Creating a Linux Virtual Machine and Deploying Nginx Using Azure:

### Creating a Virtual Machine in Azure for Linux:

1. **Azure Sign-in:**
   - Start by signing in to the Azure portal using your Azure account. Visit [https://portal.azure.com](https://portal.azure.com) to access the portal.

2. **Resource Creation:**
   - Click on "Create a resource" on the left-hand menu to initiate the virtual machine creation process.

3. **Search for Ubuntu Server:**
   - Directly select `Ubuntu Server 20.04 LTS`, or use the search bar to look for "Ubuntu Server." Choose `Ubuntu Server 20.04 LTS` from Canonical and click `Create`.

4. **Project Details**:
   - Configure the following:
     - **Subscription**: Choose your Azure subscription (ensuring it supports the free tier if applicable).
     - **Resource group**: Create a new `resource group` or select an existing one (with a unique name). For a new group, click "Create new" and name it, e.g., `Demo-RSG-YourName`.

5. **Virtual Machine Name**:
   - Specify a name for your VM, e.g., `Demo-LinuxVM-YourName`.

6. **Region**:
   - Leave it as the default (e.g., East US) or choose a region near your location for optimal performance.

7. **Availability options**:
   - Keep this setting as `No infrastructure redundancy required`.

8. **Image**:
   - Ensure "Ubuntu Server 20.04 LTS" is selected (it might be pre-selected).

9. **Size**:
   - Choose a size: `"B1s" (1 vCPU, 1 GB RAM)" to stay within the free tier limits.

10. **Authentication type**:
    - Select "SSH public key."

11. **SSH public key source**:
    - Choose `Generate a new key pair` and name it, e.g., `DemoKeyPair-YourName`, or use an existing one.
    - In the `Select inbound ports` section, choose `SSH (22)` and `HTTP (80)`.

12. Click "Next: Disks."

13. **Disks**:
    - Use the default OS disk size (usually 30 GiB).
    - For the OS disk type, select "Standard SSD" for improved performance.

14. Click "Next: Networking."

15. **Networking**:
    - Keep the default settings for the following:
    - **Virtual network**: Create a new virtual network or use an existing one.
    - **Subnet**: Create a new subnet or use an existing one (e.g., "default").
    - **Public IP**: Create a new public IP address.
    - For the NIC network security group, choose "Basic."
    - Select "SSH (22) and HTTP (80)" for public inbound ports.

16. Click "Next: Management" > "Monitoring" > "Advanced" > "Tags" > "Review + Create."

17. **Review + Create**:
    - Review the settings to ensure they comply with best practices and free tier limits.
    - Click "Create" to start provisioning the VM.
    - Download the new key pair by clicking "Download private key and create resource."

18. **Deployment Process**:
    - Monitor the deployment progress in the Azure portal. Once the VM is deployed, click "Go to Resources."

19. **Connect to Your Linux VM**:
    - Choose the `Connect` option from the left-hand menu.
    - Under "Most Common," select `Native SSH` and click "Select."
    - In "Option 3," click the copy icon to copy the Connect Command.
    - Open PowerShell, navigate to the directory with the private key (e.g., Downloads), and paste the command.
    - Example:
   ```bash
   ssh -i ~/.ssh/id_rsa.pem azureuser@172.190.132.28
   ```
   - Replace `~/.ssh/id_rsa.pem` with your Key Pair Name (e.g., `DemoKeyPair-YourName.pem`) and press Enter.
   - This establishes a connection to your VM. To verify the Internet connection, use the command `ping google.com` (stop with `Ctrl+C`).

20. This confirms your connection to the Linux VM and checks the Internet connection.

### Installing Nginx on a Linux VM (e.g., Ubuntu):

Before Installing Nginx, Copy the Public IP and paste it into a new tab in your browser to see that it does not display a web page.

1. **Update Package Lists**:
   - As a best practice, update package lists to ensure you install the latest software. Run this command:

   ```bash
   sudo apt update
   ```

2. **Install Nginx**:
   - Use the package manager to install Nginx. Execute this command:

   ```bash
   sudo apt install nginx
   ```

3. **Start Nginx**:
   - After the installation, start Nginx with this command:

   ```bash
   sudo systemctl start nginx
   ```

4. **Enable Nginx to Start on Boot**:
   - Ensure Nginx starts automatically when the VM reboots using this command:

   ```bash
   sudo systemctl enable nginx
   ```

5. **Check the Status of Nginx**:
   - Verify that Nginx is running smoothly. Use this command:

   ```bash
   sudo systemctl status nginx
   ```

   This command displays the status and other information about the Nginx service.

6. **Open a Web Browser and Access the Default Web Page**:
   - Open a new browser tab and enter your Linux VM's public IP address.
   - For instance, if the VM's public IP address is "12.34.56.78," enter it as http://12.34.56.78.
   - You should see the default Nginx welcome page, confirming Nginx installation and operation on your VM.

You have now successfully installed Nginx on your Linux VM and accessed the default web page. Further configuration can be done to host web content or applications as needed.

---

## Lab-02: Step-by-Step Guide for Creating a Windows Virtual Machine and Deploying Nginx Using Azure:

### Creating a Virtual Machine in Azure for Windows Server:

1. **Azure Sign-in:**
   - Begin by signing in to the Azure portal using your Azure account. Access the portal at [https://portal.azure.com](https://portal.azure.com).

2. **Resource Creation:**
   - Click on "Create a resource" in the left-hand menu to initiate the virtual machine creation process.

3. **Search for Windows Server:**
   - In the search bar, type "Windows Server." Select an appropriate Windows Server version (e.g., Windows Server 2022 Datacenter - x64 Gen 2) and click `Create`.

4. **Project Details**:
   - Configure the following:
     - **Subscription**: Choose your Azure subscription.
     - **Resource Group**: Create a new `resource group` (e.g., `Demo-RSG-YourName`) or use an existing one.

5. **Virtual Machine Name**:
   - Specify a name for your VM, e.g., `

Demo-WindowsVM-YourName`.

6. **Region**:
   - Leave it as the default (e.g., East US) or choose a region near your location for optimal performance.

7. **Availability Options**:
   - Keep this setting as `No infrastructure redundancy required`.

8. **Image**:
   - Ensure "Windows Server 2022 Datacenter - x64 Gen 2" is selected, or select it.

9. **Size**:
   - Choose a size: `"B1s" (1 vCPU, 1 GB RAM)" to stay within the free tier limits.

10. **Authentication Type** (Choose only if available or leave it):
    - Select "Password."

11. **Username and Password**:
    - Enter a `username` and `password` for your Windows VM. Ensure it's strong and secure.

12. **Inbound Port Rules**:
    - In `Select inbound ports`, choose "RDP (3389)" and "HTTP (80)."

13. Click "Next: Disks."

14. **Disks**:
    - Use the default OS disk size (usually 127 GiB).
    - For the OS disk type, select "Standard SSD" for better performance.

15. Click "Next: Networking."

16. **Networking**:
    - Keep the default settings:
    - Create a new virtual network and subnet if necessary.
    - Create a new public IP address or use an existing one.
    - Keep the network security group as "Basic."
    - Select "RDP (3389)" and "HTTP (80)" for public inbound ports.

18. Click "Next: Management" > "Monitoring" > "Advanced" > "Tags" > "Review + Create."

19. **Review + Create**:
    - Review the settings to ensure they comply with your requirements.
    - Click "Create" to start the VM provisioning process.

20. **Deployment Process**:
    - Azure will start deploying your Windows VM. Monitor the progress in the Azure portal.

21. **Connect to Your Windows VM**:
    - Once the VM is deployed, choose the `Connect` option from the left-hand menu.
    - Under "Most Common," select `Native RDP` and click "Select."
    - In "Option 3," click "Download RDP File" to download the RDP file.
    - Use the RDP file to connect to your Windows VM using the provided username and password.
    - Test the features and exit.

22. **Resizing a Windows Server Virtual Machine (VM) in Microsoft Azure**

To meet your resource requirements and performance:

1. **Select the Virtual Machine**:
   - In the Azure portal, navigate to the virtual machine that you want to resize.

2. **Stop the Virtual Machine** (if it's running):
   - Before you can resize a VM, it needs to be in a stopped (deallocated) state.
   - If the VM is running, select it, and click the "Stop" button on the top menu. Follow the prompts to confirm the stop action.

3. **Resizing the Virtual Machine**:
   - With the VM in the stopped state, select the VM again in the Azure portal.
   - In the left-hand menu, scroll down to the "Settings" section and click on "Size."

4. **Choose a New VM Size**:
   - You'll see a list of available VM sizes. Choose the size that best fits your requirements. Each size has information about the number of CPU cores, RAM, and other specifications.
   - Click the new size you want to use and click "Resize" to apply the change.

5. **Start the Virtual Machine**:
   - Once the size change is applied, start the VM by selecting it and clicking the "Start" button.

6. **Connect to the VM**:
   - After the VM has started with the new size, you may need to connect to it using your preferred method, such as Remote Desktop (RDP) for Windows.

7. **Monitor Performance**:
   - Keep an eye on the VM's performance to ensure it meets your needs with the new size. You can use Azure Monitor or other monitoring tools to assess the VM's resource utilization.

**Note**: Choose a size that aligns with your specific workload requirements. Additionally, be aware that some VM sizes are only available in certain regions, so ensure the size you want is available in your selected region.

---
## Lab 03: Detailed Steps for Creating an Azure Blob Storage:

**Step 1: Create an Azure Storage Account**

1. Log in to the Azure Portal (https://portal.azure.com) using your Azure account.

2. Click on "Create a resource" in the left-hand menu. This is where you start creating new Azure resources.

3. In the search bar, type "Storage account" and select "Storage account" from the search results.

4. Click the "Create" button to start the storage account creation process.

5. You'll need to fill in some information:

   - **Subscription:** Choose your Azure subscription (typically a free trial or a paid subscription).
   
   - **Resource group:** Create a new resource group with a descriptive name or select an existing one. A resource group helps you organize related Azure resources.

   - **Storage account name:** This should be a unique name that identifies your storage account. It can only contain lowercase letters and numbers.

   - **Location:** Choose a region closest to your location or where you want your storage to be hosted.

   - **Performance:** For lab purposes, you can select "Standard" for general-purpose storage.

   - **Replication:** Choose "Locally Redundant Storage (LRS)" for cost-effective redundancy, which stores data in a single region.

   - **Secure transfer required:** Enable this option to ensure data is transferred securely.

   - **Networking:** For lab purposes, select "Public endpoint (all networks)."

6. Click "Review + Create" to review your settings and ensure they are correct.

7. After reviewing, click "Create" to start the provisioning process. It might take a few minutes for your storage account to be created.

**Step 2: Access and Configure Blob Storage**

1. After your storage account is created, go to the "Storage accounts" section in the Azure Portal.

2. Click on your newly created storage account.

3. In the left-hand menu, under the "Settings" section, click on "Containers."

4. Create a new container by clicking the "+ Container" button.

5. Provide a name for the container. It's best to use lowercase letters and hyphens (e.g., "my-container").

6. Configure the public access level to "Private." This ensures that only authorized users can access the contents of the container.

7. Optionally, set metadata for the container. Metadata can be used to store additional information about the container, such as its purpose or description.

**Step 3: Uploading and Managing Blobs**

1. Click on the container you created in the previous step.

2. To upload a blob, click the "Upload" button.

3. Choose a file from your local computer to upload to the container. (For example, you can select an image file or a text document.)

4. While uploading blobs, consider giving them meaningful names and organizing them into virtual directories within the container.

**Step 4: Access Blob Storage via Azure SDKs and Tools**

1. To interact with your Azure Blob Storage programmatically, you can use various SDKs and tools.

2. Install the Azure SDK for your preferred programming language. For example, if you are using Python, you can install the Azure SDK for Python.

3. Configure authentication to access your Azure Storage account. You can use the storage account connection string, SAS tokens, or other authentication methods.

4. Use the SDK to connect to your Azure Storage account and perform operations like uploading, downloading, and deleting blobs.

   Example (Python):

   ```python
   from azure.storage.blob import BlobServiceClient

   connection_string = "your_connection_string"
   blob_service_client = BlobServiceClient.from_connection_string(connection_string)
   container_client = blob_service_client.get_container_client("your_container_name")
   blob_client = container_client.get_blob_client("your_blob_name")
   ```

**Step 5: Security and Access Control**

1. Implement shared access signatures (SAS) for granular access control. SAS tokens allow you to define permissions and expiration times for specific actions on a blob or container.

2. Consider role-based access control (RBAC) to manage access to your storage account. RBAC allows you to assign specific roles to users or applications.

**Step 6: Monitoring and Analytics**

1. Enable metrics and diagnostics logging for your storage account to monitor its performance and keep track of activities.

2. Set up Azure Monitor and create alerts for critical events, such as high blob read or write operations or security breaches.

3. Review the Azure Storage Analytics, which provides insights into how your storage account is being used.

4. You can use additional tools like Azure Log Analytics and Application Insights for advanced monitoring and analysis.

**Step 7: Cleanup**

1. After completing your lab, it's essential to delete the resources to avoid incurring unnecessary costs.

2. Delete the storage account, containers, and blobs you created during the lab. You can do this by going to the respective resource and clicking the "Delete" option.

By following these detailed steps with explanations, beginners can create an Azure Blob Storage lab, learning the fundamentals of Azure Blob Storage and its best practices for security and efficiency.

---
