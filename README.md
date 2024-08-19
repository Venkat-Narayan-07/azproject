# Capstone Project AZ
You work as an Azure professional for a Corporation. You are assigned the task of implementing the below architecture for the company’s website.

![image](https://github.com/user-attachments/assets/83cdccd4-f124-479b-be12-8449b8794fd2)

There are three web pages to be deployed:
1. The home page is the default page (VM2)
2. The upload page is where you can upload the files to your Azure Blob Storage (VM1)
3. The error page for 403 and 502 errors Application Gateway has to be configured in the following manner:
1.
Example.com should be pointed to the home page
2.
Example.com/upload should be pointed to the upload page
3.
Application Gateway’s error pages should be pointed to error.html which should be hosted as a static website in Azure Containers. The error.html file is present in the GitHub repository
The term ‘Example’ here refers to the Traffic Manager’s domain name. The client wants you to deploy them in the Central US and the West US regions such that the traffic is distributed optimally between both regions. Storage Account has to be configured in the following manner:
1. You need to host your error.html as a static website here, and then point the application gateway’s 403 and 502 errors to it.
2. Create a container named upload, this will be used by your code to upload the files. Technical specifications for the deployments are as follows:
1. Deployments in both regions should have VMs inside VNets.
2. Clone the GitHub repo https://github.com/azcloudberg/azproject to all the VMs.
3. On VM1, please run vm1.sh this will deploy the upload page, on VM2 please run VM2.sh, this will install the home page.
4. For running the scripts, please run the following command inside the GitHub directory from the terminal.
VM1: ./vm1.sh
VM2: ./vm2.sh
5. After running the scripts, please edit the config.py file on VM1, and enter the details related to your storage account where the files will be uploaded.
6. Once done, please run the following command: sudo python3 app.py
7. Both regions should be connected to each other using VNet-VNet Peering.
8. Finally, your Traffic Manager should be pointing to the application gateway

# the whole deployment is documented along with screenshots in a pdf file named "Azure Administrator Capstone Project AZ."
