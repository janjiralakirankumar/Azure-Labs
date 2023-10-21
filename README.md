## Lab-01: Step-by-Step Guide for Creating a Linux Virtual Machine and Deploying Nginx Using Azure:

### Creating a Virtual Machine in Azure for Linux:

1. **Sign in to Azure:**
   - Sign in to the Azure portal (https://portal.azure.com) using your Azure account.

2. **Create a Resource:**
   - Click on "Create a resource" on the left-hand menu.

3. **Search for Ubuntu Server:**
   - Directly select `Ubuntu Server 20.04 LTS` (Or)
   - In the search bar, type "Ubuntu Server" Select `Ubuntu Server 20.04 LTS` from Canonical and click `Create`.

4. **Project details**:

   - **Subscription**: Choose your Azure subscription (ensure it's a subscription that supports the free tier if available).
   - **Resource group**: Create a new `resource group` or use an existing one (keep resource group names unique).
     - (To create a new one, click on `Create new` and enter the name as `Demo-RSG-YourName`).

5. **Virtual machine name**:
   - Enter a name for your VM (e.g., `Demo-LinuxVM-YourName`).

6. **Region**:
   - Leave it as Default (e.g., East US) (Or)
   - Choose a region near your location for better performance.

7. **Availability options**:
   - Keep this as `No infrastructure redundancy required`.

8. **Image**:
   - Select "Ubuntu Server 20.04 LTS" (leave it if already selected).

9. **Size**:
   - Choose a size `"B1s" (1 vCPU, 1 GB RAM)` that fits within the free tier limits.

10. **Authentication type**:
    - Select "SSH public key".
  
11. **SSH public key source**:
    - Choose `Generate new key pair` and Enter the name as `DemoKeyPair-YourName`(Or) Use an existing one.
    - **Inbound port rules:** In `Select inbound ports` Choose `SSH (22)` and `HTTP (80)`

12. Click on `Next: Disks`.

13. **Disks**:
    - **OS disk Size (GiB)**: Use the default size, often 30 GiB.
    - **OS disk type**: Choose "Standard SSD" for better performance.

14. Click on `Next: Networking`.

15. **Networking**:
Leave all settings as Default for below.

    - **Virtual network**: Create a new virtual network or use an existing one.
    - **Subnet**: Create a new subnet or use an existing one (e.g., "default").
    - **Public IP**: Create a new public IP address.
    - **NIC network security group**: Choose "Basic".
    - **Public inbound ports**: Select "SSH (22) and HTTP (80)".
  
16. Click on `Next: Management` > `Monitoring` > `Advanced` > `Tags` > `Review + Create`.

17. **Review + Create**:
    - Review the settings to ensure they align with best practices and free tier limits.
    - Click `Create` to initiate the VM provisioning process.
    - Click on `Download private key and create resource` to download the new key pair.

18. **Deployment Process**:
    - Azure will start deploying your Linux VM. Monitor the progress in the Azure portal.
    - Once Deployed click on `Go to Resources`.

19. **Connect to Your Linux VM**:

    -choose the `Connect` option from the left-hand side.
    - under Most Common, Choose `Native SSH` and Click on `Select`
    - In `Option 3` click on the Copy Icon to copy the Connect Command.
    - Open PowerShell, choose the path where the Private key is available (e.g., Downloads), and paste the command.
    - Example:
   ```bash
   ssh -i ~/.ssh/id_rsa.pem azureuser@172.190.132.28
   ```
   - Replace your Key Pair Name (e.g., `DemoKeyPair-YourName.pem`) in place of `~/.ssh/id_rsa.pem` and press Enter.
   - Now, you are connected to your VM, and to check the Internet connection, enter the command `ping google.com` and press Enter (`Ctrl+C` to stop).
   - By this, you have connected with your Linux VM and tested the Internet connection.

### Installing Nginx on a Linux VM (e.g., Ubuntu):

Before Installing Nginx, Let's copy the Public IP and paste it into the Browser's new Tab and see.
As expected it will not Display any Web Page.

1. **Update Package Lists:**
   - It's a good practice to update the package lists to ensure you are installing the latest software. Run the following command:

   ```bash
   sudo apt update
   ```

2. **Install Nginx:**
   - Use the package manager to install Nginx. Run the following command:

   ```bash
   sudo apt install nginx
   ```

3. **Start Nginx:**
   - After the installation is complete, start Nginx with the following command:

   ```bash
   sudo systemctl start nginx
   ```

4. **Enable Nginx to Start on Boot:**
   - To ensure Nginx starts automatically when the VM reboots, use the following command:

   ```bash
   sudo systemctl enable nginx
   ```

5. **Check the Status of Nginx:**
   - Verify that Nginx is running without any issues. Run the following command:

   ```bash
   sudo systemctl status nginx
   ```

   This command will display the status and other information about the Nginx service.

6. **Open a Web Browser and Access the Default Web Page::**

   - Now, again open a web browser's New tab, and enter your Linux VM's public IP address.
   
   ##### `For example: if your VM's public IP address is "12.34.56.78," enter as http://12.34.56.78:`

   - You should see the default Nginx welcome page, indicating that Nginx is installed and running on your VM.

Now you've successfully installed Nginx on your Linux VM and accessed the default web page. You can further configure Nginx to host your own web content or web applications as needed.

---
## Lab-02: Step-by-step guide for creating a Windows virtual machine and deploying Nginx using Azure:

### Creating a Virtual Machine in Azure for Windows Server:

1. **Sign in to Azure:**
   - Sign in to the Azure portal (https://portal.azure.com) using your Azure account.

2. **Create a Resource:**
   - Click on "Create a resource" on the left-hand menu.

3. **Search for Windows Server:**
   - In the search bar, type "Windows Server." Select an appropriate Windows Server version (e.g., Windows Server 2022 Datacenter - x64 Gen 2) and click `Create`.

4. **Project Details**:

   - **Subscription**: Choose your Azure subscription.
   - **Resource Group**: Create a new `resource group`(e.g., `Demo-RSG-YourName`) or use an existing one.

5. **Virtual Machine Name**:
   - Enter a name for your VM (e.g., `Demo-WindowsVM-YourName`).

6. **Region**:
   - Leave it as Default (e.g., East US) (Or)
   - Choose a region near your location for better performance.

7. **Availability Options**:
   - Keep this as `No infrastructure redundancy required`.

8. **Image**:
   - Ensure that `Windows Server 2022 Datacenter - x64 Gen 2` is already selected (Or) Select it.

9. **Size**:
   - Choose a size `"B1s" (1 vCPU, 1 GB RAM)` that fits within the free tier limits.

     **Note:**
     - The above size is not enough to Use the VM for Installing Nginx.
     - To Install Nginx Choose `D2s_v3 (2 vCPU, 8 GiB RAM)`

10. **Authentication Type**: (Choose only if it is available or else leave it)
    - Select "Password."

11. **Username and Password**:
    - Enter a `username` and `password` for your Windows VM. Make sure it's strong and secure.

12. **Inbound Port Rules**:
    - In `Select inbound ports`, choose "RDP (3389)" and "HTTP (80)".

13. Click on `Next: Disks`.

14. **Disks**:
    - **OS Disk Size (GiB)**: Use the default size as 127 GiB.
    - **OS Disk Type**: Choose "Standard SSD" for better performance.

15. Click on `Next: Networking`.

16. **Networking**: Leave all settings as default.
    
    - Create a new virtual network and subnet if necessary.
    - Create a new public IP address or use an existing one.
    - Keep the network security group as "Basic."
    - Select "RDP (3389)" and "HTTP (80)" for public inbound ports.

18. Click on `Next: Management` > `Monitoring` > `Advanced` > `Tags` > `Review + Create`.

19. **Review + Create**:
    - Review the settings to ensure they align with your requirements.
    - Click `Create` to start the VM provisioning process.

20. **Deployment Process**:
    - Azure will start deploying your Windows VM. Monitor the progress in the Azure portal.

21. **Connect to Your Windows VM**:
    - Once the VM is deployed, choose the `Connect` option from the left-hand side.
    - Under Most Common > Native RDP click on `Select` and in `Option 3` click on `Download RDP File` to download the RDP file.
    - Use the RDP file to connect to your Windows VM using the provided username and password.
---
### (Optional Step) Installing Nginx on a Windows VM:

1. **Access Your Windows VM**:
   - After connecting to your Windows VM, you can start the installation process.

2. **Download Nginx for Windows**:
   - Open a web browser on your Windows VM and go to the Nginx download page (https://nginx.org/en/download.html).
   - Download the latest Windows version of Nginx.

3. **Install Nginx**:
   - Locate the downloaded Nginx installer and run it.
   - Follow the installation wizard's instructions, accepting the default settings, and completing the installation.

4. **Start Nginx**:
   - After installation, start the Nginx service by opening a command prompt with administrator privileges and running the following command:

   ```
   nginx.exe
   ```

5. **Check Nginx Status**:
   - To verify that Nginx is running without any issues, open a web browser on your Windows VM and enter "http://localhost" in the address bar.
   - You should see the default Nginx welcome page.

Now you've successfully installed Nginx on your Windows VM and accessed the default web page. You can further configure Nginx to host your own web content or web applications as needed.
