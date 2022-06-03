Launch your instance
To launch an Amazon EC2 instance using the AMI you selected, use the aws ec2 run-instances command. You can launch the instance into a virtual private cloud (VPC), or if your account supports it, into EC2-Classic.

Initially, your instance appears in the pending state, but changes to the running state after a few minutes.

EC2-VPC
The following example shows how to launch a t2.micro instance in the specified subnet of a VPC. Replace the italicized parameter values with your own.

` aws ec2 run-instances --image-id ami-xxxxxxxx --count 1 --instance-type t2.mi` {{execute}}

List your instances
You can use the AWS CLI to list your instances and view information about them. You can list all your instances, or filter the results based on the instances that you're interested in.

The following examples show how to use the aws ec2 describe-instances command.

The following command filters the list to only your t2.micro instances and outputs only the InstanceId values for each match.

 `aws ec2 describe-instances --filters "Name=instance-type,Values=t2.micro"`{{execute}}