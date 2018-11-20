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

## **Recommended documents**

1. Review [effective security group rules](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade.id.$resourceId) to ensure inbound “Allow” NSG rule exists and is prioritized for RDP port (default 3389).
2. Click [here](data-blade:microsoft_azure_network.verifyipflowblade.vmId.$resourceId) to ensure that Network Security Group is allowing traffic.
