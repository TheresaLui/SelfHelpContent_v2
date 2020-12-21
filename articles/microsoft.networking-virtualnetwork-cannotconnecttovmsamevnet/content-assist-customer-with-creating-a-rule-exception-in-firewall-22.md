<properties
	  pageTitle="Assist customer with creating a rule/exception in firewall"
	  description="Assist customer with creating a rule/exception in firewall"
      service="Microsoft.Network"
      resource="Microsoft.Network/virtualNetworks"
	  authors="anferrei"
	  ms.author="anferrei"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="d58decf9-bd41-41fe-943f-9a4e818103d5"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Assist customer with creating a rule/exception in firewall

Assist the customer with adding a rule allowing inbound traffic on the required port.

## Recommended Steps

For Windows:
Ask the customer to RDP to the VM and do the following:
1. Open an elevated command prompt
2. Run the following command:
netsh advfirewall firewall add rule name= "<Rule Name>" dir=in action=allow protocol=TCP localport=<port number>


For Linux:
Ask the customer to SSH to the VM and run the following command:
sudo iptables -A INPUT -p tcp --dport <port number> -j ACCEPT

