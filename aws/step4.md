Create you key pair by executing below command
`aws ec2 create-key-pair \
    --key-name my-key-pair \
    --key-type rsa \
    --key-format pem \
    --query "KeyMaterial" \
    --output text > my-key-pair.pem`
    {{copy}}

Make sure the aws cli installed properly

If you will use an SSH client on a macOS or Linux computer to connect to your Linux instance, use the following command to set the permissions of your private key file so that only you can read it.

`chmod 400 my-key-pair.pem`{{copy}}
If you do not set these permissions, then you cannot connect to your instance using this key pair.


Check the keypair installed properly installed or not

To describe a public key

Use the describe-key-pairs command and specify the --key-names parameter.

`aws ec2 describe-key-pairs --key-names my-key-pair`{{copy}}
