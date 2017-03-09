<properties
    pageTitle="How do I remove deprecated certificates"
    description="How do I remove deprecated certificates"
    service="scalesets"
    author="negat"
    displayOrder="27"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# How do I remove deprecated certificates? 

You must remove the old certificate from the vault certificates list but leave all the certificates that you want to remain on your machine. Doing so does not remove the certificate from all your VMs, but it also does not add the certificate to new VMs that are created in the scale set. To remove the certificate from existing VMs, you must write a custom script extension that removes the certificates from your certificate store manually.