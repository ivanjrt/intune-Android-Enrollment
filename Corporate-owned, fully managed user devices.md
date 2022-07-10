* Corporate-owned, fully managed user devices<br/>
![image](https://user-images.githubusercontent.com/44326428/178163262-1c697450-ba40-4dae-a72a-616d283e3d0f.png)

this method will generate a Unqiue BarCode Token for the tenant on which the user will have to scan.
![image](https://user-images.githubusercontent.com/44326428/178162184-8b6b12bb-aca1-41de-833d-f0869c86d918.png)

In order to bring it to the right Group a Dynamic Group will need to be created:<br/>
https://endpoint.microsoft.com/#blade/Microsoft_AAD_IAM/GroupsManagementMenuBlade/AllGroups<br/>
Dynamic Rule = ``` (device.deviceOSType -eq "AndroidEnterprise") and (device.enrollmentProfileName -eq Null)```
![image](https://user-images.githubusercontent.com/44326428/178162545-dcd352dd-c15d-4425-8bdf-bdeccef6cb83.png)

In order to onboard the phone when first turning on the phone at the Welcome Screen, User needs to Tap 7 times and then Wifi will need to be configured then upn from the customer needs to be put in, that way the Rule will apply and bring in user to the respective Assigment Groups<br/>
For Full imformation: https://vmlabblog.com/2020/07/corporate-owned-fully-managed-user-devices-cobo-with-intune/<br/>
![image](https://user-images.githubusercontent.com/44326428/178165443-ead74100-32be-4c05-906f-28da9207eac5.png)
