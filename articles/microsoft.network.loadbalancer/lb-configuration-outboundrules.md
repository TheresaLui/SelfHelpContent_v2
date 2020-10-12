<properties
	pageTitle="Azure Load Balancer Configuration Issues - Outbound Rules"
	description="Azure Load Balancer Configuration Issues - Outbound Rules"
	service="microsoft.network"
	resource="loadbalancers"
	authors="irenehua"
	ms.author="irenehua"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds=""
	resourceTags=""
	productPesIds="16098"
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="8deb7553-0965-45d3-a66d-895655a50a6b"
	ownershipId="CloudNet_LoadBalancer"
/>

# Azure Load Balancer backend pool connection issues

## **Troubleshooting Insights**
* Outbound rule is only available for [Standard Load Balancer](https://docs.microsoft.com/azure/load-balancer/load-balancer-overview#why-use-azure-load-balancer). 
* You can use outbound rule to control which virtual machines should be translated to which Public IP address. Learn more about outbound rule definition here. 
* Configure idle timeout between 4 to 30 minutes and enable tcp reset for outbound rules according to your need. Read more [here](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections#outbound-rule-definition).
* Scenarios you can achieve with outbound rules 
  1. Groom outbound connections to a [specific set of Public IP addresses](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections#scenarios-with-outbound-rules) 
  2. [Modify SNAT port allocation](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections#scenarios-with-outbound-rules)
  3. [Outbound NAT for VMs only (no inbound)](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections#scenarios-with-outbound-rules) with Network Security Group 
  4. Outbound NAT for [internal Standard Load Balancer](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections#scenarios-with-outbound-rules) 
  5. [Enable both TCP & UDP protocols](https://docs.microsoft.com/azure/load-balancer/load-balancer-outbound-connections#scenarios-with-outbound-rules) for outbound NAT with Public Standard Load Balancer 
* Outbound rules can only be applied to primary IP configuration of NIC. You cannot create an outbound rule for secondary IP of a VM or NVA.  
