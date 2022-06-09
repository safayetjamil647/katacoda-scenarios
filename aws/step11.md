Terminate your instance
Terminating an instance deletes it. You can't reconnect to an instance after you've terminated it.

As soon as the state of the instance changes to shutting-down or terminated, you stop incurring charges for that instance. If you want to reconnect to an instance later, use stop-instances instead of terminate-instances. For more information, see Terminate Your Instance in the Amazon EC2 User Guide for Linux Instances.

To delete an instance, you use the command
`aws ec2 terminate-instances --instance-ids i-1234567890abcdef0`{{copy}}
 to delete it.