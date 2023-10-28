# Walkthrough―create an Azure account.

Creating an Azure account involves the following steps:

1. **Visit Azure Sign-up Page:** Go to [https://azure.com](https://azure.com) and click "Start free" or "Sign up."

2. **Sign In/Create Microsoft Account:** Sign in with your existing Microsoft account or create a new one.

3. **Fill Personal Info:** Provide your name, country, and birthdate.

4. **Verification:** Verify your identity using a code sent to your email or phone.

5. **Choose Account Type:** Select "Individual" or "Business."

6. **Provide Payment Info:** Add your credit card or bank account info for billing verification.

7. **Verify Identity:** Verify your identity again if prompted.

8. **Agree to Terms:** Read and accept the Azure terms of service.

9. **Set Up Account:** Create a unique Azure account name.

10. **Choose Region:** Select an Azure region for your services.

11. **Customize Experience (Optional):** Tailor your Azure experience.

12. **Review and Confirm:** Double-check your information.

13. **Start Using Azure:** Your account is created, and you can start using Azure services. Be aware of potential usage costs.

---
# Exercise―explore the Learn sandbox.

To explore the Learn sandbox, follow these steps:

1. **Visit the Azure Learn Sandbox Page:**
   Go to the Azure Learn Sandbox page, which can be found at [https://docs.microsoft.com/en-us/learn/certifications/devops-engineer](https://docs.microsoft.com/en-us/learn/certifications/devops-engineer).

2. **Sign In or Create a Microsoft Account:**
   You may be required to sign in with your Microsoft account. If you don't have one, you can create a new Microsoft account.

3. **Access the Sandbox:**
   Once you're signed in, you should see an option to access the Azure sandbox. Click on it.

4. **Start a Sandbox Session:**
   You will typically be given a time-limited session in the sandbox environment, often a few hours. During this time, you can explore Azure services, create and manage resources, and follow guided tutorials.

5. **Explore Azure Services:**
   Inside the Azure sandbox, you can access various Azure services, like virtual machines, databases, web apps, and more. You can create resources, configure settings, and learn by doing.

6. **Complete Learning Modules:**
   The Azure Learn platform often provides guided learning modules and tutorials. You can complete these modules to gain hands-on experience with Azure services. Follow the instructions step-by-step.

7. **Experiment and Learn:**
   Since this is a sandbox environment, you don't need to worry about costs or resource cleanup. Feel free to experiment, make mistakes, and learn from them. This is a safe place to gain practical experience.

8. **Monitor Your Time:** Keep track of the time you have in the sandbox. Once your session expires, you'll no longer have access to the sandbox environment.

9. **Save Your Progress:**
   Some learning modules might allow you to save your progress, which can be helpful for returning to your work in the future.

10. **Additional Resources:**
    The Azure Learn platform often provides additional resources such as documentation, videos, and quizzes to enhance your learning.
---

# Walkthrough―explore the Azure global infrastructure.

### What is Azure global infrastructure?
Azure global infrastructure is made up of two key components—physical infrastructure and connective network components. The physical component is comprised of 200+ physical datacenters, arranged into regions, and linked by one of the largest interconnected networks on the planet.

With the connectivity of the global Azure network, each of the Azure datacenters provides high availability, low latency, scalability, and the latest advancements in cloud infrastructure—all running on the Azure platform.

Together, these components keep data entirely within the trusted Microsoft network and IP traffic never enters the public internet.

### What is an Azure datacenter?
Azure datacenters are unique physical buildings—located all over the globe—that house a group of networked computer servers.

What is an Azure region?
An Azure region is a set of datacenters, deployed within a latency-defined perimeter and connected through a dedicated regional low-latency network.

With more global regions than any other cloud provider, Azure gives customers the flexibility to deploy applications where they need. An Azure region has discrete pricing and service availability.

### What is an Azure geography?
An Azure geography is a discrete market, typically containing at least one or more regions, that preserves data residency and compliance boundaries. Geographies allow customers with specific data-residency and compliance needs to keep their data and applications close. Geographies are fault-tolerant to withstand complete region failure through their connection to the dedicated high-capacity networking infrastructure of Azure.

### What are Azure Availability Zones?
Azure Availability Zones are unique physical locations within an Azure region and offer high availability to protect your applications and data from datacenter failures. Each zone is made up of one or more datacenters equipped with independent power, cooling, and networking.

The physical separation of availability zones within a region protects apps and data from facility-level issues. Zone-redundant services replicate your apps and data across Azure Availability Zones to protect from single points of failure.

### What is the Azure global network?
The Azure global network refers to all of the components in networking and is comprised of the Microsoft global wide-area network (WAN), points of presence (PoPs), fiber, and others.

### What are Azure Edge Zones?
Azure Edge Zones are footprint extensions of Azure, placed in densely populated areas. Azure Edge Zones support virtual machines (VMs), containers, and a select set of Azure services that let you run latency-sensitive and throughput-intensive apps close to your end users.

Azure Edge Zones are part of the Microsoft global network and offer secure, reliable, and high-bandwidth connectivity between apps—running at the Azure Edge Zone (close to the user), and the full set of Azure services running across the larger Azure regions.

### What is Azure Space?
Azure Space is a strategic initiative that extends the utility of Azure capabilities through the power of space infrastructure. It was created to be the platform and ecosystem of choice for the mission needs of the space community. Azure Space makes connectivity and compute increasingly attainable across industries, including agriculture, energy, telecommunications, and government.

### What is Azure Orbital?
Azure Orbital is part of Azure Space strategic initiative. It provides a fully managed ground station service that enables customers to communicate, downlink, and process data from their satellites or spacecrafts on a pay-as-you-go basis—without needing to build their own satellite ground stations.

What’s the Microsoft global wide-area network (WAN)?
The Microsoft global wide-area network (WAN) connects hundreds of datacenters in regions around the world and offers high availability and capacity. With the flexibility to immediately respond to unpredictable demand spikes, the global WAN is critical in delivering a great cloud service experience.

### What’s an Azure point of presence?
An Azure point of presence, often abbreviated as PoP, is an access point or physical location where traffic can enter or exit the Microsoft global network.

### What are Azure regional network gateways?
Regional network gateways are massively parallel, hyperscale datacenter interconnects between datacenters within a region—without the need to network each individual datacenter to the others in a region.

This ensures that connection issues in one datacenter don’t cause issues for the wider region. This also allows the addition of new datacenters without the need to route direct network connections to each existing datacenter.

---

# Exercise―create an Azure resource

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

**7. Monitor the Resource Group:**
   - After the VM provisioning is complete, go to the Azure Portal dashboard.
   - Click on "Resource groups" in the left-hand menu.

**8. Select the Resource Group:**
   - Choose the resource group where you created your VM.

**9. View Resources:**
   - In the resource group overview, you will see a list of resources. Your new virtual machine should be listed here.

**10. Azure Monitor for VM Insights:**
   - To monitor the VM's performance and health, you can click on the VM's name in the resource group. Under "Monitoring," you'll find "Azure Monitor for VM Insights." This provides insights into your VM.

**11. Set Up Alerts:**
    - In the VM's monitoring section, you can configure alerts based on performance metrics. This way, you'll be notified if something goes wrong with your VM.

By following these steps, you can create a virtual machine and monitor the resource group to ensure the VM is successfully created and is performing as expected. Azure Monitor provides the tools to keep an eye on your VM's health and set up alerts to proactively address any issues that may arise.

---

## Lab-02: Exercise―create a virtual machine and Install the web server package.

Create a virtual machine in the Azure portal, connect to the virtual machine, install the web server role and test. 

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
   - Specify a name for your VM, e.g., `Demo-WindowsVM-YourName`.

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

To install a web server package on an already created Windows Virtual Machine (VM), you can use Internet Information Services (IIS), which is a popular web server for Windows. Here are the steps to install IIS on a Windows VM:

8. **Open Server Manager**:
   - Press the "Windows" key on your keyboard, type "Server Manager," and open the Server Manager application.

9. **Add Roles and Features**:
   - In the Server Manager window, click on "Manage" in the top-right corner, and then select "Add Roles and Features."

10. **Role-Based or Feature-Based Installation**:
   - In the "Before you begin" window, click "Next."
   - Choose "Role-based or feature-based installation" and click "Next."

11. **Select the Server**:
   - Select "Select a server from the server pool," and make sure your local server (the VM you are on) is selected. Click "Next."

12. **Select Features**:
   - In the "Select features" window, scroll down and find "Web Server (IIS)." Check the box next to it. You may see additional features that can be installed with IIS; you can leave them as their default selections. Click "Next."

13. **Role Services**:
   - In the "Select role services" window, the required services for a basic web server are automatically selected. Review them and click "Next."

14. **Confirmation**:
   - Review your selections, and then click "Install."

15. **Install IIS**:
    - The installation process will begin, and it may take a few minutes to complete.

16. **Completion**:
    - Once the installation is finished, you will see a "Results" screen. It should show "Installation succeeded." Click "Close" to exit the wizard.

17. **Verify IIS Installation**:
    - To verify that IIS is installed and running, open a web browser within the VM and enter "http://localhost" in the address bar. If you see the default IIS start page, IIS is up and running.

IIS is now installed and configured on your Windows VM. You can start deploying your web applications or websites on this server. Make sure to configure any additional settings, such as firewall rules or security, based on your specific requirements and needs.

---
## Lab3:  Walkthrough―configure network access:

It involves creating and configuring a Network Security Group (NSG) to control inbound and outbound traffic to and from resources within a Virtual Network (VNet). In this example, we'll configure HTTP access (port 80) to a virtual machine.

**1. Verify Currently Open Ports:**

Before making changes, you should verify the current network configuration. To check which ports are open on your VM, you can use the following steps:

- Connect to your Azure VM using Remote Desktop (RDP).
- On the VM, you can use the Command Prompt or PowerShell to run a command like `netstat -an` or `Test-NetConnection -ComputerName localhost -Port 80` to check if port 80 is already open.

**2. Create a Network Security Group:**

In this step, we'll create a Network Security Group and associate it with your virtual machine:

- In the Azure Portal, go to the "Home" or "All services" and search for "Network security groups."
- Click "Add" to create a new NSG. Provide a name and specify the resource group and region.
- Click "Review + create" and then "Create" to create the NSG.

**3. Configure HTTP Access (Port 80):**

Now, you'll configure the NSG to allow incoming traffic on port 80 (HTTP):

- Go to the newly created NSG, and in the left-hand menu, click on "Inbound security rules."
- Click "Add" to create a new rule.
- Provide a name for the rule, set the "Priority" (lower numbers have higher priority), and specify the "Source" (where the traffic is coming from, e.g., Any or a specific IP range).
- Set the "Service" to "HTTP (80)," or you can manually specify port 80.
- Choose "Allow" as the "Action."
- You can leave "Priority" as the default value or adjust it based on your requirements.
- Click "Add" to create the rule.

**4. Test the Connection:**

To test if the configuration is working as expected:

- Make sure your VM is running and your web server is set up and listening on port 80.
- Open a web browser or use a tool like cURL to access your VM's public IP address or DNS name over HTTP (e.g., `http://<your-vm-public-ip>`).
- You should be able to access your web server over HTTP. If you can, the NSG rule is configured correctly.

Make sure to monitor your NSG for any unexpected changes or access issues and adjust the NSG rules as needed based on your security requirements. Additionally, for production environments, consider using more specific source IPs and HTTPS (port 443) for added security.

---
## Lab 04: Detailed Steps for Creating an Azure Blob Storage:

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
## LAb 05: Exercise―use the Azure pricing calculator

Using the Azure Pricing Calculator is a great way to estimate the cost of Azure services and resources before you deploy them. Here's a simple exercise to get you started:

**1. Access the Azure Pricing Calculator:**

Visit the [Azure Pricing Calculator](https://azure.com/calculator) using a web browser.

**2. Configure the Pricing Calculator:**

Follow these steps to configure the pricing calculator:

- Click on "Get started" or "Pricing calculator" to begin.
- In the "Estimate your costs for Azure" section, you will see a set of options:
  - **Products**: Click on "Add products" to choose the Azure services you want to include in your estimate. You can search for services by name or browse categories.
  - **Region**: Select the Azure region where you plan to deploy your resources.
  - **Term**: Choose the term of your estimate, such as Pay-as-you-go or a specific contract.
  - **Currency**: Select your preferred currency for pricing.
  - **Additional filters**: Optionally, you can apply filters like "Service Type" or "Resource Tags" to refine your selection.
- As you make your selections, the pricing calculator will update in real-time to show the estimated cost.

**3. Add Azure Products:**

Let's add an example product for estimation:

- Click "Add products" and search for "Virtual Machines."
- Select a VM type (e.g., Windows or Linux) and specify the VM configuration (e.g., size, number of instances, and storage type).
- Click "Add" to add the VM to your estimate.

**4. Review the Pricing Estimate:**

Once you've added the products you want to estimate, the pricing calculator will provide you with a detailed breakdown of the estimated costs. You can review this information, which includes:

- Total monthly cost.
- Cost breakdown by service, region, and term.
- Details of the selected Azure services and their configurations.

**5. Save or Export the Estimate:**

You can save or export your estimate for future reference or sharing. Click on the "Save" or "Export" buttons to do this.

**6. Modify the Estimate:**

You can go back and make changes to your estimate at any time by adjusting the products, region, terms, or other settings. The estimate will automatically update.

**7. Share the Estimate:**

If you need to collaborate with others or get approvals, you can share the estimate by using the "Share" feature. This allows you to generate a URL that others can use to view your estimate.

This exercise helps you become familiar with the Azure Pricing Calculator, allowing you to estimate the costs associated with your Azure deployments and make informed decisions about your cloud spending.

---
## Lab 06: Exercise―use the Azure TCO calculator

The Azure Total Cost of Ownership (TCO) Calculator is a tool that allows you to estimate the costs associated with running your workloads on Azure compared to an on-premises environment. Here's a step-by-step exercise to use the Azure TCO Calculator:

**1. Access the Azure TCO Calculator:**

Go to the [Azure TCO Calculator](https://azure.microsoft.com/en-us/tco/calculator/) using a web browser.

**2. Configure the TCO Calculator:**

Follow these steps to configure the TCO Calculator:

- Click on "Get started" or "TCO calculator" to begin.
- In the "Estimate your TCO with Azure" section, you'll see various options:
  - **Name your estimate**: Give your estimate a name for reference.
  - **Location**: Choose your country or region to account for local costs.
  - **Organization type**: Specify whether you're an Enterprise or a Managed Service Provider (MSP).
  - **Use case**: Select the use case that best fits your scenario, such as "Migrate & Modernize" or "New Workload."

**3. Input Assumptions:**

You will be asked to provide detailed information about your current on-premises environment. Here's a simplified example:

- **On-Premises Costs**: Enter information about your current data center costs, including capital expenditure (CapEx) and operational expenditure (OpEx) items.
- **Server Workloads**: Define the number and types of servers you currently have (e.g., physical, virtual, or containerized).
- **Storage**: Enter the details of your on-premises storage environment.
- **Network**: Describe your network infrastructure and bandwidth costs.

**4. Configure Azure Options:**

Next, you'll provide information about the Azure options you want to compare. This includes:

- **Virtual Machines**: Specify the number of VMs you plan to deploy and their configurations.
- **Storage**: Define the Azure storage solutions you intend to use.
- **Network**: Provide details on Azure network costs and bandwidth.

**5. Review the Results:**

After inputting all your assumptions, the TCO Calculator will generate a comprehensive report showing a detailed breakdown of costs for your on-premises environment and the equivalent costs in Azure. It will provide insights into your potential cost savings and a comparison of the two scenarios.

**6. Save a Copy:**

To save a copy of your TCO estimate:

- Click on the "Save" button.
- You will be prompted to sign in with your Microsoft account or create one if you don't have an account.
- After signing in, you can save your estimate for future reference.

The TCO Calculator allows you to analyze the cost implications of migrating to Azure, making informed decisions about your cloud strategy and cost savings.

---
## Lab 07: Walkthrough―manage resource locks

Resource locks in Azure are used to prevent accidental deletion or modification of resources. There are two types of resource locks: "ReadOnly" and "Delete." In this walkthrough, we'll add a "ReadOnly" resource lock to a resource, update the lock, remove it, and then delete the resource.

**1. Create a Resource:**

First, you need to create a resource in Azure. For the purpose of this walkthrough, let's create a simple Azure Storage account. You can follow these steps:

- Sign in to the Azure Portal.
- Click on "+ Create a resource."
- Search for "Storage account," select it, and fill in the required details to create the storage account. Click "Review + create" and then "Create."

**2. Add a ReadOnly Resource Lock:**

Now, let's add a "ReadOnly" resource lock to the storage account:

- Go to the Azure Portal.
- Navigate to your newly created storage account.
- In the left-hand menu, under "Settings," find and select "Locks."
- Click the "+ Add" button to add a new lock.
- Provide a name for the lock, such as "ReadOnlyLock."
- Select "ReadOnly" as the lock type.
- Optionally, provide a description.
- Click "OK" to create the lock.

**3. Update the Lock and Retest:**

Now, let's update the existing lock to make a modification and then test it:

- In the "Locks" section of the storage account, find the "ReadOnlyLock" that you just created.
- Click on the "ReadOnlyLock" to view its details.
- In the "Lock details" pane, click "Edit" to make changes to the lock. For example, you can update the description.
- Click "Save" to update the lock.

To test the ReadOnly lock, try to make a change to the storage account. You'll see that Azure prevents any modifications while the lock is in place.

**4. Remove the Resource Lock:**

To remove the "ReadOnly" resource lock:

- In the "Locks" section of the storage account, find the "ReadOnlyLock."
- Click on the "ReadOnlyLock" to view its details.
- In the "Lock details" pane, click "Delete."
- Confirm the removal by clicking "Yes" in the confirmation dialog.

**5. Delete the Resource:**

To delete the resource, in this case, the storage account:

- Go to the storage account's main page.
- In the left-hand menu, under "Settings," click on "Overview."
- Click the "Delete" button, and follow the prompts to confirm the deletion. Note that you can't delete a resource if there is a "Delete" resource lock in place.

This walkthrough demonstrates how to create, update, and remove a "ReadOnly" resource lock to prevent modifications to a resource, and how to delete the resource once the lock is removed. Resource locks provide an additional layer of protection for your critical Azure resources.

---
