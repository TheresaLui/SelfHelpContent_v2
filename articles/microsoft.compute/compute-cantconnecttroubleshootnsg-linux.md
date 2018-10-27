<properties  
              pageTitle="I can't connect to my Linux VM"
              description="I can't connect to my Linux VM"
              service=""
              resource=""
              authors="tiag"
              displayOrder="37"
              selfHelpType="generic"
              supportTopicIds="32615533"
              resourceTags=""
              productPesIds="15571,16215,16065,15797,16454,16470"
              cloudEnvironments="public"
/>

# I can't connect to my Linux VM

## **Recommended documents**

1. Review [effective security group rules](data-blade:Microsoft_Azure_Network.EffectiveSecurityRulesBlade) to ensure inbound “Allow” NSG rule exists and is prioritized for SSH port (default 22).
2. Click [here](data-blade:microsoft_azure_network.verifyipflowblade.vmId.$resourceId) to ensure that Network Security Group is allowing traffic.
