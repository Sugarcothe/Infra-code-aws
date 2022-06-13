#CLOUD FORMATION

Creat a VPC in the cloud using cloud formation, using Yaml for provisioning and configuring and then json file for defining parameters.

#SUBNETS

Insisde two availability zones you created two subnets, one private and one public in one AZ, and same to the other making it zones.

#INTERNET GATEWAY

The first was the vpc, and then the internet gateway which would allow the vpc outbound from the resources

#VPC NAT

Create VPC NAT gateway for the public subnets to talk to the private subnets. Private Subnets are not reachable to the internet gateway. Internet gateway can only reach the public subnets. If we have our server in the private subnets, when a customer uses a logic in the server, it automatically gets to the public subnets and then public subnets get the information from the private subnets using the NAT gateway. 

#ROUTE TABLES

Provison the Route table to set the rule for the inbound and the outbound network. Because we might want network to move through the subnets in a certain way.

#AUTO-SCALING GROUP

Depending on were you have kept your server, either in the public or private subnet, is is a nice thing to provide an auto-scaling group, this will help in provisioning and terminating resources, if by any means it get so much workload to handle.

#LOAD BALANCER
The customer or whoever is using our service shouldnt be reaching our public subnets directly, so we have to place a load balancer after the internet gateway. So if someone reaching our service or website try to reach our resources using the internet Gateway, it would first reach the load balancer before reaching the subnets.

LB URL : http://udagr-webap-12fkhxr612zt9-108072105.us-east-1.elb.amazonaws.com/
