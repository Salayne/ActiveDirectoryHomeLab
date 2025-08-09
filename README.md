**Windows Server & Active Directory:**
- Set up a virtual machine with Windows Server 2022.
- Install and configure the Active Directory Domain Services (AD DS) role.
  ![image alt](https://github.com/Salayne/ActiveDirectoryHomeLab/blob/main/OUs/instlWinServ-11.png)
  ![image alt](https://github.com/Salayne/ActiveDirectoryHomeLab/blob/main/OUs/windowsServerSearch.png)
 ![image alt](https://github.com/Salayne/ActiveDirectoryHomeLab/blob/main/OUs/ADUsersMenu.png)

  
- Create several virtual user accounts and organizational units (OUs)
![image alt](https://github.com/Salayne/ActiveDirectoryHomeLab/blob/main/OUs/creatingOU1.png)
![image alt](https://github.com/Salayne/ActiveDirectoryHomeLab/blob/main/OUs/createdGroups.png)
![image alt](https://github.com/Salayne/ActiveDirectoryHomeLab/blob/main/OUs/createUser1.png)
![image alt](https://github.com/Salayne/ActiveDirectoryHomeLab/blob/main/OUs/createGroups2.png)
![image alt](https://github.com/Salayne/ActiveDirectoryHomeLab/blob/main/OUs/createGroups3.png)

**GROUP POLICY Management**
Windows admin tools -> Group Policy Management -> domain -> group policy object
Right click default domain controllers policy
  
***Set Password Policy***
- Is a computer configuration
- Right click on domain and select create a GPO in this domain, and Link it here
- Right click on Password Policy


***Drive Mapping GPO (maps network drives for user when they log in)***
- Right click on domain, create a gpo, name it drive mapping
- Is a User configuration, Preferences because it can be altered later on
- Preferences -> windows setting -> Drive Maps

***Restrict Access Control Policy*** 
- Prevents Users from accessing the Control Panel
- User Configuration
- Policies -> Administrative Template ->Control Panel

***Disable USB storage***
- Prevents users from using USB storage devices
- Computer Configuration -Policy

***Account Lockout Policy***
- Prevents brute force attacks
- In the Group Policy Management Editor window, navigate to the following path: Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Account Lockout Policy
- ***Account lockout threshold***: This is the most crucial setting. Set the number of invalid logon attempts that will cause an account to be locked out. A common recommendation is between 3 and 5 attempts. Setting it to 0 means the account will never be locked out.
- ***Account lockout duration***: This defines how many minutes a locked-out account remains locked before it automatically unlocks. A duration of 30 minutes is a standard choice. Setting it to 0 means an administrator must manually unlock the account.
- ***Reset account lockout counter after***: This sets the time in minutes after which the failed logon attempt counter resets. This value should typically be less than or equal to the Account lockout duration. For example, if you set the lockout duration to 30 minutes, you might set this to 30 minutes as well.



**End-User PC & Network Integration:**
- Create a virtual machine with Windows 11 and join it to the Active Directory domain you just created.
![image alt](https://github.com/Salayne/ActiveDirectoryHomeLab/blob/main/EndUserNetworkIntegration/joinServerandWin11-1.png)
![image alt](https://github.com/Salayne/ActiveDirectoryHomeLab/blob/main/EndUserNetworkIntegration/successfullAddedWin11.png)



**RESET PASSWORD**


Find the user that needs help.
![image alt](https://github.com/Salayne/ActiveDirectoryHomeLab/blob/main/Reset%20Password/findUser.png)

If the user needs to change password.
![image alt](https://github.com/Salayne/ActiveDirectoryHomeLab/blob/main/Reset%20Password/changePasswordAD.png)

If user is locked out of account.
![image alt](https://github.com/Salayne/ActiveDirectoryHomeLab/blob/main/Reset%20Password/unlockAccount.png)
