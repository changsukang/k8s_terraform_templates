## Terraform templates for Kubernetes on AWS and GCP
#### AWS
* [provider.tf](https://github.com/changsukang/k8s_terraform_templates/blob/main/aws/provider.tf)
  * declare these scripts run on AWS
* [vpc.tf](https://github.com/changsukang/k8s_terraform_templates/blob/main/aws/vpc.tf)
  * define virtual private cloud
* [subnet.tf](https://github.com/changsukang/k8s_terraform_templates/blob/main/aws/subnet.tf)
  * define public and private subnets and gateways
* [cluster.tf](https://github.com/changsukang/k8s_terraform_templates/blob/main/aws/cluster.tf)
  * set up k8s control plane
* [node_group.tf](https://github.com/changsukang/k8s_terraform_templates/blob/main/aws/node_group.tf)
  * run pods/containers on EC2
* [addon.tf](https://github.com/changsukang/k8s_terraform_templates/blob/main/aws/addon.tf)
  * set CNI (container network interface) up, not to use proxy/nat
* [iam_role.tf](https://github.com/changsukang/k8s_terraform_templates/blob/main/aws/iam_role.tf)
  * assign roles to cluster and node group to let them access and control components in VPC
* [security_group.tf](https://github.com/changsukang/k8s_terraform_templates/blob/main/aws/security_group.tf)
  * two security groups are defined, but not used yet.
#### GCP
* [provider.tf](https://github.com/changsukang/k8s_terraform_templates/blob/main/gcp/provider.tf)
  * declare these scripts run on GCP
* [vpc.tf](https://github.com/changsukang/k8s_terraform_templates/blob/main/gcp/vpc.tf)
  * define project on GCP
* [subnet.tf](https://github.com/changsukang/k8s_terraform_templates/blob/main/gcp/subnet.tf)
  * define subnets
* [router_nat.tf](https://github.com/changsukang/k8s_terraform_templates/blob/main/gcp/router_nat.tf)
  * define nat router for private nodes
* [cluster.tf](https://github.com/changsukang/k8s_terraform_templates/blob/main/gcp/cluster.tf)
  * set up k8s control plane
* [node_pool.tf](https://github.com/changsukang/k8s_terraform_templates/blob/main/gcp/node_pool.tf)
  * build nodes to run pods/containers
#### Docker
* [apache2_k8s/Dockerfile](https://github.com/changsukang/k8s_terraform_templates/blob/main/docker/apache2_k8s/Dockerfile)
  * a Docker template to run Apache2 with port 80 to serve a default index.html in Ubuntu
#### Helm
* [apache2_k8s/](https://github.com/changsukang/k8s_terraform_templates/tree/main/helm/apache2_k8s)
  * a Helm template to deploy a pod with the Docker image above, a service of NodePort, and an ingress as an external load balancer.
