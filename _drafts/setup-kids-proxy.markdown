You will need
1. Access to AWS
2. An Apple MacOS computer with Apple Configuration


On the MacOS computer, install 'Apple Configurator 2' from the app store

Open Apple configurator and click 'Get Started'

Ensure the iphone is connected to the MacOS computer via USB. If you don't see a charging indicator, try another cable.

Trust This Computer?
Your settings and data will be accesible from 'MacOS Computer' when connecting wirelessly or using a cable.
Tust or Don't Trust

Create a new configuration profile

Set general settings
Enter MySafeInternet or family information
Add a password for security regarding profile removal. (Same as profile name for testing)
<screenshot>

Restrictions
Not required in this solution but you may make personal choices

Domains
Not configured

Global HTTP Proxy
Proxy Type = Manual
Proxy Server and Port = DNS Name of your instance or provided by MySafeInternet service
User Name & Password = <blank> (Access to the proxy server will be secured by source UP address)
Allow bypassing proxy to access captive networks = Yes

The reason we allow bypassing proxy to access captive networks is so the kids can connect to guest Wi-Fi solutions at Starbucks, McDonalds etc.

In the business world, this is sometimes not allowed in case someone sets up a fake hotspot to capture logon information.

If your kids have an unlimited data plan on their mobiles or you're happy to top up their credit when needed, then you can leave this box checked for maximum security. 

DNS Proxy
- How to configure??

Content Filter
Filter Type = 'Built-in: Limit Adult Content'

Configure any other settings as required

Click File -> Save
Check it has saved correctly (The name will change at the top) and close the profile.

# Existing iPhone

## From Jamf
https://www.jamf.com/jamf-nation/discussions/14111/unsupervised-or-supervised-ios

1. Disable "Find my iPad” on the old iOS device, perform iCloud backup on the same device
2. Plug in the new device to Apple Configurator, Supervise and update the device to the latest iOS
3. Once Supervised, unplug the new device and go through the Setup Assistant to restore from iCloud
4. When the iCloud restore of the new device is complete, do not touch the Setup Assistant, plug it back into Configurator
5. Before you refresh, change the "Restore" and "Update iOS" options to "Do not Update/Restore"
6. Once refreshed, proceed through the Setup Assistant, your device should now be Supervised and ready for MDM Enrollment

## No iCloud Storage - this did not work

1. Two-finger click on the device in Apple Configurator and select 'Backup...' The phone will backup.
   <insert Screenshot>

## iCloud Backup

1. Go into the Settings app on the iPhone, select 'iCloud' and then 'iCloud Backup'
2. Verify a recent backup or click 'Backup Now'
3. Once backup has completed, update the device

## Update
4. Two-finger click on the device in Apple Configurator and select 'Update...' Apple Configurator will download and install the latest system update for iOS.

## Prepare the iPhone for supervision
??? NOTE: If you try to set up the device without signing out then the device will be activation locked and will ask you for the iTunes account and password after reset, and will not allow you to complete the setup. ???

Two-finger click on the device in Apple Configurator and select 'Prepare...'
<screenshot>
Prepare with manual configuration. Check the 'Supervise devices' box and optionally, 'Allow other devices to pair with other computers'. Click 'Next'.

'Do not enroll in MDM' Click 'Next'

Click Skip when asked to 'Sign in to Apple School Manager or Apple Business Manager'

Enter 'MySafeInternet' or your family details when asked to 'Create an Organization'

Generation a new supervision identity if this is your first device configuration, or Choose an existing supervision identity, then click Next

Choose which steps will be presented to the user in Setup Assistant. If a brand new phone is being configured, select 'Show all steps', but if you plan to restore from a backup, select 'Don't show any of these steps. Click 'Prepare'.

'You are making changes to your Certificate Trust Settings' Enter your password to allow this.

'Configurator could not perform the requested actions becaise "iPhone" has already been prepared. Click "Erase" to erase and prepare the device again. All content and settings will be deleted. This cannot be undone.'

Click 'Erase'

'Preparing "iPhone" <screenshot>
Step 3 halts when the phone has powered up and requires access to a Wi-Fi network.
Enter your network details on the iPhone and click 'Join'.

NOTE: The iPhone will now be shown in the 'Supervised' window of Apple Configurator. <screenshot>. When you open the settings app on the iPhone it will report 'This iPhone is supervised and managed by MySafeInternet'

