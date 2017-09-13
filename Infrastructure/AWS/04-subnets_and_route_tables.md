In order to complete this module you will need to understand the following:

* [EC2](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/Instances.html)
* [What is an amazon vpc?](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Introduction.html)
* [VPC IP Addressing](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/vpc-ip-addressing.html)
* [CIDR Notation](https://en.wikipedia.org/wiki/Classless_Inter-Domain_Routing)
* [Subnet Basics](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Subnets.html#vpc-subnet-basics)
* [Elastic IP](http://docs.aws.amazon.com/AWSEC2/latest/UserGuide/elastic-ip-addresses-eip.html)
* [Nat Gateways](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/vpc-nat-gateway.html)
* [Internet Gateway](http://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/VPC_Internet_Gateway.html)

# The test:

1. Create a vpc with 65,536 available private ip addresses

2. Create a public subnet called - public-subnet-1 with 4,096 available ip addresses. Ensure that the subnet assigns a public
domain by default.

3. Create a private subnet called - private-subnet-1 that can connect to the internet but cannot receive connections from the internet

4. Launch an ec2 instance in each of the two subnets  (make sure you store ssh_keys so you can connect to the instances)

5. Create a branch in your training repo entitled answers-to-test-questions 
with a file called answers.txt. In that file the following questions with as 
much specificity as you need.

* What is the difference between a private and a public subnet in aws cloud 
services?

* What is a vpn only subnet?

* In the following ip address: 192.168.255.247 which 3 digit number 
represents the 'most significant bits'? Which one represents the 'least 
significant'?

* How would you represent all ip addresses in the  range from 10.0.32.0 - 
10.0.47.255 in CIDR notation?

* Using CIDR notation how would you specify a route for all ip addresses?


