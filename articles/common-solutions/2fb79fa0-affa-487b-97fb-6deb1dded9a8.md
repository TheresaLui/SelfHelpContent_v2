<properties
  pagetitle="ASE Pro R Setup and Local UI"
  service=""
  resource=""
  ms.author="hadhand"
  selfhelptype="Generic"
  supporttopicids="32785555"
  productpesids="17132"
  cloudenvironments="public, fairfax, mooncake, blackforest, ussec, usnat"
  disableclouds=""
  articleid="2fb79fa0-affa-487b-97fb-6deb1dded9a8"
  ownershipid="StorageMediaEdge_AzureStack_Edge" />
# ASE Pro R Setup and Local UI

You can connect to your Azure Stack Edge Pro R device by using the local web UI.

The connection process can take around 5 minutes to complete.

## **Recommended Steps**

1. Configure the Ethernet adapter on your computer to connect to the Azure Stack Edge Pro R device with a static IP address of 192.168.100.5 and subnet 255.255.255.0.
2. Connect the computer to PORT 1 on your device. If connecting the computer to the device directly (without a switch), use a crossover cable or a USB Ethernet adapter. Use the following illustration to identify PORT 1 on your device.
3. Open a browser window and access the local web UI of the device at https://192.168.100.10.

This action may take a few minutes after you've turned on the device.

## **Recommended Documents**

* [Setting up ASE Pro R with Local UI](https://docs.microsoft.com/azure/databox-online/azure-stack-edge-pro-r-deploy-connect)

**Note:** At the prompt, change the device administrator password. The new password must contain between 8 and 16 characters. It must contain three of the following characters: uppercase, lowercase, numeric, and special characters.
