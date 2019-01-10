<properties  
              pageTitle="Troubleshoot my network security group (NSG)"
              description="Troubleshoot my network security group (NSG)"
              service=""
              resource=""
              authors="scottAzure"
              ms.author="scotro"
              displayOrder=""
              selfHelpType="generic"
              supportTopicIds="32615533"
              resourceTags=""
              productPesIds="15571,15797,16454"
              cloudEnvironments="public"
/>

# Troubleshoot my Network Security Group (NSG)

4 out of 5 customers resolved their VM Network Security Group issue using the steps below.<br>

## **Recommended Steps**

NSGs by default deny connections from Internet unless it is explicitly allowed. To resolve this issue, try one or more of the below steps.<br>

1. Open the [Security Rules blade](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade.id.$resourceId).<br>
2. Review the [effective security group rules](https://docs.microsoft.com/azure/virtual-network/security-overview).<br>
3. If a load balancer is present, check if the backend port used in the load balancer rule configuration is in the allow list.<br>
4. If there is no rule to allow the traffic from Internet, add a new rule to allow access to backend port, with source being 'Internet', '\*' or a specific public IP address.

## **Recommended Documents**

* [How to troubleshoot Network Security Groups (NSGs)](https://blogs.msdn.microsoft.com/mvpawardprogram/2018/05/08/troubleshoot-nsgs)<br>
* [How to configure Network Watcher to troubleshoot NSG issues](https://docs.microsoft.com/azure/network-watcher/network-watcher-create)<br>
* [How to read NSG logs generated from Network Watcher](https://docs.microsoft.com/azure/network-watcher/network-watcher-read-nsg-flow-logs)
