# Implement and manage virtual networking

`Application Gateway` manages HTTP/S traffic to web applications, not private connectivity between a web app and a VM in a virtual network.
`load balancer` manages traffic distribution but does not enable direct network connectivity between web apps and VMs.

In a `proximity placement group`, all resources are logically grouped to minimize latency by ensuring they are located within the same data center. Proximity placement groups are specific to a region and must be within a single resource group. Furthermore, each proximity placement group is associated with only one Azure Resource Group.

To create a `staging slot `for an Azure App Service plan, it must be in the Standard, Premium, or higher pricing tier. Since staging slots are not available for the Free, Shared, or Basic tiers, the solution here is to scale up Plan1 to a tier that supports deployment slots.

`Azure Container Instances` support only Linux and Windows containers, but for multi-container groups, all containers must be based on the same OS type.

` Azure Bastion `uses HTTPS on port 443 for secure communication from the user's browser to the Azure Bastion host.

`Azure Firewall` can connect to a virtual network within the same region and resource group.


port 53, which is used by the DNS service.