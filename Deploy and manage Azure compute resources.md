# Deploy and Manage Azure Compute Resources

To ensure that you can push and pull signed container images in ContReg1, you need to enable content trust. Content trust ensures that the integrity of the images is maintained by verifying that the images are signed and have not been tampered with. This allows only trusted and signed images to be pushed and pulled from the registry.

`Azure Policy` definitions can be assigned at any level in the Azure hierarchy, including the tenant root group, management groups, subscriptions,  resource groups, and individual resource.

`Tenant Root Group` cannot be excluded from policy assignments. Exclusions are applicable to management groups, subscriptions, resource groups, and individual resources only.

`DSC extension` allows you to define a desired state configuration for virtual machines in a scale set. This configuration can include installing and configuring software like NGINX on all virtual machines automatically after deployment.

`Service Tags` simplify network security group (NSG) rules by allowing you to reference a group of IP addresses associated with a specific Azure service.

App Service and Azure Container Instances both support Windows-based containers,
Azure App Service, Azure Container Apps, and Azure Container Instances all support Linux-based containers supports Linux-based containers

`ACR Tasks` are supported in all service tiers: `Basic, Standard, and Premium`. While there are performance and feature differences across the tiers (such as the number of concurrent tasks or webhook triggers), ACR Tasks functionality is available in all three tiers, including Basic.
- Premium tier of Azure Container Registry supports private endpoints. 