## Add the profile you created earlier
Two-finger click on the device in Apple Configurator and select 'Add > Profiles...'
Select the profile you saved earlier, and click 'Add'
The consent box will pop-up; click 'Accept'

## Log into the iPhone & restore a backup

In the settings app, log in with your Apple ID.
Once logged in, select General > Reset, then tap Erase All Content and Settings. Click 'Erase iPhone' & confirm.
The phone will reset.
Follow the on-screen prompts to setup the phone, with language, Wi-Fi and security. On the 'Apps & Data' screen, select 'Restore from iCloud Backup'
Login with your Apple ID
On the 'Choose Backup' screen, select your backup.
Click 'Continue to restore the settings
Select preferences for Siri & Analytics
The 'Restore from iCloud' screen will now restore all the Apps & Data, and restart the iPhone again

## ISSUE: This reverted to unspervised after restoring apps & data

# Remember! Before you start, disable Find My Phone!

# Updated process after the previous didn't work!
Two-finger click on the device in Apple Configurator and select 'Prepare...'
<screenshot>
Prepare with manual configuration. Check the 'Supervise devices' box and optionally, 'Allow other devices to pair with other computers'. Click 'Next'.

'Do not enroll in MDM' Click 'Next'

Click Skip when asked to 'Sign in to Apple School Manager or Apple Business Manager'

Enter 'MySafeInternet' or your family details when asked to 'Create an Organization'

Generation a new supervision identity if this is your first device configuration, or Choose an existing supervision identity, then click Next

Choose which steps will be presented to the user in Setup Assistant. Select 'Show only some steps' and only select 'Apps & Data'. Click 'Prepare'.

'You are making changes to your Certificate Trust Settings' Enter your password to allow this. (This is only shown once ever)

'Configurator could not perform the requested actions because "iPhone" has already been prepared. Click "Erase" to erase and prepare the device again. All content and settings will be deleted. This cannot be undone.'

Click 'Erase'

'Preparing "iPhone" <screenshot>
The iPhone will power on and display its 'Hello' screen.

### New error for Adam's phone at this point:
NOTE: You may see an error like 'Unable to activate "iPhone". The device may be activation locked. Continue on the device or use Finder to activate, and then click Try Again'

*Above error is likely becuase 'Find my phone' wasn't disabled.*

I clicked 'Stop' and continued with manual setup on the phone. After connecting to Wi-Fi it prompted: 'This phone is linked to an Apple ID. Enter the Apple ID and password that were used to setup this iPhone.


Step 3 of the 'Preparing iPhone'process halts when the phone requires access to a Wi-Fi network.
Enter your network details on the iPhone and click 'Join'.



On the Apps & Data screen, select 'Restore from iCloud Backup'.
Login to icloud using your Apple ID.
On the 'Choose Backup' screen, select your backup. The backup will be downloaded.
On the 'Restore Completed' screen, click 'Continue'
Select preferences for Touch Id, Passcode, Location Services, Siri, Analytics, Zoom, then click 'Get Started'.


On the MacOS computer & in the Apple configurator, the iPhone has now moved/will be shown in the 'Supervised' window of Apple Configurator. <screenshot>. 

### This didnt happen (when restoring a backup taken from the same phone)
When you open the settings app on the iPhone it will report 'This iPhone is supervised and managed by MySafeInternet'

## Add the profile you created earlier
Two-finger click on the device in Apple Configurator and select 'Add > Profiles...'
Select the profile you saved earlier, and click 'Add'

'Configurator requires user interaction to install the profile "MySafeInternet" on "iPhone" becuase it is not supeorvised. Tap install on the device to continue installing the profile.

'Profile Downloaded. Review the profile in the settings app if you want to install it' Click Close

Click 'Profile' in 'Settings'. The 'MySafeInternet' install profile will appear. Click 'Install'
On the Consent screen, click 'Next'
On the Warning screen, click 'Install' & confirm the warning about profile removal. We can use the password from the profile when we created it in Apple Configurator.

Profile Installation Failed. This profile can only be installed on a supervised device.





<screenshot>


Powering down your proxy overnight.


Apple Configurator
https://support.apple.com/en-gb/apple-configurator

Create and edit configuration profiles in Apple configurator 2
https://support.apple.com/en-gb/guide/apple-configurator-2/pmd85719196/2.13/mac/10.15.6

https://www.jamf.com/jamf-nation/discussions/14111/unsupervised-or-supervised-ios
https://support.apple.com/en-gb/guide/icloud/mm7e756df7fd/icloud