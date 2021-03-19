<properties
 pageTitle="Check if an NSG is blocking the customer source IP"
 description="Check if an NSG is blocking the customer source IP"
 service="Microsoft.Network"
 resource="Microsoft.Network/loadBalancers"
 authors="Centennial_CloudNet_LoadBalancer"
 ms.author="Centennial_CloudNet_LoadBalancer"
 displayOrder=""
 selfHelpType="TSG_Content"
 supportTopicIds=""
 resourceTags=""
 productPesIds=""
 cloudEnvironments="public, fairfax, usnat, ussec"
 articleId="a2c5e29b-f326-403a-b2c4-d9bb8c37d612"
 ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Check if an NSG is blocking the customer source IP

## Recommended Steps

To validate if a NSG is blocking inbound traffic, use ASC and click on the backend pool member NIC and from there, click on the attached VM link. Click on the Diagnostics tab and then scroll down to Test Traffic. Modify the following parameters:

* **Traffic Direction:** for external load balancers, select InternetIn. For internal load balancers, select TunnelOrLocalIn.
* **Source IP:** Source IP customer is attempting to connect from
* **Destination Port:** The load balanced port
* **Transport Protocol:** The load balanced protocol. This should be TCP or UDP only. Load balancers do not support ICMP and other protocols.

Click Run. Under result, click "Stateful Test (NSG Layer)" and ensure the test result is: Traffic: ALLOWED. If not, advise customer to alter their NSG and create a rule with a higher priority (lower number) to allow the traffic.
