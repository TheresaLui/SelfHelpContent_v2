<properties
    pageTitle="If I add secrets to an existing scale set"
    description="If I add secrets to an existing scale set"
    service="scalesets"
    author="negat"
    displayOrder="32"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# If I add secrets to an existing scale set, does it inject them in existing instances, or only new ones? 


Certificates get added to all the VMs, even pre-existing ones. If your scale set upgradePolicy property is set to “Manual”, the certificate is added to the VM when you perform a manual update on the VM.
 