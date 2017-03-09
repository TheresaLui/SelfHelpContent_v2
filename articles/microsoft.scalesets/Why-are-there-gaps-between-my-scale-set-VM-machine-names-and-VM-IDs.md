<properties
    pageTitle="Why are there gaps between my scale set VM machine names and VM IDs"
    description="Why are there gaps between my scale set VM machine names and VM IDs"
    service="scalesets"
    author="negat"
    displayOrder="5"
    selfHelpType="resource"
    supportTopicIds=""
    productPesIds=""
    resourceTags=""
    cloudEnvironments="public"
/>

# Why are there gaps between my scale set VM machine names and VM IDs? For example: 0, 1, 3...


There are gaps because your scale set overprovision property is set to the default value of true. With overprovisioning true, more VMs than requested are created, and the extra VMs are subsequently deleted. What you gain is increased deployment reliability at the expense of contiguous naming and contiguous NAT rules. You can set this property to false, and for small scale sets it won’t make much difference to deployment reliability.
