Apple's stance on managing iOS devices at the enterprise level has often been met with minimal native support from the company themselves. Their stance that iOS devices are personal devices to be managed by the individual end users has led the way for the growth of Mobile Device Management (MDM) software to aid in iOS management.

While there are many options to choose from, many MDM's require costly subscription licenses and/or infrastructure considerations that may be out of reach for some organizations, including public education and SMBs. Luckily, Apple Configurator 2 (AC2) includes many of the necessary functionality to manage iOS at a higher level with its supervision mode.

For those unfamiliar with how this works, we'll explore supervision, how it works, and how to configure devices for its use. But first, there are a few requirements necessary to make this work as intended.

Apple computer with macOS Mojave installed
Apple Configurator 2 (2.6 or later) installed
Internet access (Optional, but highly recommended to download applications)
iPad or iPhone device with iOS 12 (or later) installed
SEE: Mobile device computing policy (Tech Pro Research)

What is supervise mode?
Supervision was introduced in iOS 5 and has experienced many framework updates over the years as newer versions of iOS are introduced. While additional support for greater features continues to be included, the crux of supervise remains the same: To allow systems administrator's greater control over iOS devices by securing and allowing the configuration of features and functions, allowing these devices (typically enterprise-owned) to be locked down to prevent unauthorized changes that could otherwise lead to device compromise, and by extension, compromise the data and/or business network.

What features can be secured when a device is supervised?
This list of functions that are manageable are long--and continue to grow with the introduction of each new version of iOS. Among the more popular settings that admins can control include requiring passcodes for unlocking devices, setting minimum passcode lengths and complexity requirements, as well as timeouts and incorrect passcode lockouts, all of which protect data stored on devices from unauthorized access and data exfiltration in the event of loss or theft. Additional restrictions include setting profiles for corporate network and email access, company branding, and key escrow services that store a recovery key that may be used to bypass Activation Lock on iCloud-linked devices, for example.



Are there any requirements for a device to be supervised?
Any iOS device running iOS 5 (at least) is eligible for supervision. However, admins may wish to consult iOS release notes to verify that individual devices have the correct version of iOS installed so that support of required functions/features is adhered to. When supervising a device, ensure that existing data on the devices are backed-up since the supervision process erases all the data on the device and reinstalls (or upgrade) iOS, setting the foundation for the management platform.



Configuring a device for supervision
Login to the Mac computer and launch the Apple Configurator 2 (AC2) app.
Connect the device(s) to be configured to the Mac using the USB cable.
In AC2, select the iOS device you wish to configure, then click on Actions | Prepare... to launch the wizard.
Since AC2 can be used to prepare devices for MDM use, we are prompted with the Configuration type on the first page of the wizard. For the purposes of this article and since we are not configuring the device for MDM management, select Manual from the drop-down menu, then click the Next button.
On the next page, you'll be prompted to select the server to manage the device with post-AC2. Again, we will not be enrolling this device in an MDM, so we will select Do not enroll in MDM from the drop-down menu and click the Next button to proceed.
On the Supervise Devices page, you will be prompted to check the box next to Supervise devices, which enables supervision on that device. Additionally, if you wish to allow supervised devices to pair with their computers, check the box to allow that functionality. Otherwise, supervised devices will be disallowed from pairing with computers. Click the Next button to continue.
If you wish to enter information about the organization, you may do so on the following page. Enter the desired details and click the Next button.
When working with supervised devices, supervision identities are required. If setting up supervised devices for the first time, select the radio button next to Generate a New Supervision Identity to create a new one for your organization, then click Next to continue.
On the final page of the wizard, you will be prompted with choosing what options are presented to the end user during the Setup Assistant portion after the device is initialized. While optional, it is recommended that admins configure this portion by placing a check mark in the box next to each item you wish to allow the end user to configure--any boxes not checked will restrict end users from configuring those options during the Setup Assistant phase. Once these choices are configured, click the Prepare button to erase the device and reboot it in its newly supervised mode.