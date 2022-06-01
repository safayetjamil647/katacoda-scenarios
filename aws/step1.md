We will install the cli here.This topic describes how to install or update the latest release of the AWS Command Line Interface (AWS CLI) on supported operating systems. For information on the latest releases of AWS CLI, see the AWS CLI change notes on GitHub.

Use the curl command – The -o option specifies the file name that the downloaded package is written to. The options on the following example command write the downloaded file to the current directory with the local name awscliv2.zip.

`curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip"`{{copy}}

Unzip the installer. If your Linux distribution doesn't have a built-in unzip command, use an equivalent to unzip it. The following example command unzips the package and creates a directory named aws under the current directory.
`unzip awscliv2.zip`{{copy}}

Run the install program. The installation command uses a file named install in the newly unzipped aws directory. By default, the files are all installed to /usr/local/aws-cli, and a symbolic link is created in /usr/local/bin. The command includes sudo to grant write permissions to those directories.
`sudo ./aws/install`{{copy}}

To locate the existing symlink and installation directory, use the following steps:

Use the which command to find your symlink. This gives you the path to use with the --bin-dir parameter.

`which aws`{{copy}}
Output: /usr/local/bin/aws

Confirm the installation with the following command.
 
`aws --version`{{copy}}
