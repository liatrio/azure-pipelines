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

# Other Useful Links
Step by step guide for building a windows image with packer using inline powershell provisioner:
https://docs.microsoft.com/en-us/azure/virtual-machines/windows/build-image-with-packer

Setting up a service principal:
https://docs.microsoft.com/en-us/cli/azure/create-an-azure-service-principal-azure-cli

Key Vault docs:
https://docs.microsoft.com/en-us/azure/key-vault/

AZ Powershell command reference:
https://docs.microsoft.com/en-us/powershell/module/?view=azps-3.3.0
