* Corporate-owned, fully managed user devices<br/>
![image](https://user-images.githubusercontent.com/44326428/178163262-1c697450-ba40-4dae-a72a-616d283e3d0f.png)
![image](https://user-images.githubusercontent.com/44326428/178165778-ed23b21f-2dca-43cd-bd7d-e9309c91ea6e.png)

# Steps on the Device: <br/>
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


https://docs.microsoft.com/en-us/mem/intune/fundamentals/deployment-guide-enrollment-android#android-enterprise-fully-managed<br/>
this method will generate a Unqiue BarCode Token for the tenant on which the user will have to scan.
![image](https://user-images.githubusercontent.com/44326428/178162184-8b6b12bb-aca1-41de-833d-f0869c86d918.png)

In order to bring it to the right Group a Dynamic Group will need to be created:<br/>
https://endpoint.microsoft.com/#blade/Microsoft_AAD_IAM/GroupsManagementMenuBlade/AllGroups<br/>
Dynamic Rule = ``` (device.deviceOSType -eq "AndroidEnterprise") and (device.enrollmentProfileName -eq Null)```
![image](https://user-images.githubusercontent.com/44326428/178162545-dcd352dd-c15d-4425-8bdf-bdeccef6cb83.png)

In order to onboard the phone when first turning on the phone at the Welcome Screen, User needs to Tap 7 times and then Wifi will need to be configured then upn from the customer needs to be put in, that way the Rule will apply and bring in user to the respective Assigment Groups<br/>
For Full imformation: https://vmlabblog.com/2020/07/corporate-owned-fully-managed-user-devices-cobo-with-intune/<br/>
![image](https://user-images.githubusercontent.com/44326428/178165443-ead74100-32be-4c05-906f-28da9207eac5.png)
