# Introduction

This section covers elastic load balancers and auto scaling groups. An elastic load balancer is Amazon's propietary service used to balance traffic from the internet across a set of ec2 nodes. An autoscaling group is a way of dynamically increasing or decreasing the number of instances that an elb can allocate traffic to. You can read more about each following the links below:

* [Elastic Load Balancers](https://aws.amazon.com/elasticloadbalancing/)
* [Auto Scaling Groups](http://docs.aws.amazon.com/autoscaling/latest/userguide/AutoScalingGroup.html)
* [Health Checks](http://docs.aws.amazon.com/autoscaling/latest/userguide/as-add-elb-healthcheck.html)
* [Attaching Load Balancers To AutoScaling Groups](http://docs.aws.amazon.com/autoscaling/latest/userguide/autoscaling-load-balancer.html)

The Test

1. Create an autoscaling group with a launch configuration equal to the nginx ami that 
you created from the [Packer Module](https://github.com/generationtux/training-modules/blob/infrastructure-modules/Infrastructure/AWS/05-packer.md) set the default number of nodes to be 5.

2. Configure a load balancer to point at the auto scaling group, connect to the load 
balancer in the browser using the default domain name configured for the elb. 
