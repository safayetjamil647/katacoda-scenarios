A key pair, consisting of a public key and a private key, is a set of security credentials that you use to prove your identity when connecting to an Amazon EC2 instance. Amazon EC2 stores the public key on your instance, and you store the private key. For Linux instances, the private key allows you to securely SSH into your instance.

Anyone who possesses your private key can connect to your instances, so it's important that you store your private key in a secure place.

When you launch an instance, you are prompted for a key pair. If you plan to connect to the instance using SSH, you must specify a key pair. You can choose an existing key pair or create a new one. When your instance boots for the first time, the public key that you specified at launch is placed on your Linux instance in an entry within ~/.ssh/authorized_keys. When you connect to your Linux instance using SSH, to log in you must specify the private key that corresponds to the public key.

Use the create-key-pair command as follows to generate the key pair and to save the private key to a .pem file.

For --key-name, specify a name for the public key. The name can be up to 255 ASCII characters.

For --key-type, specify either rsa or ed25519. If you do not include the --key-type parameter, an rsa key is created by default. Note that ED25519 keys are not supported for Windows instances.

For --key-format, specify either pem or ppk. If you do not include the --key-format parameter, a pem file is created by default.

--query "KeyMaterial" prints the private key material to the output.

--output text > my-key-pair.pem saves the private key material in a file with the specified extension. The extension can be either .pem or .ppk. The private key can have a name that's different from the public key name, but for ease of use, use the same name.

Please click on the next button for create a key pair by your own.