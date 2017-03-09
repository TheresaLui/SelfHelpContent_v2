<properties
    pageTitle="Are there ways to parse unique arguments to extensions in scale sets"
    description="Are there ways to parse unique arguments to extensions in scale sets"
    service="scalesets"
    author="negat"
    displayOrder="4"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Are there ways to parse unique arguments to extensions in scale sets?

No, but extensions can act based on unique properties of the VM they are running on, such as the machine name. Additionally, extensions can query instance metadata on http://169.254.169.254 to get more information.