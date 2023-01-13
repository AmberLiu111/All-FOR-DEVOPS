* [Paramiko](https://www.paramiko.org/)

Example-1: connect to the remote host and run script
```
### Login to the remote host ###
import sys
import paramiko
import time
ip_address = "192.168.2.106"
username = "student"
password = "training"
ssh_client = paramiko.SSHClient()
ssh_client.set_missing_host_key_policy(paramiko.AutoAddPolicy())
# remote trust 
ssh_client.load_system_host_keys()
ssh_client.connect(hostname=ip_address,\
username=username, password=password)
ssh_client.invoke_shell()
remote_connection = ssh_client.exec_command('cd Desktop; mkdir work\n')
# stdin, stdout, stderr = ssh_client.exec_command(“sudo ls”)
# print stdout.readlines()
remote_connection = ssh_client.exec_command('mkdir test_folder\n')
print( remote_connection.read() )
ssh_client.close
```
Example-2: File transfer
```
#Downloading a file from remote machine

ftp_client=ssh_client.open_sftp()
ftp_client.get('remotefileth','localfilepath')
ftp_client.close()

#Uploading file from local to remote machine

ftp_client=ssh_client.open_sftp()
ftp_client.put('localfilepath','remotefilepath')
ftp_client.close()
```
