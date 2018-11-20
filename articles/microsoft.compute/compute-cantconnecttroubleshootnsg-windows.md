<properties  
              pageTitle="Troubleshoot my network security group (NSG)"
              description="Troubleshoot my network security group (NSG)"
              service=""
              resource=""
              authors="tiag"
              displayOrder=""
              selfHelpType="generic"
              supportTopicIds="32615533"
              resourceTags=""
              productPesIds="14749"
              cloudEnvironments="public"
/>

# I can't connect to my Windows VM

4 out of 5 customers resolved their connectivity issue using below steps:<br>

## **Recommended steps**

NSGs by default deny connections from Internet unless it is explicitly allowed. To resolve this issue, try one or more of the below steps.<br>

1. Open the [security rules in your NSG](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade.id.$resourceId).<br>
2. Review the [effective security group rules](https://docs.microsoft.com/azure/virtual-network/security-overview).<br>
3. Check if the backend port used in the load balancer rule configuration is in the allow list.<br>
3. If there is no rule to allow the traffic from Internet, add a new rule to allow access to backend port, with source being 'Internet', '\*' or a specific public IP address.

## **Recommended documents**

* [Understand  how to troubleshooting Network Security Groups (NSGs)](https://blogs.msdn.microsoft.com/mvpawardprogram/2018/05/08/troubleshoot-nsgs)<br>
* [How to configure Network Watcher to troubleshoot NSG issues](https://docs.microsoft.com/azure/network-watcher/network-watcher-create)<br>
* [How to read NSG looks generated from Network Watcher](https://docs.microsoft.com/azure/network-watcher/network-watcher-read-nsg-flow-logs)<br>
