# Microsoft Azure Cert notes



Monday, November 18, 2019
1:05 PM

	• Understand terms such as 
		○ High Availability: 24*7*365 service availability, minimal downtimes 
		○  Scalability: Pay as you need services based on usage
		○  Elasticity: Scaled based on usage follows horizontal scaling 
		○  Agility: Produce a devops environment to help increase speed to market
		○  Fault Tolerance: 
		○ Disaster Recovery: Allows to store data in multiple geographic locations same or different regions
		
	• Understand the principles of economies of scale: lower cost per unit for operating ar a larger scale. CP save on hardware and CP can leverage local government and utilities for tax breaks which are "returned to the customer" 
	
	• Expenditure
		○ Capital Expenditure (CapEx) : Price of Physical infrastructure, you'll have to pay up front for the hardware, labor, config
		○ Operational Expenditure (OpEx): Price for billed services and resources, no upfront cost and pay as you go model.
		
	• Understand the consumption-based model
	
	• Infrastructure-as-a-Service (IaaS): Most flexible complete control. Self config Infrastructure of servers and VM's. Migrating workloads easier. Test and deploy ease increases speed to market. Managed Ratio User: 75% Provider: 25%
	
	• Platform-as-a-Service (PaaS) builds app environment (w/o server and VM infrastructure configurations) complete development framework Managed Ratio User: 50% Provider: 50%
	
	• Software-as-a-Service (SaaS):  centrally hosted and managed for end user i.e. Office 365 Managed Ratio User: 25% Provider: 75%
	
	• compare and contrast the three different service types
	
	
	• Public cloud (OpEx): Cloud Provider  provides and runs hardware. Scalable, cost efficient, no hardware responsibility. Difficulty making specific security needs, may not meet certain policies, gov't requirements, legal. 
	• Private cloud (CapEx): Ensure configuration, can handle any scenario. Has CapEx, used for extra data security for sensitive data. On prem servers. 
	• Hybrid cloud: The combination of the 2 and set the cloud to your needs, can run website on cloud and run a sensitive DB in private cloud to match legal requirements for data security,. 
	• compare and contrast the three different cloud models
Comparisons: compute and setup cloud environments with all the power of the cloud capabilities. Creating a private cloud to protect sensitive data, create a public cloud for general purpose use. Hybrid cloud to help with reducing cost of private cloud costs. Choice based on what your development model requires.

	• describe Regions: Data location, keeps in mind sovereignty, local compliance and requirements per country. 
	• describe Availability Zones: creates a fault tolerant, data redundant services in the case of a data center failure, data is made on fault and updated domains to make sure that data is not lost
	• describe Resource Groups: a group of resources. Can be tagged for billing, group use, etc. if the resource group is deleted all children resources will also be deleted. R.G. can have policies and permissions set to them. Permissions full the general hierarchy rules, a child cannot pass policies to its parent. 
	• describe Azure Resource manager: Logical container for resources deployed in Azure.  All resources must belong to a Resource Group
	• describe the benefits and usage of core Azure architectural components
		○ Organize Resource groups to help delegate permissions on a resource group, R.G. can be grouped many different ways by using tags. Groupings may be by:
			§  resource type (i.e. all DBs, all Security, etc.)
			§ Environment (i.e. Dev with DB, policy, etc. )
Department (i.e. Billing, developer, devOps, etc.)

describe products available for Compute such as:
Virtual Machines (IaaS): Emulations of a physical computer, built on a OS kernel that runs. Total control over OS. Eases Migration to cloud by using images. Can run multiple VMs for availability.
Virtual Machine Scale Sets: Creates local groupings of VMs to help keep app up during militance, patches etc. Some VMs require a rest period. 
	Fabric controller handles the VMs by passing commands to help keep VMs updating in a sequence vs shutting down all VMs for an update. 
	Azure Batch: for large scale jobs scheduler and computer management. Starts and runs applications in pools. 
App Service Functions (PaaS): Serverless computing. For hosting applications (Web, API, webJobs, mobile). Abstracts services worry about code not infrastructure. Functions execute events. EVENT DRIVEN. Creates a micro billing service that makes pay as you go easier, pay per trigger instead up VM's or containers that are always running 
Logic Apps: Stateful, design first, large collection of prebuilt functions CLOUD ONLY
	Creates and executes logic blocks that are triggered by an event. 
	Persisted by JSON
Function Apps: Stateless, code first, bind types, code function for EVENT, managed by REST API, executable in CLOUD or LOCAL 
Azure Container Instances (ACI): Simple container, NO VM or additional service configurations,.
Azure Kubernetes Service (AKS): Gives user complete orchestration over kubes, also distributed architecture for many containers. 

describe products available for Networking such as:
Virtual Network: VNet, private Azure network with numerous resources such as VMs. Built for scalability and security. 
Load Balancer: traffic distribution tool to create resiliency and viability. LB receives a  request, sends to a VM, if VM is down cancel all loads from going to down VM. Prevents interruptions. No infrastructures can be set by Network tier. 
VPN: Virtual Private network. 
Gateway: all traffic is HTTP, uses TCP  routing. Can understand HTTP message structure. 
Application Gateway 
Content Delivery Network

describe products available for Storage such as
Blob Storage: Unstructured data, highly scalable (think NETFLIX)
Disk Storage:  Data persisted on a virtual disk. Can select disk type SSD or HDD
File Storage: file management system that uses Server Message Block
Archive Storage

describe products available for Databases such as 
Cosmos DB: NoSQL  DB that is globally distributed DB service. 
Azure SQL Database: MS SQL server, can use Azures DB Migration service to move data. Can generate assessment reports
Azure Database for MySQL: tool leverage of MySQL
Azure Database for PostgreSQL:
Azure Database: 
Migration service: Used by Azure SQL Database to help migrate data from other RMSDB. 

describe the Azure Marketplace and its usage scenarios: 
Solutions area power by Microsoft azure. Helps provision E2E solutions. 

describe Internet of Things (IoT) and products that are available for IoT on Azure such as
IoT Hub
 and IoT Central
describe Big Data and Analytics and products that are available for Big Data and
Analytics such as SQL Data Warehouse, HDInsight and Azure Databricks
describe Artificial Intelligence (AI) and products that are available for AI such as Azure
Machine Learning Service and Studio
describe Serverless computing and Azure products that are available for serverless
computing such as Azure Functions, Logic Apps and Event Grid
describe DevOps solutions available on Azure, such as Azure DevOps and Azure DevTest
Labs
describe the benefits and outcomes of using Azure solutions
