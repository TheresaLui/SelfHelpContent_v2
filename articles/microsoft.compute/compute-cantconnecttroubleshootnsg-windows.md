<properties  
              pageTitle="I can't connect to my Windows VM"
              description="I can't connect to my Windows VM"
              service=""
              resource=""
              authors="tiag"
              displayOrder="37"
              selfHelpType="generic"
              supportTopicIds="32615533"
              resourceTags=""
              productPesIds="14749"
              cloudEnvironments="public"
/>

# I can't connect to my Windows VM

## **Recommended documents**

1. Review [effective security group rules](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade.id.$resourceId) to ensure inbound “Allow” NSG rule exists and is prioritized for RDP port (default 3389).
2. Click [here](data-blade:microsoft_azure_network.verifyipflowblade.vmId.$resourceId) to ensure that Network Security Group is allowing traffic.
