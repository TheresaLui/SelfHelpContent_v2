<Do not merge yet!
Correct step 1 for RouteTable blade path.>
<properties
	pageTitle="I am unable to connect to virtual machines in the same VNet when using an UDR."
	description="Troubleshoot connectivity to VM in the same VNet when using an UDR"
	service="Virtual Network"
	resource="User Defined Routes"
	authors="radwiv, narayan"
	displayOrder="1"
	selfHelpType="resource"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public"
/>

# I am unable to connect to virtual machines in the same VNet when using an UDR.

## **Recommended steps**
If you are using User defined routes in your virtual network subnets and have connectivity issues, try one or more of the below steps to resolve the issue.<br>

1. Review [Route Table](data-blade:Microsoft_Azure_Insights.AzureDiagnosticsBladeWithParameter)
2. Check the route entries to ensure the destination address you are having issues with is covered by one or more routes. Communication within the Virtual network, to on-premises and to Internet is covered by system routes.<br>
[User defined routes overview](https://azure.microsoft.com/en-us/documentation/articles/virtual-networks-udr-overview/)
3. Check that the destination is reachable from other sources.<br>
4. Check that the Network security group rules on both source and destination allow this traffic.<br>
5. If you are using a NVA to route the traffic through, check that the NVA VM is running and 'IP Forwarding' is enabled.<br>
6. Check to validate that NVA is not in the same subnet as the source virtual machine. This will create a route loop.<br>

## **Recommended documents**

[User defined routes design considerations](https://azure.microsoft.com/en-us/documentation/articles/best-practices-network-security/#examples-building-security-boundaries-with-azure-virtual-networks)