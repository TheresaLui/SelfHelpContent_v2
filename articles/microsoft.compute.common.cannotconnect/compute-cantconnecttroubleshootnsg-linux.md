<properties  
              pageTitle="Troubleshoot my network security group (NSG)"
              description="Troubleshoot my network security group (NSG)"
              service=""
              resource=""
              authors="scottAzure,timbasham"
              ms.author="scotro,tibasham"
              displayOrder=""
              selfHelpType="generic"
              supportTopicIds="32615533"
              resourceTags=""
              productPesIds="15571,15797,16454,16470"
              cloudEnvironments="public"
/>

# Troubleshoot my Network Security Group (NSG)

4 out of 5 customers resolved their VM Network Security Group issue using the steps below.<br>

## **Recommended Steps**

NSGs by default deny connections from Internet unless it is explicitly allowed. To resolve this issue, try one or more of the below steps.<br>

1. Use [IP flow verify](data-blade:microsoft_azure_network.verifyipflowblade.id.$subscriptionId) to confirm if a rule in a Network Security Group is blocking traffic to or from a virtual machine.<br>
2. Edit the [Network Security Group](https://docs.microsoft.com/azure/virtual-network/manage-network-security-group) to make changes to the rules if needed.<br>
3. If there is no rule to allow the traffic from Internet, add a new rule to allow access to the backend port, with source being 'Internet', '\*' or a specific public IP address.

## **Recommended Documents**

* [How to troubleshoot Network Security Groups (NSGs)](https://blogs.msdn.microsoft.com/mvpawardprogram/2018/05/08/troubleshoot-nsgs)<br>
* [How to configure Network Watcher to troubleshoot NSG issues](https://docs.microsoft.com/azure/network-watcher/network-watcher-create)<br>
* [How to read NSG logs generated from Network Watcher](https://docs.microsoft.com/azure/network-watcher/network-watcher-read-nsg-flow-logs)<br>
* [Filter network traffic with a network security group using the Azure Portal](https://docs.microsoft.com/azure/virtual-network/tutorial-filter-network-traffic)
