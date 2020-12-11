<properties
	  pageTitle="Have Port unblocked for customer"
	  description="Have Port unblocked for customer"
      service="Microsoft.network"
      resource="Microsoft.network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="efd8be3a-4a2f-47f7-971b-37f517aea096"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Have Port unblocked for customer

Starting on November 15th, 2017, sending outbound email directly to external domains (such as outlook.com , gmail.com ) from a Virtual machine (VM) will be made available only to certain subscription types. Outbound SMTP connections using TCP port 25 (primarily used for unauthenticated e-mail delivery) will be blocked for most new subscriptions


#Recommended Steps

1. Update the area path?in Service Desk to?Virtual Network > Connectivity > Cannot send email (SMTP/Port 25)

2. **In the ASC Overview page, select the option to "Edit and Run Again" ensuring that the support topic in step 1 above is selected.

3. If the resulting Critical Insight shows "Customer Already Enabled" OR "Has now been enabled" have the customers 'STOP Deallocate' from the Azure portal and 'START' all the VMs and check again.

4. If the resulting Critical Insight shows "Qualified to be enabled" OR "Manual Approval Needed" transfer the SR to Azure Subscription Team. The SR will auto route to their team when the support topic is set per step?#1?above

5. If the resulting Critical Insight shows "Fraudulent". Close the SR and do not contact the customer.



#Reccommended Documents

1.(SMTP Blocked)[https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/137605/Email-from-VM-Port-25-blocked]

