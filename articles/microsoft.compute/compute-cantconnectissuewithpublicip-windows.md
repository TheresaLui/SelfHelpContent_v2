<properties  
              pageTitle="I can't connect to my Windows VM"
              description="I can't connect to my Windows VM"
              service="microsoft.compute"
              resource="virtualmachines"
              authors="tiag"
              displayOrder="1"
              selfHelpType="resource"
              supportTopicIds="32615527"
              resourceTags="windows, windowsSQL"
              productPesIds="14749"
              cloudEnvironments="public"
/>

# I can't connect to my Windows VM

## **Recommended documents**

1. Click [here](https://docs.microsoft.com/azure/virtual-network/virtual-network-public-ip-address) for guidelines on how to create, change or delete a public IP address.
2. Click [here]( https://docs.microsoft.com/azure/virtual-network/manage-public-ip-address-prefix1) for guidelines on how to create, change or delete a public IP address prefix.
3. If you are using VPN S2S, RDP to your VM from Internet may not work with forced tunneling enabled. Review [effective routes](data-blade:Microsoft_Azure_Network.EffectiveRoutesBlade.id.$resourceId) With forced tunneling, all outbound traffic destined to Internet will be redirected to on-premises.
4. Click [here](https://review.docs.microsoft.com/azure/virtual-machines/troubleshooting/detailed-troubleshoot-rdp?branch=pr-en-us-54175) for detailed guidelines to troubleshoot RDP connection issues.
