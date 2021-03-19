<properties
	  pageTitle="Check firewall on destination VM."
	  description="Check firewall on destination VM."
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
	  articleId="81e21dce-03e1-4b68-a8ce-a3a8dc90b60d"
	  ownershipId="Centennial_Cloudnet_VirtualNetwork"
/>

# Check firewall on destination VM.

Check if the Windows Firewall/ Linux iptables is allowing traffic on the specified port on the destination VM. 

## Recommended Steps

For Windows:
1. Open ASC for the Destination VM2
2. Go to the Diagnostics tab and run Inspect IaaS Disk with WinGuest Analyzer
3. Download and extract the zip file generated from WinGuest Analyzer
4. Navigate to the report.html file and open it with a browser of your choice
5. Open the Network tab and check if there is a rule allowing the destination port under Firewall Raw


For Linux:

1. Open ASC for the Destination VM2
2. Go to the Diagnostics tab and run Inspect IaaS Disk
3. Download and open the zip file generated
4. Open the \device_0\etc\sysconfig\iptables file. If iptables is not configured there will be no such file and you can skip to the next step assuming iptables it not blocking traffic.
5. Check what is the default behavior for inbound traffic: this is denoted as INPUT and the value next to it can either be DROP which means traffic is blocked, or ACCEPT which means traffic is accepted.
6. If the default rule is blocking traffic, check if there is a specific rule for the port they are trying to connect to that has the value ACCEPT associated with it
7. If the default rule is allowing traffic, check if there is a specific rule for the port they are trying to connect to that has the value DROP assocaited with it

