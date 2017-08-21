# Introduction

This section covers elastic load balancers and auto scaling groups. An elastic load balancer is Amazon's propietary service used to balance traffic from the internet across a set of ec2 nodes. An autoscaling group is a way of dynamically increasing or decreasing the number of instances that an elb can allocate traffic to. You can read more about each following the links below:

Pre-requisites:

* [Packer]()

* [Elastic Load Balancers](https://aws.amazon.com/elasticloadbalancing/)
* [Auto Scaling Groups](http://docs.aws.amazon.com/autoscaling/latest/userguide/AutoScalingGroup.html)
* [Health Checks](http://docs.aws.amazon.com/autoscaling/latest/userguide/as-add-elb-healthcheck.html)
* [Attaching Load Balancers To AutoScaling Groups](http://docs.aws.amazon.com/autoscaling/latest/userguide/autoscaling-load-balancer.html)

The Test

1. Create an autoscaling group with a launch configuration for a R