Connect to your Linux instance using an SSH client
Use the following procedure to connect to your Linux instance using an SSH client. If you receive an error while attempting to connect to your instance, see Troubleshoot connecting to your instance.

To connect to your instance using SSH

In a terminal window, use the ssh command to connect to the instance. You specify the path and file name of the private key (.pem), the user name for your instance, and the public DNS name or IPv6 address for your instance. For more information about how to find the private key, the user name for your instance, and the DNS name or IPv6 address for an instance, see Locate the private key and set the permissions and Get information about your instance. To connect to your instance, use one of the following commands.

(Public DNS) To connect using your instance's public DNS name, enter the following command.

ssh -i /path/my-key-pair.pem my-instance-user-name@my-instance-public-dns-name