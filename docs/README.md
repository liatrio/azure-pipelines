# Docs Page

## Tooling Recommendations

### Pipeline Orchestrator - Azure DevOps
Azure DevOps Pipelines are very well integrated with Azure. There is already a "Build Machine Image" Azure Pipeline 
task that we can utilize. This task can use custom Packer templates or the pipeline will generate it for you. This has
not been tested yet. 

_Userful Links:_
* [Microsoft Docs - Build Machine Image Task](https://docs.microsoft.com/en-us/azure/devops/pipelines/tasks/deploy/packer-build?view=azure-devops)
* [GitHub - Microsoft - azure-pipeline-tasks repo](https://github.com/Microsoft/azure-pipelines-tasks)

### Image Creation - Packer
[Packer.io](https://www.packer.io/) is tool designed to create images. It can use various provisioners including robust
provisions like [Ansible](https://www.ansible.com/) shell languages like Powershell or Bash. This is recommended for 
full VMs (i.e. Azure Images, Amazon Machine Images, etc) and not containers. 

_Useful Links_:
* [Packer Docs - Templates](https://www.packer.io/docs/templates/index.html)
* [Packer Docs - Azure Resource Manager Builder](https://www.packer.io/docs/builders/azure-arm.html)
* [Microsoft Docs - How to use Packer to create Windows virtual machines in Azure](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/build-image-with-packer)

### Provisioning
TBD

### Image Storage - Azure
Azure will host your VM images for you. There is a service called [Azure Shared Image Gallery](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/shared-image-galleries).
This will allow teams to share across the org. It can also be used with [Azure Virtual Machine Scale Sets](https://azure.microsoft.com/en-us/services/virtual-machine-scale-sets/).
It appears that you do not have to use this service if you would prefer to just have managed VM images. 

_Pricing (according to the [blog](https://azure.microsoft.com/en-us/blog/azure-shared-image-gallery-now-generally-available/))_:
* Storage charges for image versions and replicas in each region, source and target
* Network egress charges for replication across regions

_Useful Links_:
* [Microsoft Docs - Azure Shared Image Gallery Overview](https://docs.microsoft.com/en-us/azure/virtual-machines/windows/shared-image-galleries)
* [Microsoft Blog - Azure Shared Image Gallery now generally available](https://azure.microsoft.com/en-us/blog/azure-shared-image-gallery-now-generally-available/) 

# Other Useful Links
Step by step guide for building a windows image with packer using inline powershell provisioner:
https://docs.microsoft.com/en-us/azure/virtual-machines/windows/build-image-with-packer

Setting up a service principal:
https://docs.microsoft.com/en-us/cli/azure/create-an-azure-service-principal-azure-cli

Key Vault docs:
https://docs.microsoft.com/en-us/azure/key-vault/

AZ Powershell command reference:
https://docs.microsoft.com/en-us/powershell/module/?view=azps-3.3.0
