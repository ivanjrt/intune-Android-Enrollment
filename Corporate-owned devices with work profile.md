* Corporate-owned devices with work profile
![image](https://user-images.githubusercontent.com/44326428/178165307-6d341cea-91c7-4e68-9eee-525ab926e6fa.png)
![image](https://user-images.githubusercontent.com/44326428/178165706-d7dd074e-89ab-4c34-87ab-0ecd9320bd73.png)
https://docs.microsoft.com/en-us/mem/intune/fundamentals/deployment-guide-enrollment-android#android-enterprise-corporate-owned-work-profile


For this type of profile a token(s) needs to be created (where it will have an expirity date). (Similar to Bring your own Device, but this time the owner is the Tenant)<br/>
![image](https://user-images.githubusercontent.com/44326428/178164665-d8796314-0630-4c12-a5b5-19f1932c8e0a.png)<br/>
![image](https://user-images.githubusercontent.com/44326428/178164725-4b3afa3c-7d51-46be-a916-50f167e0f568.png)<br/>

<br/>In order to bring it to the right Group a Dynamic Group will need to be created: <br/>
https://endpoint.microsoft.com/#blade/Microsoft_AAD_IAM/GroupsManagementMenuBlade/AllGroups
![image](https://user-images.githubusercontent.com/44326428/178164923-1234235a-5862-4bdf-9dcc-f06c0785ebb5.png)
Dynamic Rule Example = ``` (device.enrollmentProfileName -eq "Corporate-ownedDevicesWithWorkPprofile")```<br/>
because the profile created was "Corporate-ownedDedicatedDevices" then that will be the profile needs tbe in the Dynamic Rule.<br/>

# Onboarding Experience:
--GUI
* At the Welcome screen tap 7 times
* configure the Wi-Fi 
* The device should fall in the group assigned<br/>
![image](https://user-images.githubusercontent.com/44326428/178165564-8bbdf1e4-eb9b-40d2-ade2-8614be91cd00.png)

</br> **or** <br/>

-- Steps on the Device: <br/>
https://learn.microsoft.com/en-us/mem/intune/enrollment/android-dedicated-devices-fully-managed-enroll#steps<br/>
Turn on your wiped device.<br/>
On the Welcome screen, select your language.<br/>
Connect to your Wi-fi, and then choose NEXT.<br/>
Accept the Google Terms and conditions, and then choose NEXT.<br/>
On the Google sign-in screen, enter **afw#setup** instead of a Gmail account, and then choose NEXT.<br/>
Choose INSTALL for the Android Device Policy app.<br/>
Continue installation of this policy. Some devices may require additional terms acceptance.<br/>
On the Enroll this device screen, allow your device to scan the QR code. Or, choose to enter the token manually.<br/>
Follow the on-screen prompts to complete enrollment.<br/>

for more information: <br/>
[Corporate-ownedDevicesWithWorkPprofile](https://www.inthecloud247.com/how-to-configure-android-corporate-owned-personally-enabled-user-devices-with-microsoft-intune/)

