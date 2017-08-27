# Introduction

Security groups are the equivalent to firewalls in aws. Security groups are used to 
control access to ec2 and rds resources in aws. Read the docs on security groups in 
aws before you begin the test.

* [Security Groups](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/using-network-security.html#vpc-security-groups)

The Test:

1. Launch an ec2 instance that allows all inbound traffic from port 80, but only
allows ssh access from a machine that is on a specific network.
