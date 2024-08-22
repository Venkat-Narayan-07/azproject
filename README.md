# Azure Website Deployment with High Availability
**Project Overview**
This repository showcases my ability to design and implement a highly available website architecture for a corporation using Azure services. The architecture utilizes Traffic Manager, Application Gateway, Azure VMs, Azure Blob Storage, and Azure Container Instances for optimal traffic distribution, page serving, and error handling.

**Project Goals**
* Deploy a website with three web pages: home page, upload page, and error page.
* Implement high availability by distributing traffic across two regions (Central US and West US).
* Utilize Application Gateway for routing requests to specific pages based on URL paths.
* Configure error handling for 403 and 502 errors with a custom error page hosted on Azure Blob Storage.
* Ensure secure communication within the virtual networks through VNet Peering.

**Technical Implementation**
* Traffic Manager: Routes incoming traffic to the Application Gateway in the optimal region based on defined policies.
* Application Gateway: Acts as a reverse proxy, directing requests to the appropriate web page based on URL paths.
* Azure VMs:
  - Two VMs deployed, one in each region (Central US and West US).
  - Each VM resides within a dedicated Virtual Network (VNet).
  - VMs host the application code (cloned from GitHub) and execute deployment scripts.
* Azure Blob Storage:
  - Stores the custom error page (error.html).
  - Configured as a static website to serve the error page for 403 and 502 errors.
  - Azure Container Instances: (Optional) Can be used to host the upload page in a containerized environment (not implemented in this initial version).
* VNet Peering: Enables secure communication between the VMs in different regions.

**Key Technologies Used**
* Azure Traffic Manager
* Azure Application Gateway
* Azure Virtual Machines
* Azure Virtual Network
* Azure Blob Storage

**Skills Demonstrated**
* Azure Resource Management
* High Availability Architecture Design
* Traffic Management Configuration
* Application Gateway Routing
* Azure VM Deployment and Management
* Azure Blob Storage Configuration
* VNet Peering

**Project Outcome**
A highly available website architecture ensures minimal downtime and optimal performance.
Traffic distribution between regions improves scalability and responsiveness.
Customized error handling provides a more user-friendly experience.
Further Resources
# - 
**Documentation**: A detailed PDF document "Azure Administrator Capstone Project AZ" outlines the complete deployment process with screenshots. 
# -
By showcasing this project, I aim to demonstrate my proficiency in designing and implementing robust Azure solutions for high availability and efficient website deployments.
