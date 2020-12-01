<properties
	  pageTitle="Verify if port 25 is actually blocked"
	  description="Verify if port 25 is actually blocked"
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
	  articleId="2e711524-4d89-4569-9085-c056cffc90cb"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Verify if port 25 is actually blocked

Starting on November 15th, 2017, sending outbound email directly to external domains (such as outlook.com , gmail.com ) from a Virtual machine (VM) will be made available only to certain subscription types. Outbound SMTP connections using TCP port 25 (primarily used for unauthenticated e-mail delivery) will be blocked for most new subscriptions


#Recommended Steps

1. Find the VM resource/s in 'Resource Explorer' in ASC (make sure to include VMs in the outbound path. eg. NVAs)

2.  On the 'Diagnostic' tab choose 'Test Traffic'

3. Leave all the defaults but update the 'Destination IP' to 8.8.8.8 and the 'Destination Port' to 25 then click 'Run'

4. Review results to see if customer is blocked.

5. If the results show as "Fraudulent" close the SR and do not contact the customer. 


#Reccommended Documents

1.(SMTP Blocked)[https://supportability.visualstudio.com/AzureNetworking/_wiki/wikis/Wiki/137605/Email-from-VM-Port-25-blocked]

