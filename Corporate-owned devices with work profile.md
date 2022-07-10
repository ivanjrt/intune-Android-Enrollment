* Corporate-owned devices with work profile
![image](https://user-images.githubusercontent.com/44326428/178165307-6d341cea-91c7-4e68-9eee-525ab926e6fa.png)


For this type of profile a token(s) needs to be created (where it will have an expirity date). (Similar to Bring your own Device, but this time the owner is the Tenant)<br/>
![image](https://user-images.githubusercontent.com/44326428/178164665-d8796314-0630-4c12-a5b5-19f1932c8e0a.png)<br/>
![image](https://user-images.githubusercontent.com/44326428/178164725-4b3afa3c-7d51-46be-a916-50f167e0f568.png)<br/>

<br/>In order to bring it to the right Group a Dynamic Group will need to be created: <br/>
https://endpoint.microsoft.com/#blade/Microsoft_AAD_IAM/GroupsManagementMenuBlade/AllGroups
![image](https://user-images.githubusercontent.com/44326428/178164923-1234235a-5862-4bdf-9dcc-f06c0785ebb5.png)
Dynamic Rule Example = ``` (device.enrollmentProfileName -eq "Corporate-ownedDevicesWithWorkPprofile")```<br/>
because the profile created was "Corporate-ownedDedicatedDevices" then that will be the profile needs tbe in the Dynamic Rule.<br/>

Onboarding Experience:
* At the Welcome screen tap 7 times
* configure the Wi-Fi 
* login with User's UPN

for more information: <br/>
[Corporate-ownedDevicesWithWorkPprofile](https://www.inthecloud247.com/how-to-configure-android-corporate-owned-personally-enabled-user-devices-with-microsoft-intune/)
