* Corporate-owned dedicated devices (Kiosks)
![image](https://user-images.githubusercontent.com/44326428/178163792-77a3e878-1393-486c-8923-6d976c75746d.png)
![image](https://user-images.githubusercontent.com/44326428/178165727-96beafd9-f501-494b-8ded-07cdc8b6afa8.png)
https://docs.microsoft.com/en-us/mem/intune/fundamentals/deployment-guide-enrollment-android#android-enterprise-dedicated-devices

For this type of profile a token(s) needs to be created (where it will have an expirity date). Vision Oriented to have dedicated devices for different purposes <br/>
![image](https://user-images.githubusercontent.com/44326428/178164256-1c23bd12-410d-4cf6-a69c-0a941c490a7f.png)
![image](https://user-images.githubusercontent.com/44326428/178164285-94e64156-c1d9-451a-8a8c-550576c1e211.png)


<br/>In order to bring it to the right Group a Dynamic Group will need to be created: <br/>
https://endpoint.microsoft.com/#blade/Microsoft_AAD_IAM/GroupsManagementMenuBlade/AllGroups
![image](https://user-images.githubusercontent.com/44326428/178164972-db25df94-132c-4ba8-b65c-b8695c102cc9.png)
Dynamic Rule Example = ``` (device.enrollmentProfileName -eq "Corporate-ownedDedicatedDevices") ```<br/>
because the profile created was "Corporate-ownedDedicatedDevices" then that will be the profile needs tbe in the Dynamic Rule.<br/>

# Onboarding Experience:
--GUI
* At the Welcome screen tap 7 times or at the email input type `afw#setup`
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
https://www.inthecloud247.com/how-to-start-with-android-enterprise-corporate-owned-dedicated-devices-in-microsoft-intune/
