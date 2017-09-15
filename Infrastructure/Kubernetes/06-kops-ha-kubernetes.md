** Note Commands run in this module will create resources on aws. Make sure you clean up the resources created to avoid major charges

# Inroduction

[Kops](https://github.com/kubernetes/kops) is a tool used to configure and deploy kubernetes to the cloud. This module will walk you through the important parts of their documentation and 
give a test that will show your comprehension of using Kops. 

[AWS Basic](https://github.com/kubernetes/kops/blob/master/docs/aws.md)
[HA Cluster](https://github.com/kubernetes/kops/blob/master/docs/high_availability.md)
[Private network](https://github.com/kubernetes/kops/blob/master/docs/topology.md)
[Kubernetes Dashboard](https://kubernetes.io/docs/tasks/access-application-cluster/web-ui-dashboard/)

## The Test

1. Create a highly available kubernetes cluster across three availability zones using coreos
2. Deploy the kubernetes dashboard to the cluster
