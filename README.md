## DevOps Columbus Azure Demo
This is simply a demo repository that contains everything necessary for speaking at the DevOps Columbus user group. You can find the presentation [here](https://drive.google.com/file/d/0B2eU0z_wEI6HSlRBLW95SlZOaXM/view?usp=sharing).

### Prerequisites
* [Visual Studio 2017](https://www.visualstudio.com/downloads/)
  * PC preferrable because there are more built-in features for free
* [Azure account with subscription setup](https://azure.microsoft.com/en-us/)
* [Install Azure CLI 2.0](https://docs.microsoft.com/en-us/cli/azure/install-azure-cli?view=azure-cli-latest)
  * PC or Mac is fine

### Steps
1. Create new solution and project
2. Publish to Azure
3. Store code in source control (GitHub, BitBucket, VSTS)
4. Setup continuous deployment via Azure portal
    * You can do this in Visual Studio as well
5. Download resource template and store in source control
6. Open terminal or command prompt and login to Azure (`az login`)
    * follow steps to login properly
7. Ensure directory is set to template file location 
8. Test resource template and parameters by executing a deployment 
    * `az group deployment create --name {{Name of deployment}} --resource-group {{Resource Group Name}} --template-file template.json --parameters parameters.json`
9. Witness the beauty/power of the resource templates
    1. In the Azure Portal, manually add a new Web App (follow prompts and wait until completed)
    2. In the terminal/command prompt, review the resources for the new one `az resource list`
    3. Run step 8 again, but with the property `--mode Complete`
        * The default is `--mode incremental`
    4. Run step ii and notice that the resource that was created is gone!

### Resources
* [Create and deploy to Azure via Visual Studio 2017](https://docs.microsoft.com/en-us/aspnet/core/tutorials/publish-to-azure-webapp-using-vs) 
* [Enabling continuous deployment](https://docs.microsoft.com/en-us/azure/app-service/app-service-continuous-deployment) 
* [Visual Studio Team Services (VSTS) builds and releases](https://docs.microsoft.com/en-us/vsts/build-release/actions/create-deploy-releases#create-from-build) 
* [Get existing resource template](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-manager-export-template) 
* [Deploy resource template](https://docs.microsoft.com/en-us/azure/azure-resource-manager/resource-group-template-deploy-cli?toc=%2fcli%2fazure%2ftoc.json&bc=%2fcli%2fazure%2fbreadcrumb%2ftoc.json&view=azure-cli-latest) 
* [Azure CLI command reference](https://docs.microsoft.com/en-us/cli/azure/group?view=azure-cli-latest#Commands) 
