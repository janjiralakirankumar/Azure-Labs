## Detailed and step-by-step guide for creating a virtual machine in Azure, both for Linux and Windows, along with instructions for installing Nginx on a Linux VM:

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
   - Enter a name for your VM (e.g., `Demo-VM-YourName`).

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

#### Leave all settings as Default for below.
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
    - After deployment, go to `All Resources` > Click on the VM and choose `Connect`.
    - Choose `Native SSH` and Click on `Select` under Most Common.
    - In `Option 3` click on the Copy Icon and then open PowerShell, change the path where the Private key is available (e.g., Downloads), and paste it.
    - Example:
   ```bash
   ssh -i ~/.ssh/id_rsa.pem azureuser@172.190.132.28
   ```
   - Replace your Key Pair Name (e.g., `Demo-VM-YourName_key.pem`) with `~/.ssh/id_rsa.pem` and press Enter.
   - Now, you are connected to your VM, and to check the Internet connection, enter the command `ping google.com` and press Enter (`Ctrl+C` to stop).
   - By this, you have connected with your Linux VM and tested the Internet connection.

### Installing Nginx on a Linux VM (e.g., Ubuntu):

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

6. **Open a Web Browser:**
   - On your local computer, open a web browser (e.g., Chrome, Firefox, or Edge).

7. **Access the Default Web Page:**
   - In the web browser's address bar, enter your Linux VM's public IP address. For example, if your VM's public IP address is "12.34.56.78," enter:

   ```
   http://12.34.56.78
   ```

   You should see the default Nginx welcome page, indicating that Nginx is installed and running on your VM.

Now you've successfully installed Nginx on your Linux VM and accessed the default web page. You can further configure Nginx to host your own web content or web applications as needed.

Please let me know if you need any additional details or have any questions.
