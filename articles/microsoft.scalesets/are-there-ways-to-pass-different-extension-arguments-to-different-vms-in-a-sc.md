<properties
    pageTitle="Are there ways to pass different extension arguments to different VMs in a scale set"
    description="Are there ways to pass different extension arguments to different VMs in a scale set"
    service="scalesets"
    author="negat"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Are there ways to pass different extension arguments to different VMs in a scale set?


No, but extensions can act based on unique properties of the VM they are running on, such as the machine name. Additionally, extensions can query instance metadata on http://169.254.169.254 to get more information.
