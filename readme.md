1. I created the cloud formation script using the YAML formart
2. I wrote a parameter which held our various resources
3. The first was the vpc, and then the internet gateway which would allow the vpc outbound from the resources
4. i created 4 subnets, 2 i made public and then 2 i made private
5. i provisioned Nat gateways, at the same time allocating an ip so it persist and doesnt change
6. I also provisioned and configured security group and autoscaling, and as well for scalability.

LB URL : http://udagr-webap-12fkhxr612zt9-108072105.us-east-1.elb.amazonaws.com/