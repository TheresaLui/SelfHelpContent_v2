<properties
	  pageTitle="Ensure All ports for FTP service are enabled. "
	  description="Ensure All ports for FTP service are enabled. "
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
	  articleId="b192a65d-ae9f-4ad4-816e-8ed34cac5399"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Ensure All ports for FTP service are enabled. 

FTP servers communicate using active and passive modes. Although it is not always made clear there are a range of ports in use that will all need to be available in order for traffic to be transferred successfully. 


#Recommended Steps

1. Review customer FTP application setup.

2. If any ranges are given for "Passive Mode" ensure the full range of ports are allowed through any NSGs or firewalls provisioned within the path. 

3.  If customer is still unable to reach gather a packet capture to confirm what ports are being reached out to prior to the disconnect to ensure the correct range has been enabled. 

