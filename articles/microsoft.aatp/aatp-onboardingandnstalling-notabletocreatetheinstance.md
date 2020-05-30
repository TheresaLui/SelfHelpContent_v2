<properties
	pageTitle="Not able to create the Instance"
	description="Not able to create the Instance"
	infoBubbleText="Not able to create the Instance"
	service="microsoft-aatp"
	resource="aatp"
	authors="digeler"
	ms.author="digeler"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32729038"   
	resourceTags=""
	productPesIds="16264"
	cloudEnvironments="Public,fairfax, usnat, ussec"
	articleId="1eb2d47d-0f21-4451-f8c9-b140beac15d4"
	ownershipId="Azure_Advanced_Threat_Protection"
/>
# Directions

## **Recommended Steps**

### **Common Issues**

Security Group with the same name already exists in Azure Active Directory:
	
* It looks like your tenant had an AATP instance in the past and it was deleted. However, when the instance was deleted, the AAD groups used by AATP for RBAC were not deleted. If you go to AAD you should see three groups: 
	
	* Azure ATP (instance name) Administrators
	* Azure ATP (instance name) Viewers
	* Azure ATP (instance name) Users

 To fix the above, you will need to delete the security group, and retry the operation.

* [Types of Azure ATP security groups](https://docs.microsoft.com/azure-advanced-threat-protection/atp-role-groups#types-of-azure-atp-security-groups) 

## **Recommended Documents**

* [Create your Azure ATP instance](https://docs.microsoft.com/azure-advanced-threat-protection/install-atp-step1)
* [Check out the Azure ATP forum!](https://techcommunity.microsoft.com/t5/azure-advanced-threat-protection/bd-p/AzureAdvancedThreatProtection)
