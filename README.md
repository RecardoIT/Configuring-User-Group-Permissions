<h1>File And User Permissions</h1>

 ### [YouTube Demonstration](https://youtu.be/7eJexJVCqJo)

<h2>Description</h2>
A project created within Oracle VirtualBox, in which i created two seperate virtual machines, one running Windows Server 2022 to manage Active Directory, and the second running Windows Enterprise. I also show how to configure an internal network inside of Windows Server 2022.

In this section, i will be going over how to set and configure permissions for files, folders and users within window and active directory.
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Diskpart</b>

<h2>Environments Used </h2>

- <b>Windows Server 2022</b> 
- <b>Windows 11 Enterprise</b> 

<h2>Program walk-through:</h2>

<p align="center">
To begin, click on the windows search icon, and search for "user" then click on "Active Directory Users and Computers"  <br/>
<img src="https://imgur.com/FPkDpOE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
This will open a window, where we can see our local domain that we created earlier, mine for example is "testdirectory.local" Left click on this space, and you will see an array of oragnizational units.   <br/>
<img src="https://i.imgur.com/U7ytgp0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Think of Organization Units as folders within windows, they help to keep the active directory tidy, as well as seperate different organisations within a domain. Right click on the "testdirectory.local" hover over new, and click Organizational Unit to create one of our own.   <br/>
<img src="https://i.imgur.com/MBR6mcC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
To simulate a working enviroment, lets name this organizational unit as "UK" we are then going to follow the same proccess and make two additional organizational units named "USA" & "ASIA"  <br/>
<img src="https://i.imgur.com/gIqbRPY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
After that, right click on the "UK" organizational unit we just made, and create 3 seperate organizational units inside of it, called "Computer" "Users" "Server" repeat this proccess for the "USA" and "ASIA" organizational units we created earlier. You will now see that our domain begins to grow a structure, just like it would in a real business!  <br/>
<img src="https://i.imgur.com/K0Swxs3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Now the complicated part is out of the way, we can move into creating a group. Right click on any of the "users" organizational units we created and select "new" "group" groups are created to hold a vast amount of users neatly, we'll get into adding users to these groups in just a moment!  <br/>
<img src="https://i.imgur.com/TEhGdX2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
From here, simply give your user a name and surname, here i have used the name "Simon Stone". If your group was called "admins" for example and you wanted to add multiple admin users to the group, then you may want to set the user login name to something like a-sstone. If you added a new user called "Adam Smith" then you could set their login name as "a-asmith" in order to keep the admin names consistent and neat.     <br/>
<img src="https://i.imgur.com/tlc22xi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Then, set a password for your new user, i recommend checking "password never expires" as users like to write down their passwords onto paper, and having them write new password every 2 months for example could serve as a security risk to a business! <br/>
<img src="https://i.imgur.com/v6oRHxr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
<br />
Lets make one more user to make sure you have got the hang of it. Right click on one of the "users" organizational units and select "new" "user" lets fill in their information again and set them a password like last time, this time i will create a user in the "USA" organizational unit. <br/>
<img src="https://i.imgur.com/v6oRHxr.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
This time i will name my user "Max Holloway" and then create another group in our "users" organizational folder called L1 Help Desk like last time. <br/>
<img src="" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In order to add a user into a group, right click on a chosen group and click "properties"  <br/>
<img src="https://imgur.com/HXipZk1.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Now, enter the name of the user you wish to join the following group, by typing out their name in the object names section.  <br/>
<img src="https://imgur.com/68MtEi9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Finally, press "ok" and then the "apply" button, and that users will now be added to your chosen group!  <br/>
<img src="https://imgur.com/0MMromZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
