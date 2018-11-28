<properties  
              pageTitle="I can't connect to my Linux VM"
              description="I can't connect to my Linux VM"
              service=""
              resource=""
              authors="tiag"
              displayOrder="31"
              selfHelpType="generic"
              supportTopicIds="32615527"
              resourceTags=""
              productPesIds="15571,16215,16065,15797,16454,16470"
              cloudEnvironments="public"
/>

# I can't connect to my Linux VM

## **Recommended documents**

1. Click [here](https://docs.microsoft.com/azure/virtual-network/virtual-network-public-ip-address) for guidelines on how to create, change or delete a public IP address.
2. Click [here]( https://docs.microsoft.com/azure/virtual-network/manage-public-ip-address-prefix1) for guidelines on how to create, change or delete a public IP address prefix.
3. SSH to your VM from Internet may not work with forced tunneling enabled. Review [effective routes](data-blade:Microsoft_Azure_Network.EffectiveRoutesBlade.id.$resourceId). With forced tunneling, all outbound traffic destined to Internet will be redirected to on-premises.
4. Click [here](https://review.docs.microsoft.com/azure/virtual-machines/troubleshooting/troubleshoot-ssh-connection?branch=pr-en-us-54175) for detailed guidelines to troubleshoot SSH connection issues.
