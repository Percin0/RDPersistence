# RDPerci RDPersistence

# Usage
- Choose username and password and the RDP port.
- Run RDPerci.bat on victim
- Connect to victim with the username&password created and the specified port

# Description
RDPerci is ideal for SOC operators' first analysis. It's a simple script able to enable RDP and add new admin user with the access over it. It's inspired to famous malware that works with RDP. To allow multple RDP sessions it uses termsrv_rdp_patch.ps1 from winposh repository.

# How it works
RDPerci.bat will ask for admin's privileges, when it obtain that it will run. It create new user with a new password, and try to add to Administrator's group using the default name in different languages.
Then enable RDP on the target and change the default port. It creates an ACL on WindowsFirewall for RDP connection over the selected port.

# References
https://github.com/maxbakhub/winposh

https://attack.mitre.org/techniques/T1021/001/

https://github.com/redcanaryco/atomic-red-team/blob/master/atomics/T1021.001/T1021.001.md

# Disclamer 
Only for analysis do not use without authorization. Only for educational purpose.

# Contact
If you want to help me with any suggestions please contact me to percin0@protonmail.com :) 


# Screenshot

RDPerci on victim without RDP enable.
![Cattura](https://user-images.githubusercontent.com/94323404/153262514-2ad28c12-bf36-44db-af89-9e6c65530077.PNG)

Connection with the new user's credentials and the new port.
![Cattura2](https://user-images.githubusercontent.com/94323404/153262576-7ffbf271-004d-4297-ae8c-af9b543d421c.PNG)

![Cattura3](https://user-images.githubusercontent.com/94323404/153262682-06d76a32-d925-446b-b4ce-ce1a16c332b1.PNG)

You can do all you want, you are admin!
![Cattura5](https://user-images.githubusercontent.com/94323404/153262772-bc3bab4d-db3d-4bee-ab3f-ab3c17e01ec5.PNG)
