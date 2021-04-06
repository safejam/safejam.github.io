
from https://www.perfect-privacy.com/en/manuals/android_openvpn_app

- also see
  - https://www.howtogeek.com/218851/how-to-enable-always-on-vpn-on-an-iphone-or-ipad/
  - https://www.perfect-privacy.com/en/manuals/ios_ipsec_alwayson_supervised

*MY NOTE: The standard OpenVPN Connect app was buggy and didn't stay AlwaysOn. Following an android update it was then unsupported. The open source app worked fine.*  

Install OpenVPN for Android

Please first install the open source app OpenVPN for Android by Arne Schwabe on Google Play.
Show QR Code
Download an OpenVPN profile

Download the desired profile directly onto your smartphone. You can also scan the QR code below.

Our tip: Choose a location that is geographically as close as possible to achieve the best speed.
Show QR Code
OpenVPN for Android: Import VPN profile | OpenVPN for Android

Import OpenVPN profile

Open OpenVPN for Android and tap the Import icon to import the OpenVPN profile (package with arrow pointing down).

A file browser opens. In the Downloads folder, select the OpenVPN profile you just downloaded (in the example Chicago.ovpn).

If you cannot find the downloads folder immediately, you can also access it via the Burger menu at the top left (three lines).

OpenVPN for Android: Save the VPN profile | OpenVPN for Android

The OpenVPN profile now appears in OpenVPN for Android.

Save the new profile by tapping the checkmark in the upper right corner.

OpenVPN for Android: Establish a VPN connection | OpenVPN for Android

Establish a VPN connection

To establish the VPN connection, tap on the VPN profile.

The first time you establish a connection, you will be asked whether you want to allow the VPN connection. Confirm with OK.

You will then be asked for your login data. Enter your Perfect Privacy user name and password and check Save Password.

Confirm the credentials by tapping OK.

OpenVPN for Android: Check the VPN connection | OpenVPN for Android

After a short moment the OpenVPN connection has been established. You can recognize this by the OpenVPN-for-Android icon in the system bar at the top even when the app is closed.

When the connection is established, Initialization Sequence Completed appears at the bottom of the OpenVPN log.

You can verify that the VPN connection is working correctly by going to our Check-IP page.

OpenVPN for Android: Connect automatically | OpenVPN for Android

Enable the kill switch

If you want to ensure that all your Internet traffic passes through the VPN tunnel, you can now enable the kill switch.

Please note: With the kill switch activated, the Internet connection is only available if the VPN tunnel is up and running.

Open the OpenVPN for Android app again and open the Settings tab.

Tap on Default VPN and select the installed VPN profile.

Activate the checkbox next to Connect on boot.

OpenVPN for Android: Enable the kill switch | OpenVPN for Android

Then open the Android system settings.

Go to Network & Internet → VPN.

OpenVPN for Android: Kill-Switch einschalten | OpenVPN for Android

Tap on the gear next to OpenVPN for Android and activate the two options Always-on VPN and Block connections without VPN.

Details about the kill switch can be found in the OpenVPN for Android app on the FAQ tab.

Compatibility: Unfortunately, these options are not available on Huawei and Honor devices (EMUI interface) (as of Android 9.0).