<properties
    pageTitle="How does the secrets property of virtualMachineProfile"
    description="How does the secrets property of virtualMachineProfile"
    service="scalesets"
    author="negat"
    displayOrder="31"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# How does the secrets property of virtualMachineProfile.osProfile of a scale set work? Why do you need sourceVault when you have to specify the absolute URI to a certificate with certificateUrl? 

A Win RM certificate reference must be present in the secrets property of the OS profile. 
The purpose of indicating the source vault is to be able to enforce ACL policies that exist in CSM. Without specifying the source vault, users who do not have permissions to deploy/access secrets to a key vault would be able to through CRP. The ACLs exist even for resources that do not exist.
If you provided an incorrect sourceVault id but a valid key vault URL, we would report an error when you poll the operation