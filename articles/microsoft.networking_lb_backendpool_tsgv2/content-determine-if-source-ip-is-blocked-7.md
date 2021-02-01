<properties
	  pageTitle="Determine if source IP is blocked"
	  description="Determine if source IP is blocked"
    service="Microsoft.Network"
     resource="Microsoft.Network/loadBalancers"
	  authors="dgoddard"
	  ms.author="dgoddard"
	  displayOrder=""
	  selfHelpType="TSG_Content"
	  supportTopicIds=""
	  resourceTags=""
	  productPesIds=""
	  cloudEnvironments="public, fairfax, usnat, ussec"
	  articleId="cd505a95-0e25-4b11-b38b-ae01c7fb8b6a"
	  ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Determine if source IP is blocked

## Recommended Steps

To validate if a NSG is blocking inbound traffic, use ASC and click on the backend pool member NIC and from there, click on the attached VM link. Click on the Diagnostics tab and then scroll down to Test Traffic. Modify the following parameters:
**Traffic Direction:** for external load balancers, select InternetIn. For internal load balancers, select TunnelOrLocalIn. 
**Source IP:** Source IP customer is attempting to connect from
**Destination Port:** The load balanced port
**Transport Protocol:** The load balanced protocol. This should be TCP or UDP only.

Click Run. Under result, click "Stateful Test (NSG Layer)" and ensure the test result is: Traffic: ALLOWED. If not, advise customer to alter their NSG and create a rule with a higher priority (lower number) to allow the traffic.

