# Active-Directory
This Repository will contains various tools,scripts,commands used in Active Directory Enumeration and Exploitation


## Domain Enumeration
```
Get-NetDomain: it will Give  basic info about the other domain
Get-Net-Domain -Domain abc.local : it will give info about a domain "abc.local"
Get-DomainSID: Will give SID of current domain
Get-DomainPolicy: Will give info about the policies if the current doamin.
Get-NetDomainController: Info about the domain controller
```
## User Enumeration
```
Get-netuser: List all users in the current domain
Get-netuser -username test123 : Give info about the user test123
Get-UserProperty: List all properties of the user in current domain.
Get-UserProperty -properties pwdlastse: It will give info about the a property pwdlastset of all users in current domain.
Get-NetLoggedon -Computername server16 : It will tell all the users which are actively logged on to the computer.
Get-loggedonLocally : It will list all users who are logged in locally on the computer.
Get-LastLoggedon -Computername server016 : It will list user which have last logged on to the computer.
```
## Computer Enumeration

```
Get-NetComputer : It will list down all the computer object in the domain
Get-Netcomputer -FullData : It will list down all the properties of all computer objects in the domain.
Get-Netcomputer -OperatingSystem "*Server 2016*" : It will list down all the computer objects having Server 2016 as their operating system.
Get-Netcomputer -FullData | select OperatingSystem : It will list down all the OperatingSystem Property of all the computer objects.
Get-Netcomputer -Ping : It will check which of the computer objects are live in the domain.

```

## Group Enumeration

```
Get-NetGroup: It will list down all the groups 
Get-Netgroup 'Domain Admin' : It will check whether the Domain Admin group exists or not.
Get-Netgroup -GroupName "*admin*": It will return all those groups whose name contain the word "admin".
Get-NetgroupMember -groupname 'Domain Admin' : It will list down the members of the domain admins.
Get-Netgroup -Username "studentx" : Get the group membership of the user "studentx"
Get-netlocalgroup -computername xyz-dc.abc.local" List all local group on a machine.
```

## GPO Enumeration

