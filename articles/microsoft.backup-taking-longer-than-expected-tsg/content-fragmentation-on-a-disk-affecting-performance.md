<properties
	pageTitle="Fragmentation on a disk affecting performance"
	description="Fragmentation on a disk affecting performance"
	service=""
	resource=""
	authors="TestAuthor"
	ms.author="TestAuthor"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ba6cf1af-102d-492d-b8cd-56ffcaff8296"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Fragmentation on a disk affecting performance

1. Please engage your TA for mitigation steps actions to defrag a disk
2. If this a windows VM we would recommend the customer to **DeFragment** the disk and **TRIM** it.
3. Use the below two links to defrag and trim the disk on windows

1.  [https://www.howtogeek.com/257196/how-to-check-if-trim-is-enabled-for-your-ssd-and-enable-it-if-it-isnt/](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fwww.howtogeek.com%2F257196%2Fhow-to-check-if-trim-is-enabled-for-your-ssd-and-enable-it-if-it-isnt%2F&data=02%7C01%7Craagg%40microsoft.com%7Cf14541ccd9dc4fe7397e08d6b75ba794%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636898001690197901&sdata=8gWceo5OfJoPQruidZy6RotQMNEB%2F4fRUMvA6uhgTJI%3D&reserved=0)?
2. [http://fabriccontroller.net/releasing-unused-space-from-your-windows-azure-virtual-hard-disk-reduce-billable-size/](https://nam06.safelinks.protection.outlook.com/?url=http%3A%2F%2Ffabriccontroller.net%2Freleasing-unused-space-from-your-windows-azure-virtual-hard-disk-reduce-billable-size%2F&data=02%7C01%7Craagg%40microsoft.com%7Cf14541ccd9dc4fe7397e08d6b75ba794%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636898001690197901&sdata=3JDtWMxeQrzYZB9VJr7C2T04hzamLDwxYHgN0SxRx1g%3D&reserved=0)?

**Basically 3 steps should be performed:**

1. Check if trim is enabled

~~~shell

    fsutil behavior query DisableDeleteNotify

~~~

This will tell us if TRIM is enabled or not. If return is 0, skip to step 3.

2.  To enable TRIM, run the below query:

~~~shell

    fsutil?behavior set?DisableDeleteNotify?0

~~~

3. Run the defrag against the drive in case it hasn't been able to keep up. Ensure to run this step twice.


~~~shell

    Optimize-Volume -DriveLetter?<replace with drive letter?eg: F> -ReTrim

~~~

## Recommended Documents

Other links related to trim functionality are:

1. [https://docs.microsoft.com/en-us/azure/virtual-machines/windows/about-disks-and-vhds\#one-last-recommendation-use-trim-with-unmanaged-standard-disks](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fdocs.microsoft.com%2Fen-us%2Fazure%2Fvirtual-machines%2Fwindows%2Fabout-disks-and-vhds%23one-last-recommendation-use-trim-with-unmanaged-standard-disks&data=02%7C01%7Craagg%40microsoft.com%7Cf14541ccd9dc4fe7397e08d6b75ba794%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636898001690207894&sdata=2GAbQoiPoB%2BU8R5DEbtx8fE0fF%2BlknWukrwlXed2vbM%3D&reserved=0)
2. [https://blogs.technet.microsoft.com/tip\_of\_the\_day/2014/09/18/cloud-tip-of-the-day-microsoft-azure-supports-trim/](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fblogs.technet.microsoft.com%2Ftip_of_the_day%2F2014%2F09%2F18%2Fcloud-tip-of-the-day-microsoft-azure-supports-trim%2F&data=02%7C01%7Craagg%40microsoft.com%7Cf14541ccd9dc4fe7397e08d6b75ba794%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636898001690207894&sdata=FBCi75R370i%2FR6VVpI7qVmH1EUaOfD3Rdj7bJp0wNyY%3D&reserved=0)
3. [http://fabriccontroller.net/releasing-unused-space-from-your-windows-azure-virtual-hard-disk-reduce-billable-size/](https://nam06.safelinks.protection.outlook.com/?url=http%3A%2F%2Ffabriccontroller.net%2Freleasing-unused-space-from-your-windows-azure-virtual-hard-disk-reduce-billable-size%2F&data=02%7C01%7Craagg%40microsoft.com%7Cf14541ccd9dc4fe7397e08d6b75ba794%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636898001690217889&sdata=qT41JAPhxQ8%2FlJo14m6JIXgMJwANyjahcVtIi080jBg%3D&reserved=0)
4. [http://mvwood.com/blog/trim-support-comes-to-windows-azure-virtual-machines/](https://nam06.safelinks.protection.outlook.com/?url=http%3A%2F%2Fmvwood.com%2Fblog%2Ftrim-support-comes-to-windows-azure-virtual-machines%2F&data=02%7C01%7Craagg%40microsoft.com%7Cf14541ccd9dc4fe7397e08d6b75ba794%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636898001690217889&sdata=J8PlJeQRALg92O4rhanjMNgrFlub%2FuDMJSEun1fZ2RM%3D&reserved=0)
5. [https://en.wikipedia.org/wiki/Trim\_(computing)](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fen.wikipedia.org%2Fwiki%2FTrim_\(computing\)&data=02%7C01%7Craagg%40microsoft.com%7Cf14541ccd9dc4fe7397e08d6b75ba794%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636898001690227888&sdata=2Hty%2Fb4UcuwaXagQOkxFTXa%2FytcnreivEjwrx677JGs%3D&reserved=0)
6. [https://www.howtogeek.com/257196/how-to-check-if-trim-is-enabled-for-your-ssd-and-enable-it-if-it-isnt/](https://nam06.safelinks.protection.outlook.com/?url=https%3A%2F%2Fwww.howtogeek.com%2F257196%2Fhow-to-check-if-trim-is-enabled-for-your-ssd-and-enable-it-if-it-isnt%2F&data=02%7C01%7Craagg%40microsoft.com%7Cf14541ccd9dc4fe7397e08d6b75ba794%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C636898001690227888&sdata=CjJ8pcV09xPItpnE%2FRCBkuxRSTIqYuvJPGYtRNAQp4E%3D&reserved=0)
7. [Reference ICM](https://icm.ad.msft.net/imp/v3/incidents/details/113050204/home)
