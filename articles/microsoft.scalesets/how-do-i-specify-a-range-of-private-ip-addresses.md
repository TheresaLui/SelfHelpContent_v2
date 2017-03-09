<properties
    pageTitle="How do I specify a range of private IP addresses"
    description="How do I specify a range of private IP addresses"
    service="scalesets"
    author="negat"
    displayOrder="57"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# How do I specify a range of private IP addresses, for static private IP address allocation?


IPs are selected from a subnet that you specify. 

The allocation method of scale set IPs is always “Dynamic”. It does not mean though that these IPs can change. It only means that you do not specify IP in PUT request. In other words, you specify the static set using the subnet. 
    