* Corporate-owned dedicated devices (Kiosks)
![image](https://user-images.githubusercontent.com/44326428/178163792-77a3e878-1393-486c-8923-6d976c75746d.png)

For this type of profile a token(s) needs to be created (where it will have an expirity date). Vision Oriented to have dedicated devices for different purposes <br/>
![image](https://user-images.githubusercontent.com/44326428/178164256-1c23bd12-410d-4cf6-a69c-0a941c490a7f.png)
![image](https://user-images.githubusercontent.com/44326428/178164285-94e64156-c1d9-451a-8a8c-550576c1e211.png)


<br/>In order to bring it to the right Group a Dynamic Group will need to be created: <br/>
https://endpoint.microsoft.com/#blade/Microsoft_AAD_IAM/GroupsManagementMenuBlade/AllGroups
Dynamic Rule Example = ``` (device.enrollmentProfileName -eq "Corporate-ownedDedicatedDevices") ```<br/>
because the profile created was "Corporate-ownedDedicatedDevices" then that will be the profile needs tbe in the Dynamic Rule.<br/>

Onboarding Experience:
* At the Welcome screen tap 7 times
* configure the Wi-Fi 
* The device should fall in the group assigned

for more information: <br/>
https://www.inthecloud247.com/how-to-start-with-android-enterprise-corporate-owned-dedicated-devices-in-microsoft-intune/