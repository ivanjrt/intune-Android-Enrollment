# Prerequisites:
# Connect a Google Account to the Tenant
https://endpoint.microsoft.com/#blade/Microsoft_Intune_DeviceSettings/DevicesEnrollmentMenu/androidEnrollment
![image](https://user-images.githubusercontent.com/44326428/178161538-cbbae58d-8c7f-43a5-b0ef-7bf93b1d4779.png)
![image](https://user-images.githubusercontent.com/44326428/178161607-516035f2-3e34-4573-9f63-85565e522591.png)

# * Android Enterprise Managment:
This Type of Managment is handled by Google However Intune has works in partnership to deliver and Receive most configurations for Android via Google APIs <br/>
# Prerequisites:
* Android OS version 8.0 and above. <br/>
* Devices must run a distribution of Android that has Google Mobile Services (GMS) connectivity. Devices must have GMS available and must be able to connect to GMS <br/> 
*  <a href="https://docs.microsoft.com/en-us/mem/intune/enrollment/android-kiosk-enroll#create-an-enrollment-profile">Create an enrollment profile.</a>
# Enrollment Profiles:
https://endpoint.microsoft.com/#blade/Microsoft_Intune_DeviceSettings/DevicesEnrollmentMenu/androidEnrollment<br/>



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


