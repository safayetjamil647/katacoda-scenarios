Connect to your Linux instance using an SSH client
Use the following procedure to connect to your Linux instance using an SSH client. If you receive an error while attempting to connect to your instance, see Troubleshoot connecting to your instance.

To connect to your instance using SSH

In a terminal window, use the ssh command to connect to the instance. You specify the path and file name of the private key (.pem), the user name for your instance, and the public DNS name or IPv6 address for your instance. For more information about how to find the private key, the user name for your instance, and the DNS name or IPv6 address for an instance, see Locate the private key and set the permissions and Get information about your instance. To connect to your instance, use one of the following commands.

(Public DNS) To connect using your instance's public DNS name, enter the following command.

ssh -i /path/my-key-pair.pem my-instance-user-name@my-instance-public-dns-name
(IPv6) Alternatively, if your instance has an IPv6 address, to connect using your instance's IPv6 address, enter the following command.

ssh -i /path/my-key-pair.pem my-instance-user-name@my-instance-IPv6-address
You see a response like the following:

The authenticity of host 'ec2-198-51-100-1.compute-1.amazonaws.com (198-51-100-1)' can't be established.
ECDSA key fingerprint is l4UB/neBad9tvkgJf1QZWxheQmR59WgrgzEimCG6kZY.
Are you sure you want to continue connecting (yes/no)?
(Optional) Verify that the fingerprint in the security alert matches the fingerprint that you previously obtained in (Optional) Get the instance fingerprint. If these fingerprints don't match, someone might be attempting a "man-in-the-middle" attack. If they match, continue to the next step.

Enter yes.

You see a response like the following:

Warning: Permanently added 'ec2-198-51-100-1.compute-1.amazonaws.com' (ECDSA) to the list of known hosts.
Transfer files to Linux instances using an SCP client
One way to transfer files between your local computer and a Linux instance is to use the secure copy protocol (SCP). This section describes how to transfer files with SCP. The procedure is similar to the procedure for connecting to an instance with SSH.

Prerequisites

Verify the general prerequisites for transferring files to your instance.

The general prerequisites for transferring files to an instance are the same as the general prerequisites for connecting to an instance. For more information, see General prerequisites for connecting to your instance.

Install an SCP client

Most Linux, Unix, and Apple computers include an SCP client by default. If yours doesn't, the OpenSSH project provides a free implementation of the full suite of SSH tools, including an SCP client. For more information, see https://www.openssh.com.

The following procedure steps you through using SCP to transfer a file using the instance's public DNS name, or the IPv6 address if your instance has one.